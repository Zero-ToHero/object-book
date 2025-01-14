# 03. 역할, 책임, 협력
## 협력

- 객체는 자율적인 존재 → 객체 간 협력을 위한 유일한 커뮤니케이션 == 메세지 전송 (메서드 실행)
- 수신한 메세지를 처리하는 방법은 수신 객체 스스로 선택한다.
- 객체를 자율적으로 만드는 가장 기본적인 방법은 내부 구현을 캡슐화 하는 것

## 책임

- 협력에 참여하기 위해 객체가 수행하는 행동

### 책임할당

- 책임을 수행하는 데 필요한 정보를 가장 잘 알고 있는 전문가에게 책임을 할당

### 책임 주도 설계

- 책임을 찾고 책임을 수행할 적절한 객체를 찾아 책임을 할당하는 방식으로 협력을 설계하는 방법
    - 책임 파알 → 책임 분할 → 객체에게 책임 할당 → 다른 객체의 도움이 필요한 경우 그 객체에게 책임 할당 → 객체 협력

### 메세지가 객체를 결정한다

- 객체가 최소한의 인터페이스를 가질 수 있게 된다
    - 객체는 필요한 크기의 퍼블릭 인터페이스를 가진다
- 객체는 충분히 추상적인 인터페이스를 가질 수 있게 된다.
    - 객체의 인터페이스는 무엇을 하는지 표현해야 하지만 어떻게 수행하는지를 노출해서는 안된다.

## 역할

### 역할과 협력

- 역할 : 특정한 협력 안에서 수행하는 책임의 집합 (추상화)