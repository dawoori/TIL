# OOP와 Design Pattern에 대하여

> **나중에 어떻게 바뀔 것인지**에 대해 생각한 결과 -> 관리가 용이한 객체지향 시스템을 제작 -> SOLID 원칙 -> 디자인 원칙 -> 디자인 패턴 (?)

> `디자인 패턴`이란 _나중에 어떻게 바뀔 것인지에 대한 생각_ 이라는 `인터페이스`의 `구현`

> **디자인은 예술이다**

### OOP
- 추상화 (abstraction)
- 캡슐화 (encapsulation)
- 다형성 (polymorphism)
- 상속 (inheritance)

### SOLID
- SRP (단일책임의 원칙: Single Responsibility Principle)
- OCP (개방폐쇄의 원칙: Open Close Principle)
- LSP (리스코브 치환의 원칙: The Liskov Substitution Principle)
- ISP (인터페이스 분리의 원칙: Interface Segregation Principle)
- DIP (의존성역전의 원칙: Dependency Inversion Principle)
- http://www.nextree.co.kr/p6960/

### 디자인 원칙
- 바뀌는 부분은 캡슐화한다.
- 구현이 아닌 인터페이스에 맞춰서 프로그래밍한다.
- 상속보다는 구성(composition)을 활용한다.
- 클래스는 확장에 대해서는 열려 있어야 하지만 코드 변경에 대해서는 닫혀 있어야 한다.(OCP)

## 디자인 패턴
|| Creational | Structural | Behavioral |
|---|---|---|---|
| Class | <ul><li>Factory Method</li></ul> | <ul><li>Adapter(class)</li></ul> | <ul><li>Interpreter</li><li>Template Method</li></ul> |
| Object | <ul><li>Abstract Factory</li><li>Builder</li><li>Prototype</li><li>Singleton</li></ul> | <ul><li>Adapter (object)</li><li>Bridge</li><li>Composite</li><li>Decorator</li><li>Facade</li><li>Flyweight</li><li>Proxy</li></ul> | <ul><li>Chain of Responsibility</li><li>Command</li><li>Iterator</li><li>Mediator</li><li>Memento</li><li>Observer</li><li>State</li><li>Visitor</li></ul>  |
