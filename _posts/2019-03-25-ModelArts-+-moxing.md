---
layout:     post
title:      ModelArts and Moxing
subtitle:   
date:       2019-03-25
author:     Denghui Liu
header-img: img/home-bg-art.jpg
catalog: true
tags:
    - modelArts
    - moxing
---
总结学习到的有关modelArts和moxing的知识点。

## 一. moxing
### 1.1. moxing的文件操作系统
MoXing支持本地和S3路径的读取，为了同时使用，可以import如下语句

    import moxing as mox

    mox.file.shift('os', 'mox')

mox的文件系统和os文件系统的对应关系如下：

    os.listdir        mox.file.list_directory()

    os.makedirs       mox.file.make_dirs

    os.mkdir          mox.file.mk_dir

    os.path.exists    mox.file.exists

    os.path.getsize   mox.file.get_size

    os.path.isdir     mox.file.is_directory

    os.remove         mox.file.remove()

    os.rename         mox.file.rename

    os.scandir        mox.file.scan_dir

    os.stat           mox.file.stat

    os.walk           mox.file.walk

    open              mox.file.File

    shutil.copyfile   mox.file.copy

    shutil.copytree   mox.file.copy_parallel

    shutil.rmtree     mox.file.remove

### 1.2. moxing的文件操作系统调用案例

读取OBS文件： 
    mox.file.read('s3://bucket_name/obs_file.txt')

写入OBS文件：
    mox.file.write('s3://bucket_name/obs_file.txt', 'Hello World!')

追加到一个OBS文件：
    mox.file.append('s3://bucket_name/obs_file.txt', '\nend of file.')

获取一个OBS文件(夹)的元信息：
    stat = mox.file.stat('s3://bucket_name/obs_file.txt')
    print(stat.length)
    print(stat.mtime_nsec)
    print(stat.is_directory)

移动一个OBS文件(夹)，s3 -> 本地：
    mox.file.rename('s3://bucket_name/obs_file.txt', '/tmp/obs_file.txt')
 拷贝一个OBS文件夹，s3 -> s3：
    mox.file.copy_parallel('s3://bucket_name/sub_dir_0', 's3://bucket_name/sub_dir_1')
  
  当读取OBS文件时，实际调用的是HTTP连接读去网络流，注意要记得在读取完毕后将文件关闭。为了防止忘记文件关闭操作，推荐使用with语句，在with语句退出时会自动调用mox.file.File对象的close()方法：
    with mox.file.File('s3://bucket_name/obs_file.txt', 'r') as f:
        data = f.readlines()
