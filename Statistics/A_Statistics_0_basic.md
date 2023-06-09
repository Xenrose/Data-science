# 쉽게 배우는 통계 입문
[메타코드M 유튜브](https://youtu.be/YaCQrJCgbqg)
____

## 통계란?
* 통계: 데이터의 수집, 분석, 추론, 요약 등의 방법론
  * Design(설계/계획)
  * Description(요약): 데이터를 요약 표현하기 위한 시각적(Graphical)/수치적(Numerical) 방법
  * Inference(추론): 표본에 기반한 모집단에 대한 추론/예측

___
## 기본 통계 용어
* 모집단(Poplulation): 통계학에서 관심/조사의 대상이 되는 개체의 전체 집합
* 모수(Parameter): 모집단에 대한 수치적 요약
* 표본(Sample): 모집단을 적절히 대표하는 모집단의 일부
* 통계량(Statistic): 표본에 대한 수치적 요약

<br>

### 자료의 종류
1. 범주형 자료: 속성의 범주화, 상대적 서열
   1. 명목형 자료: 단순히 속성을 분류하기 위함 ex) 혈액형
   2. 순서형 자료: 상대적인 크기 비교 ex) 만족도, 최종학력
2. 양적 자료: 자료자체가 숫자로 표현 가능
   1. 이산형 자료: 셀 수 있음 ex) 빈도수, 불량품의 수
   2. 연속형 자료: 셀 수 없음 ex) 길이, 시간
___
## 통계량 (최빈값, 중앙값, 산술평균, 가중평균, 기하평균)

* 최빈값(mode)
  * 발생빈도가 가장 높은 값
  * 극단값에 영향을 받지 않음
  * 주로 범주형 자료에 대한 대표값
  * 2개 이상 존재 가능  

<br>

 * 중앙값(median)
   * 크기 순으로 정렬된 자료에서 가운데에 위치하는 값
   * 관측값 변화에 민감하지 않음
   * 극단값에 영향을 받지 않음

<br>

* 산술평균(Arithmetic Mean)
  * 모든 자료의 값을 더하여 자료의 수로 나누어 준 값
  * 모든 값을 반영하므로 극단값에 영향을 받음

<br>

* 가중평균(Weighted Mean)
  * 자료의 중요성이 각기 다를 경우 중요도에 따라 가중치를 부여한 평균

<br>

* 기하평균(Geometric Mean)
  * 자료가 성장률, 증가율 등 앞 시점에 대한 *비율*로 나타난 경우 유용한 통계량
  * 음수가 아닌 자료값 only
  * 연간 물가 상승률
___

## 통계량 - 산포

* 분산(Variance): 편차 제곱의 합을 자료의 수로 나눈 값
  * 제곱을 하는 이유: 관측값에 평균을 뺀 모든 수를 합치면 0이 되므로 제곱을 함으로써 편차의 합이 0이 되는것을 방지함.
* 표준편차(Standard Deviation): 분산을 제곱근한 값
  * 제곱근을 하는 이유: 만약 분산에서 편차를 제곱했을 경우 가령 단위가 cm이라면 분산의 단위는 cm^2가 된다. 여기서 제곱근을 할 경우 cm^2가 cm으로 다운스케일링 되면서 원래의 단위를 찾게된다.

<br>

## 통계량 - 형태

* 왜도(Skewness): 분포의 비대칭
  * Postive Skew: Mode < Median < Mean  // 극단값이 오른쪽에 있다.
  * Symmetrical Distribution: Mode = Median = Mean
  * Negative Skew: Mean < Median < Mode // 극단값이 왼쪽에 있다.

<br>

* 첨도(Kurtosis): 뵤족한 정도 / 표준정규분포의 첨도는 **3**이 된다.

<br>

## 통계량 - 상관

* 상관(Correlation): 확률변수 X, Y의 변화가 서로 관계가 있을 때 상관관계가 있다고 함. / 선형적 관련성을 파악함

* 공분산(Covariance): $\sum_{i=1}^{n} (x_i-\bar{x})*(y_i-\bar{y}) \over n-1$

* 상관계수(Correlation Coefficient): $\sum_{i=1}^{n} (x_i-\bar{x})*(y_i-\bar{y}) \over [\sum_{i=1}^{n} (x_i-\bar{x})^2 * \sum_{i=1}^{n} (y_i-\bar{y})^2]^{1 \over 2}$
  * 피어슨 상관계수
  * 공분산을 두 변수(x,y)의 표준편차의 곱으로 나눈 값
  * -1 $\leq$ 상관계수 $\leq$ 1
  * 두 양적 변수 간의 **선형적 연관성의 강도** 측정. 
    * 즉, 비선형관계에서는 계수가 0일 수 있음.
  * 단위가 없음. 
    * 즉, 단위가 없기에 다른 단위끼리 계수를 측정해도 문제가 없음.
  * 절대값이 1에 가까울 수록 연관성의 강도가 높음