# Kaggle_PSPGP
Kaggle 대회 'Predict Student Performance from Game Play'에 참여해 사용한 코드입니다.

--대회 홈페이지--<br>
https://www.kaggle.com/competitions/predict-student-performance-from-game-play

### 1. 파일 소개

(1) __(AF)FeatureEngineering_v0.1.ipynb__ : FeatureEngineering 진행한 스크립트

(2) __(AF)Modeling_LGBM_v0.1.ipynb__ : (1)에서 만든 학습용 데이터셋을 가지고 모델을 구축한 스크립트입니다.

(3) __(AF)Inference_LGBM_v0.1.ipynb__ : (2)에서 구축한 모델을 가지고 테스트 데이터를 예측해 대회에 제출하는 코드입니다. 캐글 노트북에서 실행하여야 합니다.  

(4) __data 폴더 내 파일들__

  - (AF)feature_true.pickle : 대회 토론 게시판에서 공유된 features 리스트
  - (AF)trainset.pickle : feature engineering을 거친 학습용 데이터셋
  - (AF)LGBM_v0.1.pickle : 구축된 모델 데이터

### 2. 모델 개요

- LightGBM 모델 사용
- 1300 ~ 2300여개 features 활용
- 5 fold Stratified KFold로 학습
- 분류 결정경계 0.614 사용
- 모델 평가 : Macro F1-Score
- 모델 점수 : CV 0.705 / LB public 0.699, LB private 0.701 
