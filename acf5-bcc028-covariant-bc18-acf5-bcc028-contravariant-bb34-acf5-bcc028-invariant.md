* "T'가 T의하위클래스일때, Container\[T'\]가 Container\[T\]의하위클래스인가" 하는문제이다. \(여기서 T는타입, Container는 List같은자료구조\)
* 자식 클래스는 부모 클래스로부터 상속 받기 때문에 양적으로 같거나 더 많이 가지고 있다.
* 자식 클래스를 부모 클래스에 할당할 수 있다.부모 클래스를 자식 클래스에 할당할 수 없다. 더 적게 가지고 있기 때문이다. 한마디로 부모보다 자식이 더 잘났다.
* 상위타입이 쓰이는 곳에는 언제나 하위 타입의 인스턴스를 넣어도 이상이 없이 동작해야 한다는 의미이다.

공변

C\[T'\]는 C\[T\]의하위클래스이다. \[+T\]

반공변

C\[T\]는 C\[T'\]의하위클래스이다. \[-T\]

무공변성

C\[T\]와 C\[T'\]는아무관계가없다. \[T\]

스칼라에서 함수 선언은

val 함수이름: \(인자\) =&gt;리턴타입

으로 한다.

class GrandParents

class Parents extends GrandParents

class Child extends Parents

//리턴타입은 공변이다.

val covariantFunc:\(\) =&gt; GrandParents = \(\) =&gt; new Child

//함수 인자는 반공변이다.

val contravariantFunc:\(Child\) =&gt; String = \(a:GrandParents\) =&gt; "child"

스칼라 자료구조에서 +T는 양의 매개변수라고 부르기도 하는데 이는 List\[Child\]가 List\[Parents\]의 하위형식으로 간주된다는 것이다.

참조

[http://diehard98.tistory.com/entry/Covariance-and-Contravariance](http://diehard98.tistory.com/entry/Covariance-and-Contravariance)

