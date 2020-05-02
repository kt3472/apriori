## 개인투자자의 ETF 매수 종목 연관분석(Association Analysis) 

**1) Summary**
- 연관분석은 하나의 거래나 사건에 포함된 항목간의 관련성을 파악하여 둘 이상의 항목들로 구성된 연관성 규칙을 도출하는 분석방법. 개인투자자의 ETF 순매수 데이터를 기반으로 거래의 규칙이나 패턴 도출을 목표

**2) Association rule concepts**
- 비지도 학습에 의한 패턴분석 방법이다.
- 거래사실이 기록된 트랜잭션(Transaction)형식의 데이터 셋을 이용한다.
- 사건과 사건 간의 연관성을 찾는 방법(예:맥주와 만두)
- 지지도(제품 동시 구매패턴), 신뢰도(A제품 구매 시 B 제품 구매패턴), 향상도(A제품과 B제품간의 상관성)를 연관규칙의 평가도구로 사용한다

**3) Modeling Process**
-  python aprior 라이브러리 사용
- 1단계 : 개인투자자의 ETF 순매수 정보 데이터를 대상으로 트랜잭션 객체 생성
- 2단계 : 평가 척도(지지도, 신뢰도, 향상도) 산출 및 분석, 연관 규칙(Rule) 탐색
- 3단계 : 연관분석 해석 및 결론

**4) Results**

- 향상도(lift)가 가장높은 거래는 KODEX레버리지 -> TIGER레버리지 거래
- 지지도, 향상도, 신뢰도가 고루 높은 거래는 KODEX 200 -> KODEX레버리지 거래

  ![data](./data/aa_result_table.jpg)


<br>


**( appendix )**

- 지지도(support) = A상품과 B상품이 동시에 포함한 거래수 / 전체 거래수
- 신뢰도(confidence) = 지지도 / A상품을 포함한 거래수
- 향상도(Lift) = 신뢰도 / B상품을 포함한 거래율

