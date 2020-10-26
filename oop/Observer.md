# Observer Pattern
- 한 객체(`Subject`)의 상태가 바뀌면 그 객체에 의존하는 다른 객체(`Observer`)들에 연락이 가고 자동으로 내용이 갱신되는 방식으로 one to many 의존성을 정의한다.

## 옵저버 패턴의 핵심
- `Loose Coupling`: 서로 상호작용을 하는 객체 사이에는 가능하면 느슨하게 결합하는 디자인을 사용해야 한다.
### `Loose Coupling`? 왜?
- Subject는 Obsever에 대해 몰라도 된다. 아는 것은 오직 Observer 인터페이스를 구현한다는 것.
- Observer를 추가하는 일은 매우 쉽다. (확장에 대해 열려있음 -> OCP)
- 새로운 형식의 Obsever를 추가 할 때, Subject는 신경쓰지 않아도 된다.
- Subject와 Observer는 서로 독립적으로 재사용 가능.
- Subject나 Observer의 변경이 서로에게 영향을 미치지 않는다.


## Java 내장 옵저버 패턴
- `Observable` **클래스**, `Observer` 인터페이스
