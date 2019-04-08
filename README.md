# MachineLearning_Guide
파이썬 머신러닝 완벽가이드 정리

처음부터 차근차근 다시 정리하자!!


# 1 파이썬 기반의 머신러닝과 생태계 이해 [Link](https://github.com/miniii222/MachineLearning_Guide/tree/master/Ch1_Understanding)
### numpy
- ndarray는 같은 타입의 값들만!

### pandas
- inplace=True의 return값은 None! -> inplace=True 후 새로우 변수에 할당되는 값은 None
- axis = 0 : row / axis = 1 : columns
- numpy [] 와 pandas dataframe []는 다름
- loc[] : 명칭 기반 인덱싱만 가능. 
- iloc[] : 위치 기반 인덱싱만 가능.
- 명칭 기반 인덱싱에서 슬라이싱을 하면 종료점을 포함한 위치까지 반환
- groupby후 agg할 때, 딕셔너리타입으로 칼럼별 다른 함수 지정 가능

# 2 사이킷런으로 시작하는 머신러닝 [Link](https://github.com/miniii222/MachineLearning_Guide/tree/master/Ch2_Scikit-learn)

### cv
- GridSearchCV의 최적 성능을 나타내는 하이퍼파라미터로 학습해서 best_estimator_로 저장
### encoding
- sklearn 은 문자열 값을 입력 값으로 허용하지 않음
- label encoding : 문자열들을 숫자로 바꾸는 인코딩. 숫자의 크기가 의미 없지만, 의미를 부여하는 모델에서는 조심. 트리모델은 상관없음
- one-hot : 문자열들을 label encoding으로 숫자로 바꾼 후, 다시 one-hot\
- get_dummies : 문자열들도 바로 변환 가능
### Feature Scaling
- feature scaling : 서로 다른 변수의 값 범위를 일정한 수준으로 맞추는 작업
- Standardization(표준화) , Normalization(정규화), vector Normaliztion(벡터 정규화)

# 3 평가 [Link](https://github.com/miniii222/MachineLearning_Guide/tree/master/Ch3_Evaluation)
- Binarizer()를 이용하면, 특정값보다 큰 값을 1로, 작거나 같은 값을 0으로 만들 수 있다.
- scikitlearn의 분류모델 및 예측 메커니즘은 특정 class에 속할 확률을 구한 후, 높은 곳으로 분류한다. threshold를 조정하면, 특정 class에 속할 확률이 threshold보다 커지면, 분류하는 방식.
- predict_proba() -> Binarizer() -> 분류
- recall : negative로 잘못 판단하면 큰일이 나는, 암 예측과 같은 곳에서 중요하게 쓰임
- f1 score : recall과 precision 어느 쪽도 특별하게 치우치지 않을 때, 커진다.

# 4 분류 [Link](https://github.com/miniii222/MachineLearning_Guide/tree/master/Ch4_Classification)
- Naive bayes : Bayes 통계와 생성모델에 기반
- Logistic Regression : 독립변수와 종속변수의 선형 관계성에 기반
- Decision Tree : 데이터 균일도에 따른 규칙 기반
- SVM : 개별 클래스 간의 최대 분류 마진을 효과적으로 찾아줌
- Nearest Neighbor : 근접 거리를 기준으로
- Neural Network
- Ensemble
- Bagging : RandomForest
- Boosting : XGBoost, LightGBM


# 5 회귀[Link](https://github.com/miniii222/MachineLearning_Guide/tree/master/Ch5_Regression)
- 회귀모델은 항상 다중공선성 주의! variance-bias trade-off

# 6 차원 축소

# 7 군집화

# 8 텍스트 분석

# 9 추천 [Link](https://github.com/miniii222/BOAZ_adv_project/blob/master/study/PYTHON_ML_GUIDE%20-%20RS.md)
- 따로 정리
