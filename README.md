
## Dacon 전력사용량 예측 AI 경진대회

- 대회 개요 (2023.07.17 ~ 2023.08.28) https://dacon.io/competitions/official/236127/overview/description
- 시계열 회귀 예측 (SMAPE)
- 건물 정보와 시공간 정보를 활용하여 특정 시점의 전력 사용량을 예측하는 AI 모델 개발 
- 성과 : private 5.7%이내 - 70등/1233팀

## Summary
- **Data Selection** : 건물별(총 100개 건물) 모델링 
- **Feature Engineering** : 기온 및 습도 파생 변수 (discomfort, CDH), 공휴일
- **Visualization** : 과거 및 예측 기온 시각화 반영하여 공휴일 확인 및 피쳐 조정
- **Model** : d
- **Feature Selection** : 건물별로 Feature importance, Shap 지수 기준 하위 피쳐 드롭

## Data Preprocessing 
- Target encoding, Label encoding 
- Standard Scaling 

## Model 
- LGBM Catboost
- Auto ML  
- Optuna hyperparameter tuning

## Ensemble 
- 10Fold, SEED ensemble

## Environment
- OS: Ubuntu 18.04.4 LTS (GNU/Linux 4.15.0-162-generic x86_64)
- Environment: Anaconda 4.10.3
