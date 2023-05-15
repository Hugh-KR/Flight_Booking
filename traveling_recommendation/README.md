# traveling_recommendation
사용자 성격 기반, 사용자 현재 기분 기반, 여행지 테마(성향) 기반 여행지 추천 시스템

- 기술 스택: Anaconda, Python 3.7, Flask, tensorflow, pandas, numpy, Scikit learn, Jupyter, AWS(EC2(Ubuntu), RDS, S3)

## 데이터
- 여행지 리뷰 텍스트: 비짓 제주 리뷰 텍스트, 트립 어드바이저 리뷰 텍스트 크롤링
- 개인 성향 데이터: MBTI, 개인 성격에 따른 여행지 만족도 관련 연구 논문 바탕으로 설문지 문항 구성
- 구글 설문지: 개인 성향 파악을 위한 설문 문항에 대한 5지 선다형 + 개인의 기분에 따른 여행지 선호도

## 모델 구성
1. 여행지 리뷰 텍스트 테마 분류
   - input data:여행지 리뷰 텍스트 
   - 사용 모델: RNN
   - output: 레저/체험, 자연, 교육 분류 (by softmax)
2. 여행지 추천 모델
    - input data: 개인 성향 설문, 여행지 분류 SOFTMAX DB, 감정 라벨링 데이터
    - 사용 모델: DNN
    - output: 여행지 추천 여부
    
