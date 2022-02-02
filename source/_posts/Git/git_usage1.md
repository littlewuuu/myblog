---
title: 教会自己用 git
date: 2021-12-30 
tags: 
- 学了又忘的杂七杂八

categories:
- skills

toc: true # 是否启用内容索引
sidebar: none # 是否启用sidebar侧边栏，none：不启用
---

#实现本地文件和 Github 仓库同步
##Macbook Air M1 
1. ssh 等配置
2. 在 GitHub 上创建仓库
3. 准备好本地的文件存放位置
4. 切换终端目录到本地文件夹
5. 初始化本地文件夹
   ```git
   git init
   ```
6. 连接到 GitHub 仓库
    ```git
    git remote add origin 仓库网址（注意是 ssh 不是 url）
    ```
7. 切换
    ```git
     git branch -M main
    ```
8.  把想要上传的文件拖放到本地文件夹
9. 上传
    1. 将文件送到缓区
        1. 部分文件
        ```git 
        git add . //把本地文件夹的所有内容送到缓存区
        ```
        2. 所有文件
        ```git 
        git add filename //把指定的文件送到缓存区
        ```
    2. commit
    必须要有这一步，如果是全部文件到缓存区，则所有的文件都是这个注释，如果是指定文件到缓存区，则对指定文件注释
    ```git 
     Git commit -m “注释”  
     ```
    3. 上传
     ```git
     git push -u origin main  
     ```

