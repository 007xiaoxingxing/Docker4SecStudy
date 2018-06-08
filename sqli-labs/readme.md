#### 镜像说明
由于我最近想系统的学习一下sql注入的基础知识，所以找到了sqli-lab这个项目。之前也尝试在虚拟机上搭建过，但是每次都需要去搞环境很麻烦，正好最近也在学习docker，顺便就写个Dockerfile来构建一下镜像，以后就可以随时随地的生成镜像了。
#### 使用
1. 克隆仓库，进入到sqli-labs目录
   git clone https://github.com/007xiaoxingxing/Docker4SecStudy.git && cd sqli-labs
2. 构建
    docker build -t sqli-labs .
3. 运行镜像
    docker run --privileged -itd -p 82:80 --name sqlilab sqlilabs
    这里的需要映射的端口和容器名称就任意发挥了，我映射到了82端口。

容器运行之后，就可以打开浏览器访问docker服务器所在ip的82端口进行实验学习了。
