---
layout: post
title: "SPSS: Repeated Measure(within-subject) design ANOVA 분석"
---
<br>
Within-Subject 디자인은 비교적 적은 사람 수로 Independent variable의 significant effect를 효과적으로 확인할 수 있게 해준다. 오늘은 SPSS 프로그램으로 Repeated measure (within-subject) ANOVA를 돌려보는 과정을 정리해 볼것이다.

<img src="/assets/RManova/SPSSoverview.PNG" width="600">
<p style='text-align:center'>IBM SPSS Statistics 25버전</p>

## 어떤 테스트?

SPSS로 들어가기 전에 우선 아래 누군가 잘 정리해놓은 수형도에 오늘 정리해볼 테스트를 표시해놓았다. 가장 최근 내가 분석한 Data는 outcome variable이 1개 (정확도)였고 outcome variable의 type은 continuous, predictor variable은 1개(착용한 디바이스 종류), predictor의 type은 categorical, 카테고리의 수는 More than two (디바이스 종류 3개), 각 카테고리에 참여한 entity는 Same이다. (마지막이 Same이면 within-subject, Different면 between-subject디자인이다) 이 상황에서 정규성 검정을 통과한다면 One-way Repeated measures ANOVA 테스트를 하면 되고, 통과하지 못하면 Bootstrapped ANOVA 혹은 Friedman's ANOVA 테스트를 하면 된다.

정규성 검정부터 각 테스트에서의 구형성 체크, ANOVA 결과에 따른 significant effect (p-value), post-hoc 분석, 그래프 그리기까지 정리해보려 한다. 
<img src="/assets/RManova/toetskeuzeschema.PNG" width="900">
<p style='text-align:center'>Toetskeuzeschema Field</p>



## 채

### 우자

<br>
## 변경 이력
* 2020년 2월 3일: 글 등록
