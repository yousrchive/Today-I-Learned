#

| 모듈 이름             | 설명                                                                                                                                               |
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| `sklearn.datasets`   | 데이터셋 로드 및 샘플 데이터셋 생성 기능을 제공합니다.                                                                                                    |
| `sklearn.model_selection` | 교차 검증 도구 및 데이터셋 분할 기능을 제공합니다.                                                                                                      |
| `sklearn.preprocessing`   | 데이터 전처리 및 특성 스케일링 도구를 제공합니다.                                                                                                     |
| `sklearn.feature_selection` | 특성 선택 및 차원 축소 도구를 제공합니다.                                                                                                          |
| `sklearn.feature_extraction` | 특성 추출 도구를 제공합니다.                                                                                                                 |
| `sklearn.decomposition`   | 차원 축소를 위한 행렬 분해 알고리즘을 제공합니다.                                                                                                  |
| `sklearn.manifold`        | 비선형 차원 축소 알고리즘을 제공합니다.                                                                                                           |
| `sklearn.linear_model`    | 선형 회귀 및 분류 모델을 제공합니다.                                                                                                             |
| `sklearn.svm`             | 서포트 벡터 머신 알고리즘을 제공합니다.                                                                                                           |
| `sklearn.tree`            | 의사결정 나무 알고리즘을 제공합니다.                                                                                                             |
| `sklearn.ensemble`        | 앙상블 학습 방법을 제공합니다 (예: 랜덤 포레스트, 그래디언트 부스팅).                                                                                     |
| `sklearn.cluster`         | 클러스터링 알고리즘을 제공합니다 (예: K-평균, DBSCAN).                                                                                                 |
| `sklearn.mixture`         | 혼합 모델 알고리즘을 제공합니다 (예: 가우시안 혼합 모델).                                                                                               |
| `sklearn.neighbors`       | 최근접 이웃 알고리즘을 제공합니다.                                                                                                               |
| `sklearn.naive_bayes`     | 나이브 베이즈 분류 알고리즘을 제공합니다.                                                                                                         |
| `sklearn.neural_network`  | 인공 신경망 알고리즘을 제공합니다.                                                                                                              |
| `sklearn.gaussian_process` | 가우시안 프로세스 기반의 회귀 및 분류 알고리즘을 제공합니다.                                                                                           |
| `sklearn.semi_supervised` | 반지도 학습 알고리즘을 제공합니다.                                                                                                              |
| `sklearn.discriminant_analysis` | 선형 판별 분석 및 이차 판별 분석 알고리즘을 제공합니다.                                                                                            |
| `sklearn.metrics`         | 모델 평가를 위한 성능 지표를 제공합니다.                                                                                                          |
| `sklearn.pipeline`        | 파이프라인 도구를 제공합니다.                                                                                                                   |
| `sklearn.externals`       | 외부 라이브러리 및 유틸리티 도구를 포함합니다.                                                                                                     |

sklearn.preprocessing으로 인코딩, 정규화, 스케일링을 수행할 수 있음.
sklearn.feature_selection으로 알고리즘에 큰 영향을 미치는 피처를 우선순위대로 셀렉션 작업을 수행함
sklearn.feature_extraction으로 텍스트 데이터, 이미지 데이터의 벡터화된 피처를 추출할 수 있음
sklearn.decomposition은 차원 축소와 관련된 알고리즘을 지원함. PCA, NMF, Truncated SVD 수행 가능
model_selection 데이터 분리, 검증 및 파라미터 튜닝 가능. Grid Search로 최적 파라미터 추출 등의 API 제공
sklearn.metrics 분류, 회귀, 클러스터링, 페어와이즈 등에 대한 다양한 성능 측정 방법 제공(Accuracy, Precision, Recall, ROC-AUC, RMSE 등 제공)
sklearn.ensemble 랜덤포레스트, 에이다 부스트, 그래디언트 부스팅 등을 제공
linear_model 선형 회귀, 릿지, 라쏘 등 로지스틱 회귀 등 회귀 관련 알고리즘, SGD 관련 알고리즘 제공
pipeline ML 알고리즘 학습, 예측 등을 함께 묶어 실행 가능한 유틸리티 제공
sklearn.cluster 비지도 클러스터링 알고리즘 제공(K-means, 계층형, DBSCAN 등)
