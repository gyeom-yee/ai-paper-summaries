# Stress Detection Using Natural Language Processing and Machine Learning Over Social Interactions
   - **저자**: Tanya Nijhawan, Girija V. Attigeri, A. T
   - **발표일**: 2022-05-20
   - **인용 횟수**: 46회
   - **키워드**: Decision tree, Latent Dirichlet Algorithm, Logistic regression, Machine learning, Natural Language Processing, Random forest, Sentiment analysis, Topic modelling
   - **개요**: 소셜 네트워킹 플랫폼에서 공유된 게시물과 댓글을 기반으로 개인의 스트레스를 감지  
   - **발행**: Journal of Big Data
   - **기관**: Manipal Institute of Technology, Manipal Academy of Higher Education
   - [논문 링크](https://journalofbigdata.springeropen.com/articles/10.1186/s40537-022-00575-6)  

※ Sentiment analysis and affective computing for depression monitoring 인용(33)

---

### 🤔 Problem
- 사람들이 소셜 미디어에 올리는 게시물과 댓글을 분석하여 개인의 스트레스 탐지
- 자연어 처리와 기계 학습을 활용하여 감정 분석의 확장

### 💡 Motivation
- 소셜 미디어 분석을 통한 개인의 정신 건강 상태 파악의 중요성
- 대규모 데이터셋과 기계 학습 알고리즘, BERT 모델 사용

### 🛠️ Method
- 트윗의 감정 이진 분류
- Latent Dirichlet Allocation(LDA)을 사용하여 각 주제의 밀도를 고려한 토픽 모델링 수행, 반복 과정을 통해 주제 구조를 계산
- 스트레스 탐지를 위해 딥러닝 기반의 BERT 모델을 사용한 감정 분류
- 사용자의 입력을 받아 예측을 생성하는 Django 기반 웹 어플리케이션 개발
- 스트레스 탐지뿐만 아니라 특정 트윗에서 논의되는 주제 분석도 가능한 웹 포털 형태의 시스템 개발
- 다양한 주제에 대한 사용자 의견을 정확하게 분석하고 구분

![image](https://github.com/gyeom-yee/ai-paper-summaries/assets/78156719/48b422cc-7c59-4f4b-9202-0c0842454030)

### 🔬 Experiment
- 데이터셋: 
  1) 100,042개의 트윗 / 3개의 열: 'id', 'sentiment label', 'sentiment text' / sentiment label: 0(positive), 1(negative)
  1) 7,934개의 트윗 / 3개의 열: 'id', 'emotion', 'text' / emotion: joy, sadness, neutral, anger, fear
- 전처리: 토큰화 이후 불필요한 패턴, 중지어 제거 및 스템밍(Bag-of-Words 사용)
- LDA를 사용한 Topic Modeling
  - LDA 시각화 파이썬 패키지인 PyLDAvis 사용
  - 결과표에 나온 topic에 붙어있는 번호는 서로 다른 주제를 구분하기 위한 레이블

![image](https://github.com/gyeom-yee/ai-paper-summaries/assets/78156719/cfb622bd-7f26-4cfa-b223-7101d1dba703)
- 이진 감정 분류(결과를 긍정/부정으로 분류)
  - 다양한 기계 학습 모델 비교: 로지스틱 회귀, 결정 트리, 랜덤 포레스트 등
  - BERT 모델: ktrain을 사용하여 pre-train / Transformer를 활용하여 텍트스틔 문맥 관계 파악 가능
- 트윗의 감정 상태 및 스트레스 수준 분석

![image](https://github.com/gyeom-yee/ai-paper-summaries/assets/78156719/535151c7-40e7-4385-a140-d12046cdb3ed)

### 🎯 Conclusion
- LDA 토픽 모델링과 시각화로 트윗을 탐색적 분석을 통해 추출된 토픽이 데이터에서 유의미한 구조를 가짐을 확인
- 머신러닝과 BERT 모델의 높은 정확도로 정신적 스트레스 탐지 가능
- 웹 포털 개발을 통한 사용자 감정 분류 및 스트레스 분석 가시화
- 향후 작업: 특정 트윗의 토론 주제까지 분석, 스팸 및 비스팸 트윗 탐지, 감성어 식별 알고리즘 개선

![image](https://github.com/gyeom-yee/ai-paper-summaries/assets/78156719/eab0b1f5-3f1e-43e6-b72f-2195235335e7)