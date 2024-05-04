# Project configuration is not up-to-date with pom.xml. Select: Maven->Update Project... from the project context menu or use Quick Fix.
![image](https://github.com/GYUNGAEEEE/Troubleshooting/assets/158580466/cceb3c3f-f16c-4392-a08a-6d492d5d8838)

## 문제상황
Maven Project 생성 후 pom.xml에 다음의 코드를 추가하였더니 발생
```xml
<dependencies>
  <dependency>
    <groupId>org.springframework</groupId>
    <artifactId>spring-context</artifactId>
    <version>5.2.9.RELEASE</version>
  </dependency>
</dependencies>

<build>
  <plugins>
    <plugin>
      <artifactId>maven-compiler-plugin</artifactId>
      <version>3.1</version>
      <configuration>
        <source>11</source>
        <target>11</target>
        <encoding>utf-8</encoding>
      </configuration>
    </plugin>
  </plugins>
</build>
```

## 원인
Maven Project의 설정이 pom.xml 파일과 일치하지 않음을 감지했을 때 발생하는 에러

## 해결방법
Maven Project를 업데이트하여 Maven 설정을 프로젝트와 동기화하여 프로젝트의 설정을 pom.xml 파일에 맞게 업데이트한다.   
프로젝트 마우스 오른쪽 버튼 > Maven > Update Project...

![image](https://github.com/GYUNGAEEEE/Troubleshooting/assets/158580466/5d7c14b9-3b47-489e-ac6a-27e9af8fcc70)

