# object_book_study
---
『객체지향의 사실과 오해』에서는 협력, 책임, 역할의 관점으로 객체지향을 볼 수 있는 개념을 학습했다. 이 책을 통해 직접 여러 객체지향 구조들을 코드로 구현해보면서 객체지향에 관한 공부를 이어 나가 보자.

이 스터디의 주 목적은 책에 있는 코드를 직접 따라 치는 것에서 끝나는 것이 아니라 객체지향의 구조에 대해 스스로 생각할 수 있는 시간을 가지는 것이다.

---
## CHAPTER1
- 객체 사이의 의존성이 높을 경우 결합도가 높다고 말한다. **객체는 스스로 자신의 데이터를 처리할 수 있는(=책임 질 수 있는) 자율적인 객체로 만들어야 한다.**

- 자신의 데이터를 스스로 처리하는 자율적인 객체를 만들면 응집도가 높고 결합도가 낮은 객체를 만들 수 있다.

- 캡슐화의 목적은 변경하기 쉬운 객체를 만드는 것이다. 캡슐화를 통해 데이터와 기능을 객체 내부로 함께 묶고, 접근제어를 통해 객체 내부로의 접근을 제한하면 변경에 대한 파급효과를 제어할 수 있고 객체 간 결합도가 느슨해지기 때문에 자율적인 객체를 만들 수 있다.

- 소프트웨어 객체를 생물로 생각하자. 현실 세계에서는 수동적인 존재라도 객체지향의 세계에서는 능동적이고 자율적인 존재로 바뀐다. 이러한 방식으로 객체를 설계하는 원칙을 가리켜 의인화라고   부른다.

- 객체는 인터페이스와 구현으로 나누고, 인터페이스만을 공개하여 객체 사이의 결합도를 낮추고 변경하기 쉬운 코드를 작성해야 한다.
---
## CHAPTER2

- 객체 내부로의 접근을 제어하는 이유는 객체를 자율적인 존재로 만들기 위해서다. 객체지향의 핵심은 스스로 상태를 관리하고, 판단하고, 행동하는 자율적인 객체들의 공동체를 구성하는 것이다. 자율적인 객체는 외부의 간섭으로부터 최소화되야한다.

- 책임은 객체의 공용 인터페이스를 구성한다.

- 객체는 다른 객체의 인터페이스에 공개된 행동을 수행하도록 요청하고, 요청받은 객체는 자율적인 방법에 따라 요청을 처리한 후 응답한다. 객체는 다른 객체와 메세지를 통해서만 상호작용할 수 있다. 메세지를 수신한 객체는 자율적으로 메세지를 처리할 방법을 결정한다. 이처럼 수신된 메세지를 처리하기 위한 자신만의 방법을 메서드라고 부른다.

- 자식 클래스는 상속을 통해 부모 클래스의 인터페이스를 물려 받는다.
인터페이스는 객체가 이해할 수 있는 메세지의 목록을 의미한다. 
결과적으로 자식 클래스는 부모가 수신할 수 있는 메세지를 모든 메세지를 수신할 수 있기 때문에 
외부 객체는 부모 클래스와 자식 클래스를 동일한 타입으로 간주할 수 있다.

- 자식 클래스가 부모 클래스를 대신하는 것을 업캐스팅이라고 부른다.

- 동일한 메세지를 전송하지만 실제로 어떤 메서드가 실행될 것인지는 메세지를 수신하는 객체의 클래스가 무엇이냐에 따라 달라진다. 이를 다형성이라고 부른다.

- Movie와 DiscountPolicy는 합성관계로 이어져 있고, DiscountPolicy와 AmountDiscountPolicy, PercentDiscountPolicy는 상속관계로 연결돼 있다.
코드를 재사용하는 경우에는 상속보다 합성, 다형성을 위해 인터페이스를 재사용하는 경우에는 상속과 합성의 조합을 이용하는 것이 좋다.
---
## CHAPTER3

- 객체지향의 핵심은 역할, 책임, 협력이다. 협력은 애플리케이션의 기능을 구현하기 위해 메시지를 주고받는 객체들 사이의 상호작용이다. 책임은 객체가 다른 객체와 협력하기 위해 수행하는 행동이고, 역할은 대체 가능한 책임의 집합이다.

- 협력이란 객체들이 애플리케이션의 기능을 구현하기 위해 수행하는 상호작용을 말한다. 협력은 설계를 위한 문맥을 결정한다. 

- 두 객체 사이의 협력은 메세지 전송을 통해 이루어진다. 메세지를 수신받은 객체는 스스로 메세지를 처리할 수 있는 메서드를 선택하고 실행하여 요청에 응답한다. 

- 객체가 책임을 수행하게 하는 유일한 방법은 메세지를 전송하는 것이다.

- 협력이라는 문맥을 갖춘 후 협력에 필요한 행동을 수행할 수 있는 객체를 찾는다. 이때 협력에 참여하기 위해 객체가 수행하는 행동을 책임이라고 부른다.

- 책임을 수행할 적절한 객체를 찾아 책임을 할당하는 방법을 책임 주도 설계라고 부른다. 

- 객체에게 책임을 할당하는 데 필요한 메세지를 먼저 결정하고 메세지를 처리할 객체를 나중에 선택해야 한다. 

- 행동이 상태를 결정한다. 상태가 행동을 결정할 경우, 내부 구현이 공용 인터페이스에 노출되기 쉽기 때문에 캡슐화를 저해한다.

- 역할은 동일한 책임을 할 수 있는 다양한 종류의 객체를 끼워 넣을 수 있는 일종의 슬롯이다.

- 역할의 가장 큰 장점은 설계의 구성 요소를 추상화 할 수 있다는 것이고 상위 수준의 정책을 쉽고 간단하게 표현할 수 있다.

- 역할과 객체의 구분: 나중에 동일한 책임을 서로 다른 방식으로 수행할 수 있는 객체들이 필요해질 때가 왔을 때 역할의 도입을 고려해도 늦지 않다.


## CHAPTER5
- 메세지는 메세지를 수신할 객체가 아니라 메세지를 전송할 객체의 의도를 반영해서 결정해야 한다(= 메세지를 수행하는 메서드의 이름을 송신자 객체의 입장에서 작성). 

- 1. 메세지를 전송할 객체는 무엇을 원하는가?
- 2. 메세지를 수신할 적합한 객체는 누구인가?

- 정보 전문가 패턴에서 책임을 수행할 객체가 꼭 데이터를 가질 필요는 없다. 정보를 제공할 수 있다는 것은 정보 제공 객체를 알고 있는 것도 포함하기 때문이다. 

- 역할은 추상 클래스 또는 인터페이스를 사용한다.
- 추상 클래스: 역할을 대체하는 클래스들 사이에서 구현을 공유해야 할 필요가 있을 때 사용한다.
- 인터페이스: 역할을 대체하는 클래스의 책임만 정의하고 싶을 때 사용한다.

- 객체의 타입에 따라 변하는 로직을 if ~ else 또는 switch 를 통해 처리할 경우 프로그램이 수정될 경우 조건 논리를 수행해야 한다.
- 객체의 타입에 따라 변하는 행동이 있다면 타입을 분리하여 명시적인 클래스로 정의하고(상속 관계 설정) 각 타입에 다형적으로 행동하는 책임(@Override)을 할당하라. 이를 다형성 패턴이라고 부른다. 
