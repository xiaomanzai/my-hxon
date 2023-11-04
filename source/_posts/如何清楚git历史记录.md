---
title: "git如何清楚历史记录"
date: 2023-11-04T07:53:58.907Z
tags: git
category: 技术
---
#### 创建新的孤儿分支

``` bash
1. git checkout --orphan latest_branch
```

#### 增添本地文件

``` bash
2.git add -A

```

如果你是 idea 那么直接添加就行

#### 删除主分支

``` bash
git commit -am "master"
```

#### 重命名当前分支

``` bash
git branch -m master
```

#### 强制提交

``` bash
git checkout --orphan latest_branch
```


接着去 GitHub 修改

![image.png](https://s2.loli.net/2023/11/04/Z26aUVOGqjQIPCo.png)

设置主分支
![image.png](https://s2.loli.net/2023/11/04/uyp9CiAsdt2q3Nz.png)

修改分支成 master 或者 main 
