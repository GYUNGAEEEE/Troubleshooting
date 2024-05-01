# FAILURE: Build failed with an exception.
![image](https://github.com/GYUNGAEEEE/Troubleshooting/assets/158580466/b164354d-0593-4714-b438-91b76c15fcef)

## 문제상황
콘솔에서 스프링 부트 애플리케이션을 빌드하고 실행하려 했는데 빌드에 실패

## 원인
Spring boot 3.x 버전은 Java 17 버전부터 지원한다.

## 해결방법
고급 시스템 설정 > 환경 변수 에서 환경 변수를 수정해준다. 
- Before   
![image](https://github.com/GYUNGAEEEE/Troubleshooting/assets/158580466/4c836d23-9cf0-4419-b7e4-b53f0940c935)

- After   
![image](https://github.com/GYUNGAEEEE/Troubleshooting/assets/158580466/2dac37fe-403c-4980-8d44-1ff73b77d577)

Java 버전이 잘 바뀌었는지 확인하는 명령어는 다음과 같다.
```
> java -version
```
