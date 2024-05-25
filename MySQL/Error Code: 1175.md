# Error Code: 1175
```
You are using safe update mode and you tried to update a table without a WHERE that uses a KEY column.  
To disable safe mode, toggle the option in Preferences -> SQL Editor and reconnect.
```

## 문제상황
테이블의 모든 데이터를 delete하려했더니 발생
```
delete from testTable;
```

## 원인
safe update mode 상태에서 WHERE절 사용없이 테이블의 update를 시도하여 발생

## 해결방법
1. MySQL Workbench에서 Edit > Preferences > SQL Editor의 Safe Updates 체크 해제

![image](https://github.com/GYUNGAEEEE/Troubleshooting/assets/158580466/372f021a-94ff-40ec-9231-5b05efada2b3)

2. MySQL Workbench 재부팅
