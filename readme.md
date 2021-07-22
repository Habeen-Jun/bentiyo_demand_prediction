프로젝트명 : 벤티요 미국 판매 데이터 기반 각 주별 수요 예측 모델 개발

<실행단계 및 소스코드 설명서>

1. 데이터 수집

* weatherAPI.py -> 미국 주별, 일별 날씨 데이터 수집 용
* scraping.py -> 미국 주별, 월별 날씨 데이터 수집 용

2. 데이터 분석

* 판매데이터분석.ipynb -> 벤티요 회사의 판매 데이터 EDA(탐색적 데이터 분석 수행)

입력데이터: orderdata.xlsx

* 변수간상관관계분석.ipynb -> 타겟변수(Quantity)와 상관관계 높은 종속변수 추출

입력데이터: OrderData + ChildData.xlsx


* 인구수 데이터 + 판매데이터.ipynb -> 각 주별 0-4세 영유아 인구수 데이터와 판매데이터 merge (key = state)

입력데이터: childpopulationUnder4.xlsx, processed_orderdata.xlsx, tatesAbbrev.xlsx
출력데이터: child_data.xlsx, OrderData + ChildData.xlsx

3. AI 모델링
lstm.ipynb
입력데이터: final_merged_cali.csv
->  학습된 weight(가중치) 로드하는 부분에서 오류 해결 필요

VAR.ipynb
입력데이터: final_merged_cali.csv


