# Twitter Arabic Sentiment Analysis to Detect Depression Using Machine Learning
   - **저자**: Dhiaa A. Musleh, Taef A. Alkhales, Reem A. Almakki, Shahad E. Alnajim, Shaden K. Almarshad, Rana S. Alhasaniah, Sumayh S. Aljameel, Abdullah A. Almuqhim
   - **발표일**: 2021-10-11
   - **키워드**: Depression, sentiment analysis, twitter, supervised learning, machine learning
   - **개요**: 아랍어 트위터 사용자의 트윗을 분석하여 우울증을 탐지하는 기계 학습 모델 개발에 관한 연구입니다.
   - **인용 횟수**: 19회
   - **발행**: Computers Materials & Continua
   - **기관**:  Imam Abdulrahman Bin Faisal University, Department of Computer Science, College of Computer Science and Information Technology
   - [논문 링크](https://dx.doi.org/10.32604/cmc.2022.022508)

---

### 🤔 Problem
- 전 세계적으로 우울증은 주요 문제이지만 아랍어를 사용하는 지역에서 우울증에 대한 인식과 치료가 부족한 상황
- 소셜 미디어, 그중 트위터 사용자를 분석하여 우울증 여부를 파악하는 것의 중요성

### 💡 Motivation
- 영어에 비해 아랍어 트윗을 통한 우울증 감지 연구의 부족과 어려움
- 자연어 처리(NLP), 머신러닝 기법 활용하여 아랍어 트위터 사용자의 우울증 감지

### 🛠️ Method
- 데이터 수집: CES-D 설문조사에 응답 및 진단 시사 아랍어 트위터 사용자로부터 수집
- 사용된 모델: SVM, RF, LR, KNN, AdaBoost, NB
- 평가 지표: accuracy, recall, precision, F1 score
- 사용된 아랍어:
  - Modern Standard Arabic (MSA): 실사용이 적음
  - Dialectal Arabic (DA): 가장 자주 사용되며 의사소통

![image](https://github.com/gyeom-yee/ai-paper-summaries/assets/78156719/c965a768-7c6f-474b-9b13-2c3f050f1c08)

### 🔬 Experiment
- 데이터셋(4542*3): 
  - 열[0] 전체 텍스트
  - 열[1] 우울증 징후(The American Psychiatric Association Diagnostic Depression Nine Symptoms, **Table 2**)
![image](https://github.com/gyeom-yee/ai-paper-summaries/assets/78156719/39beb463-49df-4d7e-8c0c-6cda1be2ce91)
  - 열[2] 세 가지 클래스(우울, 비우울, 중립)
- 전처리
  - Pyarabic, re 라이브러리 사용하여 Normalization
  - Stop-word Removal, Tokenization, Stemming
- Feature Extraction (TF-IDF, N-gram)
  - Term frequency-inverse document frequency (TF-IDF)
    - $TF − IDF(t, d) = TF(t, d) ∗ IDF(t)$
    - TF(t, d)는 문서 'd'에서 't'라는 단어가 나타나는 횟수
    - $IDF(t) = log(n/DF(t))+ 1$
    - 'n'은 총 문서 수이고 'DF(t)'는 't'라는 단어가 포함된 문서 수
  - N-gram
    - 텍스트에서 문자 또는 단어를 추출 (어간, 맞춤법 검사 및 텍스트 압축에 사용)
- 결과 및 토론: 
  - RF가 다른 모델에 비해 우수한 성능(82.39%의 정확도)을 보임
  - 우울한 사용자는 온라인 상호작용(언급, 리트윗)이 상대적으로 적은 양상을 보임
  - 우울한 사용자는이모티콘 사용률이 낮으며 혹여 사용해도 부정적인 이모티콘 사용
  - TF-IDF를 사용한 N-그램 데이터셋의 모델 성능 향상
![image](https://github.com/gyeom-yee/ai-paper-summaries/assets/78156719/d095ee95-dc99-4f20-af06-c8166db044ac)

### 🎯 Conclusion
- 아랍어 소셜 미디어 데이터를 통한 우울증 감지의 잠재력 확인, 이를 통해 우울증 예방 및 조기 감지에 기여할 수 있음
- 향후 작업: 데이터셋 크기 확대, 더 많은 모델, 트윗 시간 추가