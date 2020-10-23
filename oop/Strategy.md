# Strategy Pattern

### 스트래티지 패턴의 핵심
- 알고리즘군(바뀌는 부분)을 캡슐화하여
- How? 상속보다는 구성(composition)을 활용

```uml
Object <|-- Dummy

class Dummy {
  String data
  void methods()
  -field1
  #field2
  ~method1()
  +method2()
}

class Flight {
   flightNumber : Integer
   departureTime : Date
}

class Car

Driver - Car : drives >
Car *- Wheel : have 4 >
Car -- Person : < owns

```

## 상속에 대하여
- 수퍼클래스에 특정 메소드가 추가되면서 일부 서브클래스에 적합하지 않은 행동이 전부 추가될 수 있다.
- 이게 왜?
- 수퍼클래스를 수정하면 서브클래스들을 모두 살펴보고 오버라이드 해야 하는 불상사가 생길 수 있다.
- 