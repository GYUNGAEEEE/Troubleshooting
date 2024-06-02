# com.mysql.cj.exceptions.UnableToConnectException: Public Key Retrieval is not allowed

## 문제상황
MySQL DB 접속 불가

## 원인
MySQL 8.0 버전부터는 DB에 접속하려면  url, username, password 뿐만 아니라 useSSL 옵션에 대한 추가적인 설정이 필요하다.
MySQL 8.0은 'caching_sha2_password' 인증 메커니즘을 사용하는데 SSL을 사용하지 않고 공개키 인증을 허용하지 않으면(설정하지 않으면) 클라이언트는 서버에 연결할 때 인증을 수행하지 못하게 되어 오류가 발생한다.

## 해결방법
연결 url에 "allowPublicKeyRetrieval=true" 옵션을 추가한다.
```
url=jdbc:mysql://...?useSSL=false&allowPublicKeyRetrieval=true
```
