# 사용법

1. git clone을 받기
2. clone 받은 파일에 .env, .gitignore 만들기
3. .env에 

    MYSQL_USER=checkit<br>
    MYSQL_PASSWORD=checkit<br>
    MYSQL_ROOT_PASSWORD=checkit<br>
    MYSQL_DATABASE=chekit<br>
    위 내용을 작성해주고 .gitignore에 .env 적어주기
<br>
4. 터미널을 켜 clone 받은 파일로 이동 = 현재 있는 폴더에 Dockerfile이 있어야 함<br>
5. 터미널에 `docker build -t check-it-mysql .` 입력<br>
6. build가 끝났으면 `docker image ls` 입력 후 mysql이라는 이미지가 생성되어 있는지 확인<br>
7. 생성되어 있다면 `docker run --name check-it-mysql -p 3306:3306 -h localhost --env-file ./.env -d mysql`<br>
