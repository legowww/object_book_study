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

- 동일한 메세지를 전송하지만 실제로 어떤 메서드가 실행될 것인지는 메세지를 수신하는 객체의 클래스가 무엇이냐에 따라 달라진다. 즉, 동일한 메세지를 수신받고 다르게 반응하는 것을 다형성이라고 부른다.

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

- 메세지를 전송할 객체는 무엇을 원하는가? NEXT 메세지를 수신할 적합한 객체는 누구인가?

- 정보 전문가 패턴에서 책임을 수행할 객체가 꼭 데이터를 가질 필요는 없다. 정보를 제공할 수 있다는 것은 정보 제공 객체를 알고 있는 것도 포함하기 때문이다. 

- 역할은 추상 클래스 또는 인터페이스를 사용한다.
- 추상 클래스: 역할을 대체하는 클래스들 사이에서 구현을 공유해야 할 필요가 있을 때 사용한다.
- 인터페이스: 역할을 대체하는 클래스의 책임만 정의하고 싶을 때 사용한다.

- 객체의 타입에 따라 변하는 로직을 if ~ else 또는 switch 를 통해 처리할 경우 프로그램이 수정될 경우 조건 논리를 수행해야 한다.

- 객체의 타입에 따라 변하는 행동이 있다면 타입을 분리하여 명시적인 클래스로 정의하고(sequence -> SequenceCondition) 각 타입에 다형적으로 행동하는 책임(@Override)을 할당하라. 이를 다형성 패턴이라고 부른다. 

- 객체로 책임을 분배할 때 가장 먼저 할 일은 메서드를 응집도 있는 수준으로 분해하는 것이다. 긴 메서드는 읽기 어렵고 재사용하는 것이 불가능하고 코드 중복을 초래하기 쉽다.

- 그 다음으로 해야할 일은 객체를 자율적으로 만드는 것이다. 메서드가 사용하는 데이터를 저장하고 있는 클래스로 메서드를 이동시키면 된다.

- 책임 주도 설계, 즉 객체에게 책임을 할당하는 작업이 어렵게 느껴진다면 일단 데이터 중심으로 구현한 후 리팩터링을 통해 결과물을 얻을 수 있다. 

- 생성자, 다형성, 정보 보호 패턴을 CHATRER5 코드와 주석을 통해 읽어보자

## CHAPTER6

- 메세지를 통해 객체간의 협력이 이루어진다.

- 객체의 책임은 수신받을 수 있는 메세지의 기반이된다. 객체가 수신하는 메세지들이 모여 퍼블릭 인터페이스를 구성한다.

- 퍼블릭 인터페이스란 객체가 협력에 참여하기 위해 외부에서 수신할 수 있는 메세지의 묶음이다. 퍼블릭 인터페이스의 품질이 객체의 품질을 결정한다.

- 객체지향 어플리케이션에서 가장 중요한 재료는 클래스가 아니라 객체가 주고받는 메세지이다. 

- 메세지는 전송자와 수신자 사이의 협력 관계를 강조하는 데 비해 오퍼레이션은 메세지를 수신하는 객체의 인터페이스를 강조한다. 

- 메서드는 메세지에 응답하기 위해 실행되는 코드 블럭이다. 메서드는 오퍼레이션의 구현이며 동일한 오퍼레이션이라고 해도 다형에 의해 다른 메서드를 호출 할 수 있다.

- 흐름: 메세지전송 -> 오퍼레이션 호출 -> 메서드 실행

- 객체가 메세지를 수신받을 때, 객체의 타입에 따라 실행되는 메서드가 달라질 수 있다. 메세지와 메서드가 실행시점에 연결되며 이를 통해 두 객체간 결합도가 낮아진다.

- condition.isSatisfiedBy(screening) = 수신자.오퍼레이션명(인자)

퍼블릭 인터페이스의 품질에 영향을 미치는 요소


```java
1. 디미터 법칙: 객체의 내부 구조에 강하게 결합되지 않도록 협력 경로를 제한하라, 하나의 도트(.)만 사용하라
디미터 법칙을 따르는 코드는 메세지 수신자의 내부 구조가 전송자에게 노출되지 않으며(캡슐화 증대), 메세지 전송자는 
수신자의 내부 구현에 결합되지 않는다. 따라서 클라이언트와 서버 사이에 낮은 결합도를 유지 할 수 있다.

클래스 내부의 메서드가 아래 조건을 만족하는 인스턴스에만 메세지를 전송하도록 프로그래밍해야 한다.
<this 객체, this의 속성, this의 속성인 컬렉션의 요소, 메서드의 매개변수, 메서드 내에서 생성된 지역객체>


public class ReservationAgency {
    public Reservation reserve(Screening screening, Customer customer, int audienceCount) {
        Money fee = screening.calculateFee(audienceCount);
        return new Reservation(customer, screening, fee, audienceCount);
    }
}
- 디미터 법칙 적용 -> 메서드의 인자인 Screening 인스턴스에만 메세지를 전송하고 있다. 인스턴스의 내부 구조에 대해서는 전혀 알고있지 않다.
calculateFee()는 Screening 의 퍼블릭 인터페이스이지 내부 구조라고 할 수 없다.

screening.getMovie().getDiscountConditions();
- 디미터 법칙 위반 -> 기차가 충돌된 모양처럼 생겨서 기차 충돌이라고 부르는 코드이다. 
getter()를 통해 내부의 객체들을 참조하는 형태의 코드를 가진다. 
수신자인 screening에게 내부 구조에 대해 물어보고 있으며 메세지 전송자가 메세지 수신자의 내부 구현에 강하게 결합된다.
```
```java
2. 묻지 말고 시켜라: 디미터 법칙의 코딩 스타일
screening.getMovie().getDiscountConditions(); 처럼 객체의 상태에 대해 묻지 말고 
screening.calculateFee(audienceCount); 처럼 원하는 것을 시켜라

객체의 정보를 이용하는 행동을 객체의 외부가 아닌 내부에 위치시키기 때문에 높은 응집도를 가진 클래스를 얻을 수 있다.
```
```java
3. 의도를 드러내는 인터페이스: 인터페이스는 객체가 "어떻게" 하는지가 아니라 "무엇을" 하는지를 서술해야 한다. 
무엇을에 초점을 맞출 경우 동일한 작업을 수행하는 메서드들을 하나의 타입 계층으로 묶을 수 있는 가능성이 커진다.

isSatifiedByPeriod, isSatifiedBySequence -> isSatifiedBy 

이유
- 두 메서드의 내부 구조를 이해하지 못하면 두 메서드가 동일한 작업을 수행한다는 사실을 알아채기 어렵다.
- 할인 방법이 달라질 경우 메서드의 이름을 변경해야 한다. 그 말은 메서드를 사용하는 클라이언트(전송자)의 코드도 변경해야 한다.
- 동일한 인터페이스를 가지고 있지 않으므로 다형적으로 행동하는 책임(@Override)을 사용할 수 없다. 
 
```

```java
4. 명령-쿼리 법칙: CHAPTRE6 코드 참조
```
