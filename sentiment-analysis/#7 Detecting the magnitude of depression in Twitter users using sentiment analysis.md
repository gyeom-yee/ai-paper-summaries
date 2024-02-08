# Detecting the magnitude of depression in Twitter users using sentiment analysis
   - **저자**: JJ Stephen, P Prabu
   - **발표일**: 2019-04-13
   - **인용 횟수**: 68회 (24.01 기준)
   - **키워드**: Depression, Emotional integrity, Sentiment analysis, Twitter data, Weighted average scoring
   - **개요**: 계산된 감정 점수를 다른 감정과 결합하여 우울증 점수를 계산하는 더 나은 방법을 제공
   - **발행**: International Journal of Electrical and Computer Engineering (IJECE)
   - **기관**: Christ (Deemed University) Department of Computer Science
   - [논문 링크](https://www.academia.edu/43685211/Detecting_the_magnitude_of_depression_in_Twitter_users_using_sentiment_analysis)

---

### 🤔 Problem
- 트위터 사용자의 우울증 정도를 효율적으로 감지하는 방법 제안

### 💡 Motivation
- 사람의 정서적 일관성 기반의 우울증 평가 가능 여부

### 🛠️ Method
- 데이터 수집(Python): 
   1) 트위터 개발자 계정의 API로 트윗 추출
   2) 추출된 트윗의 json 데이터 파싱
   3) 선택된 데이터를 특정 형식으로 CSV 파일 생성
- 계산 및 시각화(R): 기본 감정 분석, 감정 계산 및 우울증 점수 계산, 시각화(ggplot)

### 🔬 Experiment
1) 말뭉치 구축: 우울증 관련 태그를 사용한 사용자 목록 큐레이션하여 데이터 추출(52명 / 각 사용자 평균 약 2,000개 트윗 / 데이터를 하루 단위로 세분화)
2) 데이터 전처리: 
   - File Conversion: 유니코드 특수 기호 제거, 메타데이터 키값이 있는 데이터만 선택, 쉼표 구분 CSV 생성
   - Data Cleaning: 특수 기호 제거 후 null값 생성 과정 생략, 소문자화
   - Stop Word Removal: TM라이브러리 사용, 우울증 분석을 위해 긍정 중지 단어만 제거
3) 우울증 정도 계산:
   - 기본 감정 계산: Syuzhet 패키지 사용, 각 트윗에 대한 기본 감정 계산하여 8가지(anger, anticipation, disgust, fear, joy, sadness, surprise, trust) 감정 목록 구현 / 긍정, 부정 추가
   - 감정 점수 평가: 트윗을 bigram과 trigram으로 토큰화한 후 AFINN, BING, NRC 세 가지 어휘집으로 감정 분석 / 이후 정규화하고 평균 내어 트윗 묶음(데이터는 하루 단위)에 대한 최종 감정 점수 계산
   ![image](https://github.com/gyeom-yee/ai-paper-summaries/assets/78156719/996fd757-c6ff-4992-a8ca-b0c6ba4f4af7)
   - 가중 평균 점수 및 최종 우울증 정도: 평가에 사용된 각 감정 8가지에 대해 특정 가중치 부여 후 최종 감정 점수와 곱한 값을 합하고 정규화하여 __사용자의 일일 우울 수준 도출__
   ![image](https://github.com/gyeom-yee/ai-paper-summaries/assets/78156719/d203eee5-6faa-4ea1-b6a2-088a57bad452)
- 결과:
   - 일일 우울 수준값으로 우울증 단정짓지 못하지만(장기간 영향을 끼치기에) 해당 기간 동안 우울증에 걸렸을 가능성 시사
   - 시각화 인사이트: 음수값인 날(우울한 상태)의 트윗은 특정 패턴(시간대, 요일)을 보임

### 🎯 Conclusion
- 결론: 트위터 트윗을 통해 우울증의 수준을 평가할 수 있음을 보여주며, 우울증과 관련된 트윗의 패턴 식별