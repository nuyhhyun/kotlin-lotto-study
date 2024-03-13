# 🎊 kotlin-lotto 🎉
> 로또를 구매한 후 발행된 번호들과 당첨 번호를 비교하여 당첨 통계를 받아 보는 게임이다.
---

## 🪄 기능 요구 사항
### 로또
- [X] 로또 구입 금액에 해당하는 로또 수량 및 로또를 발급해야 한다. 로또 1장의 가격은 1,000원이다.
  - [X] 로또 구입 금액은 거스름돈 없이 1,000원 단위로 받는다.
  - [X] 로또 구입 금액은 양의 정수이어야 한다.
  - [X] 로또는 한 장 이상 구매해야 한다.
  - [X] 발행한 로또들의 번호를 저장한다.
- [X] 사용자가 구매한 로또 번호와 당첨 번호, 보너스 번호를 비교하여 당첨 여부를 확인한다.
### 로또 티켓
- [X] 1개의 로또를 발행할 때 중복되지 않는 6개의 숫자를 무작위로 뽑는다.
  - [X] 로또 번호의 숫자 범위는 1~45까지이다.
  - [X] 로또 번호는 오름차순으로 정렬하여 보여준다.
### 당첨 번호
- [X] 당첨 번호 추첨 시 중복되지 않는 숫자 6개와 보너스 번호 1개를 뽑는다.
  - [X] 당첨 번호와 보너스 번호의 범위는 1~45까지이다.
### 순위
- [X] 일치하는 번호의 갯수에 따라 어느 유형으로 당첨됐거나 당첨되지 않았는지 알려준다.
  - 당첨 기준과 금액은 아래와 같다.
    - 3개 번호 일치 : 5,000원
    - 4개 번호 일치 : 50,000원
    - 5개 번호 일치 : 1,500,000원
    - 5개 번호 + 보너스 번호 일치 : 30,000,000원
    - 6개 번호 일치 : 2,000,000,000원
- [X] 당첨 유형마다 몇 개의 로또가 당첨됐는지 저장한다.
- [X] 총 수익을 구할 수 있다.
### 수익률
- [X] 구입 금액에 따른 수익률을 구할 수 있다. 수익률은 소수점 셋째 자리에서 반올림한다.

## 🖨️ 실행 예시
```
구입금액을 입력해 주세요.
14000

14개를 구매했습니다.
[8, 21, 23, 41, 42, 43]
[3, 5, 11, 16, 32, 38]
[7, 11, 16, 35, 36, 44]
[1, 8, 11, 31, 41, 42]
[13, 14, 16, 38, 42, 45]
[7, 11, 30, 40, 42, 43]
[2, 13, 22, 32, 38, 45]
[23, 25, 33, 36, 39, 41]
[1, 3, 5, 14, 22, 45]
[5, 9, 38, 41, 43, 44]
[2, 8, 9, 18, 19, 21]
[13, 14, 18, 21, 23, 35]
[17, 21, 29, 37, 42, 45]
[3, 8, 27, 30, 35, 44]

지난 주 당첨 번호를 입력해 주세요.
1, 2, 3, 4, 5, 6

보너스 볼을 입력해 주세요.
7

당첨 통계
---------
3개 일치 (5000원)- 1개
4개 일치 (50000원)- 0개
5개 일치 (1500000원)- 0개
5개 일치, 보너스 볼 일치(30000000원) - 0개
6개 일치 (2000000000원)- 0개
총 수익률은 0.35입니다.
```