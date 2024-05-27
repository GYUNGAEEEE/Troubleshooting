# [Workbench] Restore Workspace
![image](https://github.com/GYUNGAEEEE/Troubleshooting/assets/158580466/19fdc987-f3f4-4109-b32b-b19354ac0793)

## 문제상황
MySQL Workbench를 처음 부팅하면 발생(ignore하고 작업하여도 문제가 있지는 않음)

## 원인
이전 작업 공간 데이터를 복원하려고 할 때 설정 파일이 손상되었거나 비정상적인 종료로 인해 불완전하게 저장된 경우

## 해결방법
```
C:\Users\YOURUSER\AppData\Roaming\MySQL\Workbench\sql_workspaces
```
폴더 내 파일 모두 삭제

![image](https://github.com/GYUNGAEEEE/Troubleshooting/assets/158580466/b60a6172-a870-4353-971b-c1464377ae8e)
