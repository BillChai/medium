# docker跟docker-compose的差別

[主要文章]([url](https://medium.com/@chaiyomin/docker%E8%B7%9Fdocker-compose%E7%9A%84%E5%B7%AE%E5%88%A5-842958041349))

## 概要

文章中比較了docker跟docker-compose的差別，並要在這個repository中示範用`DOCKER FILE`製作一個image並用`docker-compose.yaml`來組建一個service。

## 內容

1. 使用`python`的`flask`來創建一個簡易的網頁服務
2. 使用`nginx`來代理flask應用

資料夾中的文件位置

```sh
❯ tree
.
├── README.md
├── app
│   ├── Dockerfile (falsk的image)
│   ├── app.py (flask的啟動框架)
│   └── requirements.txt(python的配置文件)
├── docker-compose.yaml(整個服務的容器)
└── nginx
    └── default.conf(nginx的代理配置)

3 directories, 6 files
```

## How to Build

```sh
docker-compose build
docker-compose up -d
```

## How to Start

```sh
❯ curl http://localhost:8080/
Hello from Flask!%
```
