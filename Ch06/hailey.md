# 메시지와 인터페이스
- 퍼블릭 인터페이스 : 객체가 의사소통을 위해 외부에 공개하는 메시지의 집합
- 오퍼레이션 : 퍼블릭 인터페이스에 포함된메시지
  - 수행 가능한 어떤 행동에 대한 추상화
  - 내부의 구현 코드는 제외하고 단순히 메시지와 관련된 시그니처를 가리키는 경우가 대부분
- 시그니처 : 오퍼레이션(또는 메서드)의 이름과 파라미터 목록을 합쳐 부르는 이름

## 인터페이스와 설계 품질
- 좋은 인터페이스는 최소한의 인터페이스와 추상적인 인터페이스 조건을 만족해야 함
- 최소한의 인터페이스 : 꼭 필요한 오퍼레이션만을 인터페이스에 포함
- 추상적인 인터페이스 : 어떻게 수행하는지가 아니라 무엇을 하는지를 표현

=> 최소주의를 따르면서도 추상적인 인터페이스를 설계할 수 있는 가장 좋은 방법은 책임 주도 설계 방법을 따르는 것

### 디미터 법칙 : 협력하는 객체의 내부 구조에 대한 결합으로 인해 발생하는 설계 문제를 해결하기 위해 제안된 원칙
1. 객체의 내부 구조에 강하게 결합되지 않도록 협력 경로를 제한하라
2. 객체가 자기 자신을 책임지는 자율적인 존재여야 한다는 사실을 강조
3. 메서드가 작업을 어떻게 수행하는지를 나타내도록 이름 짓는 것 => 메서드의 이름은 내부의 구현 방법을 드러냄
4. 무엇을 하는지를 드러내는 것
   - 클라이언트의 관점에서 동일한 작업을 수행하는 메서드들을 하나의 타입 계층으로 묶을 수 있는 가능성이 커짐
   - 다양한 타입의 객체가 참여할 수 있는 유연한 협력을 얻게 됨
   - 의도를 드러내는 선택자(Intention Revealing Selector) 라고 부름
5. 의도를 드러내는 인터페이스(Intention Revealing Interface)
   - 의도를 드러내는 선택자를 인터페이스 레벨로 확장한 것
   - 구현과 관련된 모든 정보를 캡슐화하고 객체의 퍼블릭 인터페이스에는 협력과 관련된 의도만을 표현해야 함
   - 객체에게 묻지 말고 시키되 구현 방법이 아닌 클라이언트의 의도를 드러내야 함

## 원칙의 함정
원칙을 아는 것보다 더 중요한 것은 언제 원칙이 유용하고 언제 유용하지 않은지를 판단할 수 있는 능력을 기르는 것

## 명령-쿼리 분리 원칙
- 루틴 : 어떤 절차를 묶어 호출 가능하도록 이름을 부여한 기능 모듈
- 프로시저 : 정해진 절차에 따라 내부의 상태를 변경하는 루틴의 한 종류
  - 부수효과를 발생시킬 수 있지만 값을 반환할 수 없음
- 함수 : 어떤 절차에 따라 필요한 값을 계산해서 반환하는 루틴의 한 종류
  - 값을 반환할 수 있지만 부수효과를 발생시킬 수 없음
- 오퍼레이션은 부수효과르ㅏㄹ 발생시키는 명령이거나 부수효과를 발생시키지 않는 쿼리 중 하나여야함
- 어떤 오퍼레이션도 명령인 동시에 쿼리여서는 안됨
- 즉 질문이 답변을 수정해서는 안됨
- 명령은 상태를 변경할 수 있지만 상태를 반환해서는 안됨
- 쿼리는 객체의 상태를 반환할 수 있지만 상태를 변경해서는 안됨
- 책임 주도 설계 방법에 따라 메시지가 객체를 결정하게 해야 함
- 계약에 의한 설계(Design By Contract) : 협력을 위해 클라이언트와 서버가 준수해야 하는 제약을 코드 상에 명시적으로 표현하고 강제할 수 있는 방법