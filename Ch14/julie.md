## 협력을 일관성 있게 만들기 위한 지침
1. 변하는 개념을 변하지 않는 개념으로부터 분리하라
2. 변하는 개념을 캡슐화하라

## 데이터 은닉
- 오직 외부에 공개된 메서드를 통해서만 객체의 내부에 접근할 수 있게 제한함으로써,
객체 내부 상태의 구현을 숨기는 기법을 의미한다

## 캡슐화
- 단순히 데이터를 감추는 것이 아니라, 소프트웨어 안에서 변할 수 있는 어떤 개념이라도 감추는 것을 말한다
-  일관성 있는 협력의 핵심은 변경을 분리하고 캡슐화하는 것이다

만약 애플리케이션에서 유사한 기능에 대한 변경이 지속적으로 발생한다면,
**변경을 캡슐화할 수 있는 적절한 추상화를 찾은 후**,
이 추상화에 변하지 않는 공통적인 책임을 할당하는 것이 좋다