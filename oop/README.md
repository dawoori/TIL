# OOP와 Design Pattern에 대하여

> **나중에 어떻게 바뀔 것인지**에 대해 생각한 결과 -> 관리가 용이한 객체지향 시스템을 제작 -> SOLID 원칙 -> 디자인 원칙 -> 디자인 패턴 (?)

> `디자인 패턴`이란 _유지보수에 용이하게 코딩하라_ 는 `인터페이스`의 `구현`

> **디자인은 예술이다**

### OOP
- 추상화 (abstraction): 모델링
- 캡슐화 (encapsulation)
- 다형성 (polymorphism)
- 상속 (inheritance)

### SOLID
- SRP (단일책임의 원칙: Single Responsibility Principle): 어떤 변화에 의해 클래스를 변경해야 하는 이유는 오직 하나뿐이어야 한다.
- OCP (개방폐쇄의 원칙: Open Close Principle): 자신의 확장에는 열려 있고, 주변의 변화에 대해서는 닫혀 있어야 한다.
- LSP (리스코브 치환의 원칙: The Liskov Substitution Principle): 서브 타입은 언제나 자신의기반 타입(base type)으로 교체할 수 있어야 한다. 다형성 (polymorphism)
- ISP (인터페이스 분리의 원칙: Interface Segregation Principle): 클라이어트는 자신이 사용하지 않는 메서드에 의존 관계를 맺으면 안 된다.
- DIP (의존성역전의 원칙: Dependency Inversion Principle): 자신보다 변하기 쉬운 것에 의존하지 마라.
- 개인적인 생각: SOLID 원칙 중 OCP가 메인인듯?
- http://www.nextree.co.kr/p6960/

### 디자인 원칙
- 바뀌는 부분은 캡슐화한다.
- 구현이 아닌 인터페이스에 맞춰서 프로그래밍한다.
- 상속보다는 구성(composition)을 활용한다.
- 클래스는 확장에 대해서는 열려 있어야 하지만 코드 변경에 대해서는 닫혀 있어야 한다.(OCP)
- 서로 상호작용을 하는 객체 사이에는 가능하면 느슨하게 결합하는 디자인을 사용해야 한다.

## 디자인 패턴
|| Creational | Structural | Behavioral |
|---|---|---|---|
| Class | <ul><li>Factory Method</li></ul> | <ul><li>Adapter(class)</li></ul> | <ul><li>Interpreter</li><li>Template Method</li></ul> |
| Object | <ul><li>Abstract Factory</li><li>Builder</li><li>Prototype</li><li>Singleton</li></ul> | <ul><li>Adapter (object)</li><li>Bridge</li><li>Composite</li><li>Decorator</li><li>Facade</li><li>Flyweight</li><li>Proxy</li></ul> | <ul><li>Chain of Responsibility</li><li>Command</li><li>Iterator</li><li>Mediator</li><li>Memento</li><li>[Observer](Observer.md)</li><li>State</li><li>[Strategy](Strategy.md)</li><li>Visitor</li></ul>  |
