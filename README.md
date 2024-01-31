
## Dacon 전력사용량 예측 AI 경진대회

- 대회 개요 (2023.07.17 ~ 2023.08.28) https://dacon.io/competitions/official/236127/overview/description
- 시계열 회귀 예측 (SMAPE)
- 건물 정보와 시공간 정보를 활용하여 특정 시점의 전력 사용량을 예측하는 AI 모델 개발 
- 성과 : private 5.7%이내 - 70등/1233팀

## Summary
- **Data Selection** : 건물 개별(총 100개 건물) 예측 
- **Feature Engineering** : 기온 및 습도 파생 변수 추가 (discomfort, CDH 등), 공휴일 추가, 시계열 변수들을 이동평균값 EMA으로 조정 후 예측
- **Visualization** : 과거 및 예측 전력량 시각화하여 공휴일 확인 및 피쳐 추가/드롭에 반영
- **Feature Selection** : 건물별로 Feature importance, Shap 지수 기준 하위 피쳐 드롭
- **Model** : LGBM 모델 사용 - 팀원별 LGBM 예측치 산술평균 앙상블

## Review 
- 속도 문제로 다양한 모델 활용하지 못함
- 예측값 (전력량) 자체에 대한 이동평균 및 log화 시도 가능성
- 건물 유형별 (백화점, 데이터센터 등) 전력량 mean, std, max 등 활용 가능성

## Environment
- OS: Ubuntu 18.04.4 LTS (GNU/Linux 4.15.0-162-generic x86_64)
- Environment: Anaconda 4.10.3
