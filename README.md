**2021년 BigContest 수산Biz 공모전 (평가지표 : RMSE)**

**0. Raw Data** : 2015~2019년 수산 품목별 데이터

**1. EDA 및 Feature Engineering**
  1) 이상치 확인 ==> 제거 근거 미약
  2) Meta Data의 Label Encoding ==> Prophet 모델로 미래 Meta Data 예측 ==> 회귀모델 Meta-Data로 활용
  3) 차분 ==> ARIMA 모델 활용

**2. 가격선정 방법**
  1) 구축모델 : 
    a. 회귀모델 : LGBM, Random Forest, SVM
    b. 시계열모델 : ARIMA
  2) 구축된 모델을 통해 2020~2021년 P_PRICE를 예측
     ==> 2020년 예측된 P_PRICE와 주최사에서 제공한 '자율평가데이터'와 비교하여 가장 유사한 값을 보인 모델을 주차별로 선정
     ==> 2020년에서 가장 낮은 RMSE를 보인 주차별 모델을 2021년에도 동일하게 적용하여 P_PRICE 선정
     
**3. 아쉬운점**
  1) 첫 공모전이였기에 각 모델에 대해 파악 및 구축소요시간이 필요 이상 소요
  2) 소비자물가지수 등 추가 데이터를 준비해놓고 시간에 좇겨 추가하지 못함
  3) EDA 및 Feature Engineering 부분 미흡
  4) 모델구축 완벽성 미흡
  5) 2021년 RMSE 검증 시간부족으로 인해 미흡

[BigContest 결과보고서.pdf](https://github.com/moohan132435/BigContest2021/files/7221878/BigContest.pdf)
