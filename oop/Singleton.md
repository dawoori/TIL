# Singleton Pattern
해당 클래스의 인스턴스가 하나만 만들어지고, 어디서든지 그 인스턴스에 접근할 수 있도록 하기 위한 패턴. 자원관리의 효율성, 결과의 일관성.
ex) 스프링 빈은 default scope 싱글턴으로 관리된다.

## 싱글턴 패턴 구현
### static 변수를 사용
싱글턴 패턴의 목적 중 클래스의 인스턴스가 하나만 존재하도록 하는 목표를 달성할 수 없다. 게으른 인스턴스 생성을 할 수 없다.

### 고전적인 방법
```java
public class Singleton {
    private static Singleton uniqueInstance;

    private Singleton() {}

    public static Singleton getInstance() {
        if (uniqueInstance == null) {
            uniqueInstance = new Singleton();
        }
        return uniqueInstance;
    }
}
```
문제점
- Thread Safety를 보장할수 없다. 여러 스레드가 다른 싱글턴 객체를 사용하게 될 가능성이 있다.

### 멀티스레딩 문제 해결 방법 1
`getInstance()` 메소드를 동기화시키면 멀티스레딩 문제가 해결된다.
```java
public class Singleton {
    private static Singleton uniqueInstance;

    private Singleton() {}

    public static synchronized Singleton getInstance() {
        if (uniqueInstance == null) {
            uniqueInstance = new Singleton();
        }
        return uniqueInstance;
    }
}
```
단점
- 성능의 문제: 메소드를 동기화하면 성능이 100배정도 저하된다.

### 멀티스레딩 문제 해결 방법 2
인스턴스를 처음부터 만들어 버린다.
```java
public class Singleton {
    private static Singleton uniqueInstance = new Singlton();

    private Singleton() {}

    public static synchronized Singleton getInstance() {
        return uniqueInstance;
    }
}
```
싱글턴 인스턴스가 항상 필요한 경우 괜찮은 방법이다.

### 멀티스레딩 문제 해결 방법 3
DCL(Double Checking Locking)을 이용.
```java
public class Singleton {
    private volatile static Singleton uniqueInstance;

    private Singleton() {}

    public static Singleton getInstance() {
        if (uniqueInstance == null) {
            synchronized (Singleton.class) {
                uniqueInstance = new Singleton();
            }
        }
        return uniqueInstance;
    }
}
```
* `volatile`키워드를 사용하면 멀티스레딩을 쓰더라도 안전하게 진행할 수 있다.
동기화로 인한 오버헤드를 줄일수 있는 합리적인 방법이다. (자바 5 부터 사용 가능)