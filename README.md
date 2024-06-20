# 영화 관객 수 예측을 위한 새로운 변수 개발

### 김형민 김기훈
<img src="https://www.khu.ac.kr/upload/cross/images/000004/imgSub11500_02.jpg" style="width:300px">

## 프로젝트 개요
본 연구는 머신러닝기초및응용 2024 기말 프로젝트로, 차주 영화 관객 수 예측을 위한 새로운 변수를 개발하고 이를 모델링에 적용하여 예측 성능을 평가하는 것을 목표로 합니다. 네이버 트렌드 데이터를 포함한 다양한 변수들을 사용하여 예측 모델의 성능을 향상시키고자 하였습니다.

## 데이터
- **수집 방법**: 2022년 이후로 축적된 영화 데이터를 사용하였습니다.
- **전처리 과정**: 데이터의 이상치 및 결측치를 처리하고, 주차별 누적 관객수 데이터를 정리하였습니다.

## 변수 선택
- 변수의 중요도를 평가하여 예측 모델에 사용될 주요 변수를 선정하였습니다.
- 네이버 트렌드 데이터를 포함한 다양한 변수를 분석하였습니다.

## 모델 구축
본 연구에서는 다양한 회귀 모델을 사용하여 예측 성능을 비교하였습니다:
- KNeighbors Regressor
- RandomForest Regressor
- XGBoost
- Ridge
- Lasso

### 하이퍼파라미터 튜닝
- 10-Fold 교차 검증을 통해 모델의 하이퍼파라미터를 최적화하였습니다.

## 모델 평가
모델의 성능을 평가하기 위해 다음과 같은 지표를 사용하였습니다:
- RMSE (Root Mean Square Error)
- MAPE (Mean Absolute Percentage Error)
- R² (R-squared)

### 평가 결과
- 선형 회귀 모델인 Ridge와 Lasso가 비선형 모델들(KNeighbors Regressor, RandomForest Regressor, XGBoost)보다 높은 성능을 보였습니다.
- 이는 주차별 누적 관객수 데이터가 종속 변수와 강한 선형 관계를 가지기 때문입니다.

## 네이버 트렌드 피처 평가
- 네이버 트렌드 데이터는 모델의 중요한 피처로 작용하였으며, MAPE 지표를 개선하는 데 기여하였습니다.
- 그러나 피처 증가로 인한 모델의 복잡도가 높아져 RMSE 지표는 증가하였습니다.

## 결론 및 제언
- 선형 회귀 모델이 차주 영화 관객 수 예측에 더 적합함을 확인하였습니다.
- 본 연구의 한계로는 데이터의 불균형 문제와 피처 증가로 인한 모델 복잡도 증가가 있습니다.
- 향후 연구에서는 영화 제작 이전 단계에서 첫 주차 관객 수 또는 영화 흥행 여부를 예측할 수 있는 모델의 개발이 필요합니다.


