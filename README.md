# Gallstone Prediction ML Model (담석증 진단 예측 모델)

## Project Overview
본 프로젝트는 '고급데이터분석' 수업의 일환으로, 임상 데이터를 활용하여 담석증 유무를 예측하는 머신러닝 모델을 개발한 프로젝트입니다.
- Goal: 정확도와 재현율(Recall)을 모두 고려한 고성능 분류 모델 개발 및 의학적 해석(XAI)
- Key Performance: AUC 0.79, Recall 0.79 달성
- Tech Stack: Python, Scikit-learn, PyCaret, SHAP

## Code Description (실행 순서)
이 프로젝트는 데이터 전처리부터 모델 해석까지 논리적인 순서로 구성되어 있습니다.

1. 01_Data_Preprocessing_EDA.ipynb: 결측치(MICE) 처리 및 이상치 탐지 등 데이터 전처리
2. 02_Feature_Engineering_SBS.ipynb: 상관관계 분석 및 SBS 기법을 통한 22개 핵심 바이오마커 선정
3. 03_Model_Comparison_PyCaret.ipynb: 다양한 모델(LR, SVM, RF 등) 비교 분석
4. 04_Hyperparameter_Tuning.ipynb: Grid Search를 이용한 최적의 파라미터 탐색
5. 05_Regularization_Experiment.ipynb: L2 규제 강도에 따른 과적합 방지 효과 검증
6. 06_Final_Model_Pipeline.ipynb: 최종 선정된 로지스틱 회귀 모델 파이프라인 구축 및 평가
7. 07_Model_Interpretation_SHAP.ipynb: SHAP을 활용한 변수 중요도 시각화 및 의학적 타당성 검증

## Conclusion
- 다양한 모델을 비교해본 결과, L2 규제(C=1)를 적용한 로지스틱 회귀 모델이 일반화 성능 면에서 가장 우수했습니다.
- SHAP 분석을 통해 모델이 담낭 운동성 관련 지표를 중요하게 판단함을 확인하였으며, 이는 실제 의학적 소견과 일치합니다.