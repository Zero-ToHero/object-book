# 객체지향 프로그래밍
### 객체지향이란 객체를 지향하는 것!
1. 어떤 객체들이 필요한지 고민하라
   - 어떤 객체들이 어떤 상태와 행동을 가지는지를 먼저 결정해야함
   - 객체를 중심에 두는 접근 방법은 설계를 단순하고 깔끔하게 만듦
2. 객체를 독립적인 존재가 아닌 기능을 구현하기 위해 협력하는 공통체의 일원으로 봐야함
   - 장점 :  설계를 유연하고 확장 가능하게 만듦
3. 자율적인 객체
   - 상태와 행동을 함께하는 복합적인 존재
   - 객체가 스스로 판단하고 행동하는 자율적인 존재

### 객체지향의 핵심은 스스로 상태를 관리, 판단, 행동하는 자율적인 객체들의 공동체를 구성하는 것
### => 외부의 간섭을 최소화해야함

### 도메인 : 문제를 해결하기 위해 사용자가 프로그램을 사용하는 분야
1. 클랙스의 이름은 대응되는 도메인 개념의 이름과 동일하거나 유사하게 지어야함
2. 최대한 모데인 개념 사이에 맺어진 관계와 유사하게 만들어서 프로그램의 구조를 이해하고 예상하기 쉽게 만들어야 함
3. 도메인의 개념과 관계를 반영하도록 프로그램을 구조화해야함

### 다향성 : 어떤 메서드가 실행될 것인지는 메시지를 수신하는 캑체의 클래스가 무엇이냐에 따라 달라짐
- 다형적입 협력에 참여하는 객체들은 모두 같은 메시지를 이해할 수 있어야 함
- 지연 바인딩(lazy binding), 동적 바인딩(dynamic binding) : 메시지와 메서드를 실행 시점에 바인딩

