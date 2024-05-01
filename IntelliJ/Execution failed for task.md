# Execution failed for task ':HelloSpringApplication.main()'
![image](https://github.com/GYUNGAEEEE/Troubleshooting/assets/158580466/8222ef51-f1f3-4ea2-8bcd-e3080dc06ee3)

## 문제상황
기본 메인 클래스를 실행하였는데 발생

## 원인
Gradle 빌드 도중에 오류가 발생, 실행 환경에 문제가 있을 수 있다.

## 해결방법
File > Settings > Build, Execution, Deployment > Build Tools > Gradle에서 'Build and run using'과 'Run tests using'을
Gradle에서 IntelliJ IDEA로 변경

![image](https://github.com/GYUNGAEEEE/Troubleshooting/assets/158580466/b8bb642d-dbd3-4263-b5d4-e2444a932d14)
