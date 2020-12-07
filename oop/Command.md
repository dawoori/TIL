# Command Pattern
![structure](img/commnad_uml.png)
요구 사항을 객체로 캡슐화 할 수 있으며, 매개변수로 여러 가지 다른 요구 사항을 집어 넣을 수도 있다. 요청 내역을 큐에 저장하거나 로그로 기록, 작업취소 등의 기능도 지원 가능하다.

`Receiver`의 `action()` 메소드를 직접 노출하지 않고 `Command`를 통해 `execute()` 메소드 하나만 외부에 공개하게 된다. `Client`는 `Invoker`를 통해서 요구 사항을 처리하게 된다. `Invoker`는 `Command`를 통해 요구 사항을 처리하고 `Receiver`가 어떤식으로 구현 되어 있는지 신경 쓸 필요가 없어진다.
