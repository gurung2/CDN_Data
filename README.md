<!-- more -->
Step 08. IDE Edit Plug-in (IntelliJ)
<!-- more -->

<!-- excerpt -->
<!-- excerpt -->

지금까지의 Tutorial을 통해 Mocha에 대해서 어느 정도 인지하고 습득하였다. 아직도 Mocha에 대해 애매모호한 기분이 들거나 뭔가 아쉬움이 남는다면 다시 돌아가 [JavaScript 단위 테스트 프레임워크 - Mocha](https://kdydesign.github.io/2017/06/08/Mocha/)부터 살펴보도록하자.
이제 지금까지 배운 내용을 토대로 실제로 Mocha를 가지고 TDD를 진행해 보자. 이 Tutorial을 추가한 이유는 두 가지로 분류하였다.

> 1. TDD를 이해하기 위함이며,
> 2. Mocha를 실전에 사용해 보기 위함이다.

이 두 가지를 생각하며 Tutorial을 시작해보자.

## TDD(Test-Driven-Development) Cycle

TDD는 [Step 03: Hooks](https://kdydesign.github.io/2017/06/16/Mocha-step-03/)에서 살짝 설명한 바가 있다. TDD는 짧은 Cycle을 반복적으로 테스트하는 개발 프로세스로 테스트 코드를 먼저 작성하고 작성된 테스트 코드를 패스할 수 있도록 비즈니스 로직을 개발하는 방법이다. 자세한 TDD가 무엇인지는 구글링을 통해 알아보자. 

시작하기 앞서 TDD의 프로세스를 생각해두자. 위에서 말했듯이 하나의 짧은 Cycle을 반복저으로 수행하는 것인다. 이 Cycle의 대략적인 순서는 이렇다.

{% alert info %}
1. 개발**명세작성**
2. 개발 명세에 따른 **테스트 코드 작성**
3. 테스트 실행
4. 테스트가 성공하도록 최소한의 비스니스 로직 작성
5. 테스트 실행
6. 테스트 케이스 추가
7. 테스트 실행
8. 테스트 코드 및 테스트 케이스 Refactring
9. 테스트 실행
{% endalert %}
