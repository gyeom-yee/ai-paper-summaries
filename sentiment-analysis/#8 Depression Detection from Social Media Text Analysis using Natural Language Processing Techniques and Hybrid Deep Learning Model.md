# Depression Detection from Social Media Text Analysis using Natural Language Processing Techniques and Hybrid Deep Learning Model
   - **저자**: Vankayala Tejaswini, Korra Sathya Babu, Bibhudatta Sahoo
   - **발표일**: 2022-11-05
   - **키워드**: Deep learning, Depression, Natural language processing, Social Media Conversations
   - **개요**: 소셜 미디어 텍스트 분석을 통해 우울증을 탐지하기 위한 자연어 처리 기술과 하이브리드 딥 러닝 모델에 관한 연구
   - **인용 횟수**: 5회
   - **발행**: ACM Transactions on Asian and Low-Resource Language Information Processing (TALLIP)
   - **기관**: National Institute of Technology Rourkela, Odisha, Indian Institute of Information Technology Design and Manufacturing Kurnool, Andhra Pradesh
   - [논문 링크](https://dx.doi.org/10.1145/3569580)

---

### 🤔 Problem
- 우울증 식별을 위한 딥러닝 하이브리드 모델 개발
- 소셜 미디어를 통해 공유된 텍스트에서 우울증을 감지

### 💡 Motivation
- 우울증 환자 수의 급증과 이에 대한 조기 감지의 중요성 인식
- 우울증 환자의 경우 자신을 감추려는 경향을 가지며, 간편하고 메모리 효율적인 텍스트를 많이 활용하기에 자연어처리 연구에 적합

### 🛠️ Method
- 데이터셋:
  1) Reddit [링크](https://www.nature.com/articles/s41598-020-68764-y)
  2) Kaggle [링크](https://www.kaggle.com/datasets/hyunkic/twitter-depression-dataset)
- 전처리
  - NLTK, Gensim 라이브러리
  - 토큰화, 소문자 사용, 중지 단어 제거, 어간 추출, 축약
- 단어 임베딩과 하이브리드 딥러닝 모델을 결합하면 우울증을 높은 정확도로 검출
- 사용된 모델: FCL
  - CNN, LSTM: Keras, Tesor-flow
  - FastText 임베딩(with N-gram; 말뭉치에 없는 단어 구성), CNN, LSTM
- 평가 지표: Accuracy, Precision, Recall, F1-Score
![image](https://github.com/gyeom-yee/ai-paper-summaries/assets/78156719/2a53b9d4-8782-475f-92e5-18ee8d0dc7f3)

### 🔬 Experiment
![image](https://github.com/gyeom-yee/ai-paper-summaries/assets/78156719/1075de6e-95d2-401d-8d89-ce0f0fb6aac7)
- 참고 문헌들에서 대부분 데이터셋은 일반적으로 1만개 보다 적으면 'small', 많으면 'large'로 봄
- confusion matrix, error matrix, contingency table은 분류 모델 성능 평가 및 예측에 도움이 됨(Pareto Principle; 80:20 rule)

![image](https://github.com/gyeom-yee/ai-paper-summaries/assets/78156719/6b774448-12ea-4094-aee0-4f78b07b4b24)

### 🎯 Conclusion
- FCL 모델이 우울증 감지에 있어서 기존 방법보다 높은 성능을 보임
- 텍스트 분석은 공유된 텍스트의 기본 패턴을 지속적으로 모니터링하여 질병을 진단하는 데 도움
- 향후 연구 방향: 의료 진단 시스템 자동화, 복약 순응도 측정, 챗봇을 통한 환자와의 상호작용