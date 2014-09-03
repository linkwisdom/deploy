eploy
======

测试环境快速部署工具

> eploy 线下测试环境快速部署工具，支持[`D`]eploy前的最终效果验证 

### 动机
- 自动提交本地patch到目标机器
- 测试机器自动部署代码
- 开发环境自动提供预览效果

### 安装

npm install eploy -g

- 自动部署代码

### 原理

- 自动更新主干代码
- 生成本地diff文件
- 通过post方式提交diff文件
- 将本地patch文件push到目标机器
- 目标机器更新主干代码
- 目标机器自动patch上传的diff文件
- 目标机器自动触发部署脚本

### 使用方法

#### 配置

```sh
    eploy set baseDir ~/work/fengchao/workspace
    eploy set workDir ~/work/fengchao/workspace/nirvana-workspace
    eploy set autoUpdate true
    eploy set deployTarget 'http://fctest.baidu.com/fcinsta/upload'
    eploy addTarget 'http://dev025.baidu.com:8189/upload'
```

#### 上传文件

```sh
    eploy push [options]
```
