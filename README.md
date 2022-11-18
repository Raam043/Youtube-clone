# `Youtube-clone` Installation with Docker
Directly you can run this app by using docker images pls visit my DcokerHub account => **[raam043](https://hub.docker.com/u/raam043)**
```sh
docker run --name greetings -d -p 80:80 raam043/youtube-clone
```

Release linux server and install Jenkins and Docker

```sh
yum update -y
yum install docker -y
systemctl enable docker
systemctl start docker
yum install pip -y
pip install docker-py

yum install git -y
```
Make app directory and add Application files using git clone
```sh
rm -rf /opt/youtube/*
mkdir /opt/youtube
cd /opt/youtube
git clone https://github.com/Raam043/Youtube-clone.git
cp /opt/youtube/Youtube-clone/* /opt/youtube

```

Build Docker images and Run container 
```sh
docker stop youtube
docker rm -f youtube
docker image rm -f youtube
docker build -t youtube .
docker run --name youtube -d -p 80:80 youtube
```
Open New tab with `Server_Public_IP:`

With Above commands Jenkins CICD can be made

Output :- 

![Screenshot 2022-11-18 at 11 26 03 PM](https://user-images.githubusercontent.com/111989928/202771051-eb65723e-c92b-4c41-bea6-2f73e5d8e24a.png)



