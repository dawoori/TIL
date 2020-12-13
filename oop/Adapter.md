# Adapter Pattern
한 클래스의 인터페이스를 클라이언트에서 사용하고자 하는 다른 인터페이스로 변환한다.

![object](img/object_adapter.png)
![class](img/class_adapter.png)

어댑터 패턴을 사용하면 `Client`는 `Adaptee`클래스를 마치 `Target`클래스인것 처럼 쓸 수 있게 된다.
* 클래스 어댑터 패턴을 쓰려면 다중 상속이 필요한데, 자바에서는 다중 상속이 불가능하다.