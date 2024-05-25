# [IntelliJ] 한글 깨짐
![image](https://github.com/GYUNGAEEEE/Troubleshooting/assets/158580466/8a2b4354-a5cb-440e-839b-565893b3fd99)

## 문제상황
갑자기 한글이 깨진다!

## 해결방법
1. File > Settings > Editor > File Encodings 모든 설정을 UTF-8로 설정

![image](https://github.com/GYUNGAEEEE/Troubleshooting/assets/158580466/42a213f7-9408-463d-8223-9cf2d5e87366)

2. IntelliJ 실행시 사용할 가상 머신의 인코딩 설정을 지정
```
C:\Program Files\JetBrains\IntelliJ IDEA Community Edition 2024.1.1\bin
```
![image](https://github.com/GYUNGAEEEE/Troubleshooting/assets/158580466/0da0c307-bc67-40cd-80a4-7d7fb4fd20ff)

파일 맨 밑에 -Dfile.encoding=UTF-8 추가

![image](https://github.com/GYUNGAEEEE/Troubleshooting/assets/158580466/9926be67-74eb-49b5-92f8-764eedac631e)

해결 완료!

![image](https://github.com/GYUNGAEEEE/Troubleshooting/assets/158580466/e70b1db5-c51a-42d7-b524-66638978347c)
