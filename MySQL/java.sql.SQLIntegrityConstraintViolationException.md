# java.sql.SQLIntegrityConstraintViolationException
```
Cause: java.sql.SQLIntegrityConstraintViolationException: Cannot add or update a child row: a foreign key constraint fails
```
## 문제상황
UPDATE 쿼리문을 실행했는데 발생

## 원인
외래 키(FK) 제약 조건 위반
- 쿼리에서 지정한 참조값이 테이블에 존재하지 않는 경우
- 외래 키가 올바르게 설정되지 않았거나, 참조하는 테이블과의 관계가 잘못 설정된 경우
- 데이터베이스의 무결성 제약 조건이 손상된 경우

## 해결방법
UPDATE를 수행하려는 컬럼의 FK의 값이 참조하는 테이블에 존재하지 않았다.
값이 잘못 설정된 부분을 수정하였다.
