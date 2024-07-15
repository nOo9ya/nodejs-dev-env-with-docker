# Nodejs development environment with docker
docker(alpine) = php-fpm + mariadb + redis + node

# …or repository from the command line
```shell
git clone https://github.com/nOo9ya/nodejs-dev-env-with-docker.git

# or

git init
git remote add origin https://github.com/nOo9ya/nodejs-dev-env-with-docker.git
git branch -M main
git add .
git commit -am "first init"
git push -u origin main

# or

git init --initial-branch=main
git remote add origin https://github.com/nOo9ya/nodejs-dev-env-with-docker.git
git add .
git commit -am "first init"
git pull origin main
```


```shell
# 개발환경은 아래와 같이 실행하여 시작합니다.
docker-compose up --build --force-recreate

# docker cache 로 문제가 발생될 수 있으므로 아래와 같이 실행하여 캐시로 인한 문제를 회피하며 빌드
docker builder prune -af
docker-compose build --no-cache
```

## node 개발 파일이 없을 시 접근 후 설치
```shell
docker exec -it nuxt-js /bin/sh
# node 개발에 필요한 command 입력
```

## node 개발 소스 설치가 완료 되었다면 다시 실행
```shell
docker compose down
docker compose up --build --force-recreate
```