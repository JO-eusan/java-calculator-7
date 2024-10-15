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
    * 사용자가 잘못된 값을 입력하는 경우 예외 처리 (IllegalArgumentException)
2. 덧셈 계산 기능
    * 구분자 찾기: 입력 문자열의 첫 문자를 기준으로 기본/커스텀 구분자 분류
    * 기본 구분자 덧셈 계산
    * 커스텀 구분자 덧셈 계산
3. 결과값 출력
    * "결과 : {num}" 양식에 맞춰 출력


