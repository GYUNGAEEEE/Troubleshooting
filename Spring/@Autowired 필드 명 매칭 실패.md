# @Autowired 필드 명 매칭 실패
```java
@Component
public class FixDiscountPolicy implements DiscountPolicy { }
```
```java
@Component
public class RateDiscountPolicy implements DiscountPolicy { }
```
```java
@Autowired
public OrderServiceImpl(MemberRepository memberRepository, DiscountPolicy rateDiscountPolicy) {
    this.memberRepository = memberRepository;
    this.discountPolicy = rateDiscountPolicy;
}
```
```
org.springframework.beans.factory.UnsatisfiedDependencyException: Error creating bean with name 'orderServiceImpl' defined in file [C:\springStudy\core\out\production\classes\hello\core\order\OrderServiceImpl.class]: Unsatisfied dependency expressed through constructor parameter 1: No qualifying bean of type 'hello.core.discount.DiscountPolicy' available: expected single matching bean but found 2: fixDiscountPolicy,rateDiscountPolicy
```

## 문제상황
조회 대상 빈이 2개 이상일 때 '@Autowired 필드 명 매칭' 방법을 이용하여 해결이 안되는 상황

## 원인
스프링 부트 3.2부터 매개변수의 이름을 인식하지 못하는 문제가 있다.

## 해결방법
Gradle을 사용해서 빌드하고 실행한다.

File > Settings > Build, Execution, Deployment > Build Tools > Gradle 에서
Build and run using을 'IntelliJ IDEA'에서 'Gradle'로 바꿔준다.

![image](https://github.com/GYUNGAEEEE/Troubleshooting/assets/158580466/f7cfa397-5458-4464-a088-20700f74dad5)
