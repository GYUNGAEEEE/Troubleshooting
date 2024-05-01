# A problem occurred configuring root project 'hello-spring'
![image](https://github.com/GYUNGAEEEE/Troubleshooting/assets/158580466/092eb794-6ae3-426e-ac46-913b8589b7e1)

## 문제상황
intelliJ 첫 설치 후 project를 open 했더니 발생

## 원인
"Gradle이 Java 11과 호환되는 Spring Boot Gradle 플러그인을 찾지 못했다."   
Spring boot 3.x 버전은 Java 17 버전부터 지원한다.

## 해결방법
(1) 프로젝트 JDK 설정   
Ctrl+Shift+Alt+S를 눌러 SDK를 17로 변경

![image](https://github.com/GYUNGAEEEE/Troubleshooting/assets/158580466/83148c1c-a4fd-4f25-9e1b-3f2cea34b167)

(2) Gradle JDK 설정   
File > Settings > Build, Execution, Deployment > Build Tools > Gradle에서 Gradle JVM의 버전을 JAVA 17로 변경

![image](https://github.com/GYUNGAEEEE/Troubleshooting/assets/158580466/cac116bc-e583-4ec3-ab7a-4332dde8a1fd)

(3) Reload Gradle Project
***
위에 떠있는 경고창에서 Setup SDK를 17로 설정해주면...?

![image](https://github.com/GYUNGAEEEE/Troubleshooting/assets/158580466/51be80ea-c1f8-4488-820c-7c4f4860f76d)
