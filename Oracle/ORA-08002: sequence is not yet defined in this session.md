# ORA-08002: sequence is not yet defined in this session

![image](https://github.com/GYUNGAEEEE/Troubleshooting/assets/158580466/84dd3f65-86fe-4fe2-8eeb-f169c58cb0f5)

## 원인
시퀀스의 NEXTVAL보다 먼저 CURRVAL이 호출되었기 때문이다.
CURRVAL은 현재 세션에서 마지막으로 반환된 NEXTVAL 값을 반환한다.

## 해결방법
NEXTVAL을 먼저 실행 후 CURRVAL을 실행
```
SELECT 시퀀스명.NEXTVAL FROM DUAL;
SELECT 시퀀스명.CURRVAL FROM DUAL;
```
