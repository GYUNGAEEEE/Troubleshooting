# ORA-12519: TNS:적절한 서비스 처리기를 찾을 수 없습니다.
![image](https://github.com/GYUNGAEEEE/Troubleshooting/assets/158580466/3811eae5-36b1-4ef2-8c4b-8f1b370271bb)

## 문제상황
웹 사이트 개발 중 ORA-12519 에러가 발생 + 성능 저하 현상과 페이지 요청의 무한 로딩

## 원인 (1)
접속 가능한 오라클 프로세스 수를 초과한 경우 발생하는 오류

## 해결방법 (1): 프로세스 수의 한계값을 늘려준다.
```
SQL> conn /as sysdba -- sys 관리자 계정 접속
SQL> alter system set processes=200 scope=spfile; -- 프로세스 한계값을 200으로 늘리기
SQL> commit; -- 커밋
SQL> shutdown immediate; -- DB 종료
SQL> startup; -- DB 시작
```
만약 프로세스 수의 한계값이 작아서 발생한 문제라면 위의 방법으로 문제가 해결될 수 있다.

하지만, 새로 설정한 한계값까지도 프로세스 수가 계속해서 늘었고 문제가 해결되지 않았다.
따라서, 프로세스가 늘어나는 상황을 파악하도록 하였다.
```
SQL> select * from v$resource_limit where resource_name = 'processes'; -- 프로세스 제한 정보 가져오기
```

## 원인 (2)
DB Connection을 닫지 않는다면, 프로세스가 계속해서 활성 상태로 유지될 수 있다.
따라서, Connection을 확실히 close()하지 않는다면, 프로세스 수를 늘리는 원인이 될 수 있다.

## 해결방법 (2): Connection close()

DB Connection을 수행한 후 close()해주지 않은 것이 원인이었다.
try-with-resources문을 사용하여 Connection을 자동으로 close()하여 리소스 누수를 사전에 방지하도록 코드를 변경하였다.
