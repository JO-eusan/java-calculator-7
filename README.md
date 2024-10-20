# [WEEK1] 문자열 덧셈 계산기

### 목표: 구분자를 기준으로 분리된 숫자의 총합을 반환하는 덧셋 계산기 구현

---
구분자는 2가지 종류가 존재하므로 각각의 경우를 나누어 예외처리가 필요하다.

* 기본 구분자: 쉼표(,)와 콜론(:)
* 커스텀 구분자: "//"와 "\n" 사이에 있는 문자

### 구현 기능 목록

---

1. 입력 처리
    * camp.nextstep.edu.missionutils.Console의 readLine()을 활용하여 문자열 입력 받기
    * 사용자을 기준으로 기본/커스텀 구분자 분류
    * 사용자가 잘못된 값을 입력하는 경우 예외 처리 (IllegalArgumentException)
2. 덧셈 계산 기능
    * 기본 구분자 덧셈 계산
    * 커스텀 구분자 덧셈 계산
3. 결과값 출력
    * "결과 : {num}" 양식에 맞춰 출력

### 기능 설명

---

* 입력 처리: `InputInfo.validateFormat()`
    * 기본 구분자의 경우, 계산 문자열은 입력값 자체이다.
    * 커스텀 구분자의 경우, 계산 문자열은 index 5 이후의 문자열이다.
* 계산 문자열 검증: `InputInfo.validateNumbers()`
    * 실제 계산 문자열이 비어있는 경우는 0을 반환
    * 구분자로 끝나는 경우, 예외를 발생
    * 정해진 구분자와 숫자 이외의 값이 입력값에 포함된 경우, 예외를 발생
    * 숫자는 양의 정수만 허용되므로 음수가 입력된 경우, 예외를 발생
    * 이외에 구분자가 연속해서 나오는 경우 등을 처리하기 위한 예욀르 발생
* 숫자 분리 및 계산 로직: `AddCalculator`
    * `separate()`: `InputInfo` 클래스에서 처리한 구분자와 포맷을 기반으로 계산할 숫자를 리스트에 저장한다.
    * `calculate()`: 리스트에 저장되어 있는 숫자들을 모두 더한다.
