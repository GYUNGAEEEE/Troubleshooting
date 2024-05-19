# H2 DataBase 추가 생성 에러

![image](https://github.com/GYUNGAEEEE/Troubleshooting/assets/158580466/987ec22f-70ac-4123-bed5-27096f2e8a00)

## 문제상황
이전에 만들어 놓은 첫번째 데이터 저장소가 있는 상황에서 추가 저장소를 생성하려고 하였는데 발생

## 원인
첫번째 데이터 저장소 생성 방법과 동일하게 생성할 수 없다. (추측)

## 해결방법
1. h2.bat 실행 후, H2 Database Engine를 통해 Create a new database...

![image](https://github.com/GYUNGAEEEE/Troubleshooting/assets/158580466/f0c288be-6809-42ef-866c-bb594c0bc4dc)

2. 저장하고 싶은 경로와 Password를 입력하여 Create

![image](https://github.com/GYUNGAEEEE/Troubleshooting/assets/158580466/f2d2b892-77b9-4a95-a059-0420f5193367)

지정한 경로 밑에 -.mv.db 파일이 생성됨을 확인할 수 있다.

![image](https://github.com/GYUNGAEEEE/Troubleshooting/assets/158580466/0e5f6be9-c899-42f4-bca5-18b405c4035f)

3. JDBC URL 'jdbc:h2:tcp://localhost/저장경로'와 Password를 입력하여 연결

![image](https://github.com/GYUNGAEEEE/Troubleshooting/assets/158580466/2c105b51-e0d1-42ba-8c0e-abab228f8458)

(추가) 
```
ALTER USER SA SET PASSWORD '';
```
사용자의 비밀번호를 공백('')으로 변경하여 비밀번호 입력없이 연결할 수 있도록 한다.
