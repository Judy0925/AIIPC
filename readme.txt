1.install docker

要在Ubuntu上下载和安装Docker，可以按照以下步骤进行操作：

1.#更新apt软件包列表：
sudo apt update

2.#安装必要的软件包以允许apt使用HTTPS源：
sudo apt install apt-transport-https ca-certificates curl gnupg-agent software-properties-common

3.#添加Docker的官方GPG密钥：
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

4.#添加Docker的APT存储库：
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"

5.#更新apt软件包列表：
sudo apt update

6.#安装Docker CE：
sudo apt install docker-ce

7.#验证Docker是否已成功安装并正在运行：
sudo docker run hello-world



以上步骤应该可以在Ubuntu上成功下载并安装Docker。如果需要进一步的帮助或信息，请参考Docker官方文档。

默认情况下，只有root用户和docker组的用户才能运行Docker命令。我们可以将当前用户添加到docker组，以避免每次使用Docker时都需要使用sudo。命令如下：
sudo usermod -aG docker $USER
注：重新登录才能使更改生效

8.我们可以通过启动docker来验证我们是否成功安装。命令如下：
systemctl start docker

9.重启docker
service docker restart



2.install docker-compose
#打开终端并输入以下命令下载 Docker Compose 的二进制文件：
sudo curl -L "https://ghproxy.com/https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
#在下载完成后，将 docker-compose 文件设置为可执行权限：
sudo chmod +x /usr/local/bin/docker-compose
#最后，输入以下命令验证 Docker Compose 是否成功安装：
docker-compose --version

3.install node:
sudo docker pull node:14.21.3

4.install mongo:
sudo docker pull mongo:4.0.28