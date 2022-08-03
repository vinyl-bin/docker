<try1 설명>

다음의 코드를 실행할 것.   
`docker run -d -p <your port>:1234 ghcr.io/vinyl-bin/try1 node /home/app2`

http://<your ip>:<your port> 로 접속

<your ip>는 $ ifconfig 해서 wlp에 inet에 있는 번호 혹은 localhost다.

or

<try1 설명2>
1. 이미지 pull하기(링크 복사 붙여넣기)
2. '# docker run -t -i --name <원하는 이름> -p <호스트포트>:<컨테이너포트> <저장소이름(생략가능)/이미지 이름:이미지 버전'   
    ex) docker run -t -i --name new -p 5555:6666 ghcr.io/vinyl-bin/try1:latest
3. cd home/app2
4. vim index.js
   i 눌러서 포트번호를 자신이 지정한 포트번호로 바꾸고(ex)6666) esc누른 후 wq누르고 엔터를 누른다.
5. npm start
6. 다른 터미널에 ifconfig를 눌러 wlp1s0의 inet 뒤에 있는 번호를 확인한다.(공유기 ip임)
7. http://공유기ip:호스트
