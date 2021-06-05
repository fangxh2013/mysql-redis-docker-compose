# mysql-redis-docker-compose

## 步骤：

1. 安装docker,docker-compose

   

2. 拉取mysql5.7镜像，参考：https://hub.docker.com/_/mysql

   ```shell
   docker pull mysql:5.7
   ```

3. 拉取redis镜像，参考：https://hub.docker.com/_/redis

   ```shell
   docker pull redis
   ```

4. 准备redis配置文件，参考：https://github.com/redis/redis/blob/unstable/redis.conf

   修改内容如下：

   ```
   bind 127.0.0.1 #注释掉这行
   protected-mode no #默认yes，开启保护模式：本地访问
   dir  /data #redis数据库目录
   appendonly yes #redis持久化
   ```

   

5. 进入目录下执行:

   ```shell
   docker-compose up -d
   ```

   

