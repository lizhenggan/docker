## 使用说明

```
克隆项目到本地
cd 到本地目录
```

目前PHP挂载目录在
```
../Code
```
你可以在docker-compose.yml 中修改挂载配置

nginx配置文件在
```
vhost
```

```
docker-compose up -d
```
就这样 你就拥有了 PHP5.6 + redis + mysql5.6 + nginx 的环境

### 配置swoole
cd 到swoole目录执行
```
bash ./build.sh
```

docker-compose.yml 配置
```
  swoole:
    image: swoole-server:0.1
    ports: 
        - "8080:8080"
    volumes:
        - /var/www:/var/www/html
```
