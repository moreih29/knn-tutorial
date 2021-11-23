# KNN tutorial

## 개요
k-Nearest Neighbor(k-NN)알고리즘은 데이터를 입력 받았을 때, 해당 데이터와 근접한 다른 k개의 데이터를 보고 해당 데이터의 class를 판단하는 알고리즘

## 동작 과정
![knn 결정 과정](https://upload.wikimedia.org/wikipedia/commons/thumb/e/e7/KnnClassification.svg/330px-KnnClassification.svg.png)

- k=3 일 때, 타겟 데이터(초록색 원형)과 근접한 검은 실선 안에는 빨간 세모 데이터 두 개와 파란 네모 데이터 한 개가 존재
- 이 경우, 빨간 세모 데이터가 두 개로 가장 많기 때문에 타겟 데이터는 빨간 세모로 분류
- k=5 일 때, 타겟 데이터와 근접한 검은 점선 안에는 빨간 세모 데이터 2개와 파란 세모 데이터 3개가 존재
- 이 경우, 파란 네모 데이터가 세 개로 가장 많기 때문에 타겟 데이터는 파란 네모로 분류

## 고려할 점
### k값 선택
- 분류 기준이 되는 k값을 선택하는 것이 가장 중요
- 가장 적절한 k는 데이터 별로 다름
- k를 짝수로 할 경우, 근접한 k개의 데이터 안에서 다수 클래스가 2개 이상 나올 가능성(빨간 세모 2개, 파란 네모 2개가 될 경우)이 높기 때문에 주로 홀수로 함

### 특징 추출 및 차원 축소
- k-NN은 기본적으로 타겟 데이터와의 거리를 기준으로 근접한 데이터를 선택
- 그러나 10차원이 넘는 고차원 데이터의 경우, 모든 벡터가 타겟 데이터와 비슷한 유클리드 거리를 갖을 가능성이 있음 (많은 점들이 대부분 타겟 데이터를 중심으로 하는 원 위에 있다면, 검색 공간에서 타겟 데이터와 모든 데이터 사이의 거리는 비슷함)
- 이를 해결하기 위해 데이터의 특징 중에서 분류에 주요한 특징만 추출하는 주성분 분석(PCA), 선형 판별 분석(LDA)를 사용하여 차원을 축소함

---
출처
- https://ko.wikipedia.org/wiki/K-%EC%B5%9C%EA%B7%BC%EC%A0%91_%EC%9D%B4%EC%9B%83_%EC%95%8C%EA%B3%A0%EB%A6%AC%EC%A6%98
- https://hleecaster.com/ml-knn-classifier-example/