# org.h2.jdbc.JdbcSQLNonTransientConnectionException: Connection is broken: "java.net.ConnectException: Connection refused: no further information: localhost" [90067-224]

![image](https://github.com/GYUNGAEEEE/Troubleshooting/assets/158580466/d248e69c-1c63-4059-a761-3e2821bf4fbc)

## 문제상황
JPA에서 데이터베이스와 연결할 수 없어서 발생한 오류

## 원인
H2 데이터베이스를 실행하지 않아 발생

## 해결방법
H2 데이터베이스를 실행하여 해결
