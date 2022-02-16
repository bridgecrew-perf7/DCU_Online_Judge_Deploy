## Windows 10

# requirements
Docker, Docker-compose 설치

### Docker
WSL2 기반 Docker 설치
[Docker-desktop install](https://www.docker.com/products/docker-desktop)

Docker - Setting - General에서
Docker-Compose V2 옵션 적용
![image](https://user-images.githubusercontent.com/40351426/143538687-36a4bb2f-0727-4404-911b-649b48cb0dea.png)

이후 아래 명령어를 통해 각 컨테이너 이미지 내려받기 & 컨테이너 compose up 진행

```
docker-compose -f docker-compose.yaml up -d
# 개발 환경 구성의 경우 docker-compose -f docker-compose-develop.yaml up -d
```

## Linux

Docker, Docker-compose 등 필요 소프트웨어 설치

```bash
sudo apt-get update && sudo apt-get install -y vim python-pip curl git
pip install docker-compose
```

Docker 설치
```bash
sudo curl -sSL get.docker.com | sh
```

## 설치 과정

터미널에서 아래 명령어 입력

```bash
git clone https://github.com/DCUSnSLab/DCU-Online-Judge-Deploy.git
```

이후 해당 경로로 이동한 뒤 아래 명령어 입력


```bash
docker-compose -f docker-compose.yaml up -d
# 개발 환경 구성의 경우 docker-compose -f docker-compose-develop.yaml up -d
```

서비스 URL은 ```localhost:80``` 
초기 Admin 계정은 ```root```, 패스워드는 ```rootroot``` 입니다.

## pgadmin4

docker-compose 시 개발 환경 구성으로 셋업하는 경우,
데이터베이스 확인을 위한 pgadmin4 컨테이너를 포함하여 compose를 진행합니다.
pgadmin4 디폴트 계정 ID / PW는 아래와 같습니다.

admin@admin.com
root

# Forked by
https://github.com/QingdaoU/OnlineJudgeDeploy/tree/2.0
