# KNN tutorial

## 개요
k-Nearest Neighbor(k-NN)알고리즘은 데이터를 입력 받았을 때, 해당 데이터와 근접한 다른 k개의 데이터를 보고 해당 데이터의 class를 판단하는 알고리즘

## 동작 과정
![knn 결정 과정](https://upload.wikimedia.org/wikipedia/commons/thumb/e/e7/KnnClassification.svg/330px-KnnClassification.svg.png)

- k=3 일 때, 타겟 데이터(초록색 원형)과 근접한 검은 실선 안에는 빨간 세모 데이터 두 개와 파란 네모 데이터 한 개가 존재
- 이 경우, 빨간 세모 데이터가 두 개로 가장 많기 때문에 타겟 데이터는 빨간 세모로 분류
- k=5 일 때, 타겟 데이터와 근접한 검은 점선 안에는 빨간 세모 데이터 2개와 파란 세모 데이터 3개가 존재
- 이 경우, 파란 네모 데이터가 세 개로 가장 많기 때문에 타겟 데이터는 파란 네모로 분류

---
출처
- https://ko.wikipedia.org/wiki/K-%EC%B5%9C%EA%B7%BC%EC%A0%91_%EC%9D%B4%EC%9B%83_%EC%95%8C%EA%B3%A0%EB%A6%AC%EC%A6%98
- https://hleecaster.com/ml-knn-classifier-example/