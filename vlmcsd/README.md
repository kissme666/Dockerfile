# 本镜像是什么？

本镜像是使用vlmcsd构建的Docker镜像，用于批量激活Windows系统

## 搭建

仅需一条命令就可以使用

* 使用docker 命令启动
```bash
docker run -d  -p 1688:1688 evildocker/kms:latest
```

* 使用docker-compose 启动（需要下载相应的docker-compose 文件具体请访问Github项目地址）


```bash
docker-compose up -d
```


**测试**

```bash
# 输出有successful即搭建成功
./vlmcs-Windows-x64.exe -v -l 3 your kms server domain or ip
```


### Windows 使用

具体请Google搜索 vlmcsd 激活

https://github.com/kissme666/Dockerfile/tree/master/vlmcsd