# Could not initialize class com.thoughtworks.xstream.converters.collections.PropertiesConverter
![image](https://github.com/GYUNGAEEEE/Troubleshooting/assets/158580466/47e1023d-83c4-42ba-802d-1349f79771cf)

## 문제상황
STS 설치 후 Spring Legacy Project를 생성하는 도중 발생

## 원인
클래스가 클래스패스에 없거나 클래스를 초기화하는 데 필요한 종속성이 누락되었거나 잘못 설정되었을 때 발생

## 해결방법
STS.ini 파일을 찾아 이클립스에서 사용할 JDK 버전을 명시해준다.

![image](https://github.com/GYUNGAEEEE/Troubleshooting/assets/158580466/b3fdb628-53c5-43bd-8bc7-e9d0fa6f97de)
