# java-racingcar
자동차 경주 게임 미션 저장소

## 문자열 계산기
### 기능 요구사항
- 사용자가 입력한 문자열 값에 따라 사칙연산을 수행할 수 있는 계산기를 구현해야 한다.
- 문자열 계산기는 사칙연산의 계산 우선순위가 아닌 입력 값에 따라 계산 순서가 결정된다. 즉, 수학에서는 곱셈, 나눗셈이 덧셈, 뺄셈 보다 먼저 계산해야 하지만 이를 무시한다.
- 예를 들어, "2 + 3 * 4 / 2"와 같은 문자열을 입력할 경우 2 + 3 * 4 / 2 실행 결과인 10을 출력해야 한다.

### 기능 목록 정의
1. [입력] 사용자로부터 계산식을 입력받는다.
  - [예외처리] 숫자, 연산자(+,-,*,/)가 아닌 경우. (예 : 알파벳 등 문자인 경우, 공백이 2개 이상인 경우.)
  - [예외처리] 길이가 3미만인 경우.
  - [예외처리] 0으로 나누는 경우.
  - [예외처리] 순서가 잘못된 경우. (예 : 1 + + , 2 2 / 등.)
2. [계산] 입력받은 계산식의 결과를 반환한다.
3. [테스트]  2번 기능에 대한 테스트 코드를 작성한다.
4. [예외] 1번 기능에 대한 예외 처리를 구현한다.
5. [테스트] 4번 기능에 대한 테스트 코드를 작성한다.
6. [리팩토링]


## 자동차 경주 게임
### 기능 요구사항
- 주어진 횟수 동안 **n대의 자동차는 전진 또는 멈출 수 있다.**
- 각 자동차에 **이름을 부여** 할 수 있다. 전진하는 자동차를 출력할 때 자동차 이름을 같이 출력한다.
- 자동차 이름은 쉼표(,)를 기준으로 구분하며 **이름은 5자 이하만** 가능하다.
- 사용자는 **몇 번의 이동을 할 것인지를 입력** 할 수 있어야 한다.
- 전진하는 조건은 0에서 9 사이에서 random 값을 구한 후 **random 값이 4 이상일 경우 전진** 하고, **3 이하의 값이면 멈춘다.**
- 자동차 경주 게임을 완료한 후 **누가 우승했는지를 알려준다.** 우승자는 한 명 이상일 수 있다.

### 기능 목록 정의
1. 사용자에게 자동차 이름을 입력받는다.
  - [예외처리]  자동차 이름이 6글자 이상인 경우.
  - [예외처리]  잘못된 입력인 경우.(예 : 연속된 쉼표일 경우, 공백, 빈문자열인경우)
  - [예외처리] 알바펫이 아닐 경우.
2. 사용자에게 시도할 회수를 입력받는다.
  - [예외처리] 자연수가 아닐 경우. (예 : 공백, 문자, -1, 0 등.)
3. 사용자가 입력한 이름의 수만큼 자동차 객체를 생성한다.
4. 0-9까지의 랜덤 값을 구한다.
5. 랜덤값에 따라 자동차를 전진하거나 정지한다.
6. 회수마다 실행결과를 출력한다.
7. 가장 멀리 이동한 자동차를 구한다.
8. 최종 우승자를 출력한다.