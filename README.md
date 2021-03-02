# useful-command-list



디렉토리 뒤짐
find . *.log

데이터베이스(mlocate)를 뒤져서
locate *.log

실행파일 위치 찾기
whereis ls

압축 하기
tar -czvf name-of-archive.tar.gz /path/to/directory-or-file
-c: Create an archive
-z: Compress the archive with gzip.
-v: Display progress 
-f: Allows you to specify the filename

압축 풀기
tar -xzvf archive.tar.gz
-x extract

파이프
|
> file write
>> file add

패키지 목록들을 업데이트
apt-get update

패키지 찾기
apt-cache search [패키지명]
apt-get install [패키지명]
apt-get upgrade
apt-get upgrade [패키지명]
apt-get remove [패키지명]


/bin: 사용자가 사용하는 명령어 모음
/sbin: 관리자가 사용하는 명령어 모음
/etc: 프로그램 설정을 관리하는 디렉토리
/etc/init.d: daemon의 목적을 가진 프로그램들 있음.
/var: 내용이 바뀔 수 있는 파일들 모음
/tmp: 임시파일들. 컴퓨터가 꺼지면 날아간다.
/home: 사용자들의 파일들이 저장되는 디렉토리
/lib: /bin과 /sbin에 있는 프로그램들이 사용하는 라이브러리 모음
/usr: 유저가 다운받은 프로그램들 저장..

백그라운드 실행
ctrl + z

백그라운드로 돌아가는 프로그램 확인
jobs

포그라운드로
fg


현재 접속한 계정의 정보 확인
id

계정 추가
sudo useradd -m [사용자명]

루트 권한 추가
sudo usermod -a -G sudo [사용자명]

비번 변경
passwd 

; - 앞의 명령어가 실패해도 다음 명령어가 실행
&& - 앞의 명령어가 성공했을 때 다음 명령어가 실행
& - 앞의 명령어를 백그라운드로 돌리고 동시에 뒤의 명령어를 실행


http://pyrasis.com/Docker/Docker-HOWTO
docker
docker search ubuntu
docker pull ubuntu:latest

docker run -it --name hello ubuntu /bin/bash
ctrl p q

docker start hello
docker restart hello
docker attach hello
docker exec hello echo "Hello World"
docker rm hello
docker rm `docker ps -aq`

docker rmi ubuntu:latest


docker run --name hello-nginx -d -p 80:80 -v /root/data:/data hello:0.1
-v 공유폴더
-p host:container

docker cp <컨테이너 이름>:<경로> <호스트 경로>

