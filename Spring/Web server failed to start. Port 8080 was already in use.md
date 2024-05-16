# Web server failed to start. Port 8080 was already in use.
![image](https://github.com/GYUNGAEEEE/Troubleshooting/assets/158580466/4192af4a-a1fe-475a-9f7a-1b8e8f8ec869)

## 문제상황
APPLICATION FAILED TO START

## 원인
다른 프로세스가 이미 8080 포트를 사용하고 있기 때문에 포트 충돌 발생

## 해결방법 1
(1) 터미널 또는 명령 프롬프트에서 다른 프로세스가 8080 포트를 사용하고 있는지 확인
```
> netstat -ano | findstr 8080
```
(2) 프로세스의 PID를 확인한 후, 해당 프로세스를 종료한다. (여기서는 4128)
```
> taskkill /pid 4128 /f
```
(3) 프로세스(PID 4128)를 종료할 수 없습니다.

![image](https://github.com/GYUNGAEEEE/Troubleshooting/assets/158580466/bf761f86-52bb-4f85-8ca6-0aa42935bae8)

(4) 명령 프롬프트(CMD)를 '관리자 권한'으로 실행

![image](https://github.com/GYUNGAEEEE/Troubleshooting/assets/158580466/4d29d08c-c6c8-4c89-b1de-46d299c37f58)

## 해결방법 2
포트 번호 변경
- application.properties
```
server.port=변경할포트번호
```
