# JVM에서 자바 메모리 관리(Xms, Xmx)


자바 메모리 관리는 기본적으로 새로운 객체를 할당하고 적절하게 미사용 객체를 삭제하는 과정이다.

이번 글에서 자바 가상머신(JVM)를 논의하고 메모리 관리, 메모리 모니터링 도구, 메모리 모니터링 사용법에 대해 알아본다.

## JVM

* `JVM`은 컴퓨터가 자바 프로그램을 실행하는 데 사용되는 가상 머신이다.

* `JVM`은 메모리 관리를 자동으로 처리하여 **자바 애플리케이션의 성능을 최적화**한다.

* 메모리 관리는 `Xms`와 `Xmx`라는 JVM 옵션을 사용하여 구성할 수 있다.

## Xms

* `Xms`(Initial Java Heap Size): JVM이 시작될 때 할당하는 **최소 힙(heap) 크기**를 지정한다.

* 힙은 자바 애플리케이션의 런타임 데이터, 객체 인스턴스 및 배열을 저장하는 메모리 영역이다.

* Xms 옵션은 `-Xms<size>` 형식으로 사용되며, 여기서 `<size>`는 바이트 단위의 크기를 나타낸다.

* 예를 들어, `-Xms256m`의 의미는 최소 256MB의 힙을 할당하도록 지정한다.

## Xmx

* `Xmx`(Maximum Java Heap Size): JVM이 사용할 수 있는 **최대 힙 크기**를 지정한다.

* 애플리케이션의 메모리 요구 사항에 따라 힙 크기를 **동적**으로 조정하는 데 사용된다.

* Xmx 옵션은 `-Xmx<size>` 형식으로 사용되며, Xms와 마찬가지로 `<size>`는 바이트 단위의 크기를 나타낸다.

* 예를 들어, `-Xmx1024m`의 의미는 최소 1GB의 힙을 할당하도록 지정한다.

## 결론

