---
layout: post
title: "SPSS: Repeated Measure(within-subject) design ANOVA 분석"
---
<br>
Within-Subject 디자인은 비교적 적은 사람 수로 Independent variable의 significant effect를 효과적으로 확인할 수 있게 해준다. SPSS 프로그램으로 Repeated measure (within-subject) ANOVA를 돌려보는 과정을 정리해보자.

<img src="/assets/RManova/SPSSoverview.PNG" width="600">
<p style='text-align:center'>IBM SPSS Statistics 25버전</p>

## 어떤 테스트?

SPSS로 들어가기 전에, 누군가 잘 정리해놓은 수형도를 보자. 가장 최근 내가 분석한 데이터는 
* Outcome variable 개수 = 1개 (Accuracy)
* Outcome variable type = Continuous
* Predictor variable 개수 = 1개(착용한 디바이스 종류)
* Predictor variable type = Categorical
* How many categories? = More than two (3개, 디바이스 종류)
* Same or different entities in each category? = Same 
(마지막이 조건이 Same이면 within-subject, Different면 between-subject 디자인이다) 
마지막으로 정규성 검정을 통과한다면 One-way Repeated measures ANOVA를 하면 되고, 통과하지 못하면 Bootstrapped ANOVA 혹은 Friedman's ANOVA를 하면 된다.

<img src="/assets/RManova/toetskeuzeschema.PNG" width="900">
<p style='text-align:center'>Toetskeuzeschema Field</p>

지금부터 SPSS로 해볼 것은 다음과 같다:
* 데이터의 정규성 검정
* 각 테스트 (One-way RM ANOVA / Friedman's ANOVA)
  * 구형성 체크
  * Significant effect (p-value) 체크
  * post-hoc 분석
* 그래프 (with error bar) 그리기


## 채

### 우자

<br>
## 변경 이력
* 2020년 2월 3일: 글 등록
