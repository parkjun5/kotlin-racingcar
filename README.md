# kotlin-racingcar

### 4단계 요구사항
- 각 자동차에 이름을 부여할 수 있다. 자동차 이름은 5자를 초과할 수 없다.
- 전진하는 자동차를 출력할 때 자동차 이름을 같이 출력한다.
- 자동차 이름은 쉼표(,)를 기준으로 구분한다.
- 자동차 경주 게임을 완료한 후 누가 우승했는지를 알려준다. 우승자는 한 명 이상일 수 있다.

### 5단계 요구사항
- 핵심 비지니스 로직을 가지는 객체를 domain 패키지, UI 관련한 객체를 view 패키지에 구현한다.
- MVC 패턴 기반으로 리팩토링해 view 패키지의 객체가 domain 패키지 객체에 의존할 수 있지만, domain 패키지의 객체는 view 패키지 객체에 의존하지 않도록 구현한다.


작동 프로세스

1. 컨트롤러에서 요청을 받음
2. InputView에서 사용자에게 차 이름들과 트랙 횟수를 받음
3. 사용자 입력 정보를 바탕으로 Car 객체 리스트를 Race 도메인에 전달
4. 트랙 횟수만큼 차를 반복시킴
5. 결과물을 Response로 변환 전달
6. Race도메인에 저장된 List를 통해 우승자 정보를 전달한다.