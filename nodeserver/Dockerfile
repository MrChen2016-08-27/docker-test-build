#基于cenos
FROM centos:7.3.1611

#维护者信息
MAINTAINER chenjianbin 1909916440@qq.com

WORKDIR /home/nodeServer

# 首先安装 wget
RUN yum install -y wget

# 安装 nodejs linux版本
RUN wget https://nodejs.org/dist/v10.16.3/node-v10.16.3-linux-x64.tar.xz

# 解压
RUN tar -xvf node-v10.16.3-linux-x64.tar.xz

# 删除多余的tar压缩包空间
RUN rm -rf node-v10.16.3-linux-x64.tar.xz

# 部署bin文件
RUN ln -s /home/nodeServer/node-v10.16.3-linux-x64/bin/node /usr/bin/node
RUN ln -s /home/nodeServer/node-v10.16.3-linux-x64/bin/npm /usr/bin/npm


# 安装pm2
RUN npm install -g pm2

# 配置全局变量
RUN ln -s /home/nodeServer/node-v10.16.3-linux-x64/bin/pm2  /usr/local/bin/pm2



# CMD [ "/bin/bash" ]








