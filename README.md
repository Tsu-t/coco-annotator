<p align="center"><img src="https://i.imgur.com/AA7IdbQ.png"></p>

<p align="center">
  <a href="#features">Features</a> •
  <a href="https://github.com/jsbroks/coco-annotator/wiki">Wiki</a> •
  <a href="https://github.com/jsbroks/coco-annotator/wiki/Getting-Started">Getting Started</a> •
  <a href="https://github.com/jsbroks/coco-annotator/issues">Issues</a> •
  <a href="#license">License</a>
</p>

---

# Installation
## Install docker
```
sudo apt-get update
```
```
sudo apt-get -y install \
  apt-transport-https \
  ca-certificates \
  curl \
  gnupg-agent \
  software-properties-common
```
```
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
```
```
sudo add-apt-repository \
 "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
 $(lsb_release -cs) \
 stable"
```
```
sudo apt-get update
```
```
sudo apt-get -y install docker-ce docker-ce-cli containerd.io
```
```
sudo apt-get update
```
```
which docker && docker --version
```
/usr/bin/docker
Docker version 20.10.16, build aa7e414

## Install docker-compose
```
sudo curl -L "https://github.com/docker/compose/releases/download/1.25.4/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
```
```
sudo chmod +x /usr/local/bin/docker-compose
```
```
which docker-compose && docker-compose --version
```
/usr/local/bin/docker-compose
docker-compose version 1.25.4, build 8d51620a

## Setup coco-annotator
```
git clone https://github.com/jsbroks/coco-annotator.git
```

## docker setting
```
sudo gpasswd -a $YOUR_USERNAME docker
```
```
cat /etc/group | grep docker
```
docker:X:999:YOUR_USERNAME
```
sudo reboot
```

# Demo
```
cd coco-annotator
```
```
docker-compose up
```
Connect to http://localhost:5000 in your browser

| Login Information      |
| ---------------------- |
| **Username:** admin    |
| **Password:** password |

https://annotator.justinbrooks.ca/

# License

[MIT](https://tldrlegal.com/license/mit-license)

# Citation

```
  @MISC{cocoannotator,
    author = {Justin Brooks},
    title = {{COCO Annotator}},
    howpublished = "\url{https://github.com/jsbroks/coco-annotator/}",
    year = {2019},
  }
```
