---
layout: post
title: "SPSS: Repeated Measure(within-subject) design ANOVA 분석"
---
<br>
Within-Subject 디자인은 비교적 적은 사람 수로 Independent variable의 significant effect를 효과적으로 확인할 수 있게 해준다. SPSS 프로그램으로 repeated measure (within-subject) ANOVA를 돌려보는 과정을 정리해보자.

<img src="/assets/RManova/SPSSoverview.PNG" width="600">
<p style='text-align:center'>IBM SPSS Statistics 25버전</p>

## 어떤 테스트?

SPSS로 들어가기 전에, 누군가 잘 정리해놓은 수형도를 보자. 가장 최근 내가 분석한 데이터는 
* Outcome variable 개수 = 1개 (Accuracy)
* Outcome variable type = Continuous
* Predictor variable 개수 = 1개(착용한 디바이스 종류)
* Predictor variable type = Categorical
* How many categories? = More than two (3개, 디바이스 종류)
* Same or different entities in each category? = Same <br>
(이 조건이 Same이면 within-subject, Different면 between-subject 디자인이다) 

마지막으로 정규성 검정을 통과한다면 One-way Repeated measures ANOVA를 하면 되고, 통과하지 못하면 Bootstrapped ANOVA 혹은 Friedman's ANOVA를 하면 된다.

<img src="/assets/RManova/toetskeuzeschema.PNG" width="900">
<p style='text-align:center'>Toetskeuzeschema Field</p>

지금부터 SPSS로 해볼 것은 다음과 같다:
* 데이터의 정규성 검정
* 그래프(+ Error Bar) 그리기
* 각 테스트 (One-way RM ANOVA / Friedman's ANOVA)
  * 구형성 체크
  * significant effect (p-value) 체크
  * post-hoc 분석
  


## 정규성(Normality) 검정

### 프로그램 사용

1. 분석 - 기술통계량 - 데이터 탐색 클릭
<img src="/assets/RManova/normality_spss_step1.PNG" width="600">
2. 검사하려는 변수를 종속변수에 추가한 후 '통계량' 클릭
<img src="/assets/RManova/normality_spss_step2.PNG" width="400">
3. 아래 옵션으로 설정 후 '계속' 클릭
<img src="/assets/RManova/normality_spss_step3.PNG" width="300">
4. 도표 클릭
<img src="/assets/RManova/normality_spss_step4.PNG" width="400">
5. 아래 옵션으로 설정 후 '계속' 클릭
<img src="/assets/RManova/normality_spss_step5.PNG" width="300">
6. '확인' 클릭
<img src="/assets/RManova/normality_spss_step6.PNG" width="400">

### 결과 분석
* 정규성 검정 표 확인
  * Shapiro-Wilk Test의 유의확률(p-value)이 0.05보다 크면 정규성 성립
<img src="/assets/RManova/normality_test_result.PNG" width="500">


## 그래프 그리기 (with Error Bar)

통계 분석에 들어가기 전에 데이터가 전체적으로 어떻게 생겼는지 Bar Chart를 그려서 확인해보자. 에러바도 있다면 statistical difference를 대충 예상할 수도 있겠다.

### 프로그램 사용

ANOVA를 돌릴 때처럼 각 Column에 컨디션에 따른 관측값을 분리해서 넣어놓으면 안되고, 한 Column에 전부 몰아 넣고 Independent variable의 Column을 하나 따로 만들어줘야 한다. (그냥 그대로 할 수 있는 방법이 있을지도.. )

1. 분석 - 기술통계량 - 데이터 탐색 클릭
<img src="/assets/RManova/normality_spss_step1.PNG" width="700">
2. 검사하려는 변수를 종속변수에 추가한 후 '통계량' 클릭
<img src="/assets/RManova/normality_spss_step2.PNG" width="500">
3. 아래 옵션으로 설정 후 '계속' 클릭
<img src="/assets/RManova/normality_spss_step3.PNG" width="500">
4. 도표 클릭
<img src="/assets/RManova/normality_spss_step4.PNG" width="500">
5. 아래 옵션으로 설정 후 '계속' 클릭
<img src="/assets/RManova/normality_spss_step5.PNG" width="500">
6. '확인' 클릭
<img src="/assets/RManova/normality_spss_step6.PNG" width="500">

### 결과 분석
* 정규성 검정 표 확인
  * Shapiro-Wilk Test의 유의확률(p-value)이 0.05보다 크면 정규성 성립
<img src="/assets/RManova/normality_test_result.PNG" width="700">


<br>
## 변경 이력
* 2020년 2월 3일: 글 등록
