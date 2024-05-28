# Caused by: org.attoparser.ParseException: Instantiation of new objects and access to static classes or parameters is forbidden in this context
## 문제상황
파라미터로 넘어온 값을 다음과 같이 사용
```
${param.no}
```

## 원인
Thymeleaf 3.0.12 버전 이후로 보안 정책상 제한되었다.

## 해결방법
Model에 담아 전달하여 사용하였다.
```java
model.addAttribute("scheduleNo", scheduleNo);
```
```html
${scheduleNo}
```
