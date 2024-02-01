# Natural language processing and psychosis: on the need for comprehensive psychometric evaluation
   - **저자**: Alex S Cohen, Zachary Rodriguez, Kiara K Warren, Tovah Cowan, Michael D Masucci, Ole Edvard Granrud, Terje B Holmlund, Chelsea Chandler, Peter W Foltz, Gregory P Strauss
   - **발표일**: 2022-06-23
   - **키워드**: machine learning, reliability, validity, psychometrics, psychosis, paranoia, bias
   - **개요**: 스마트폰 기기로 촬영한 비디오 '셀카'에서 임상적으로 평가된 편집증을 추적하기 위한 자연어 처리 측정법을 개발하는 과정에서 이러한 문제를 집중적으로 다룹니다. 조현병 또는 양극성 장애를 앓고 있는 환자를 모집하여 일주일 동안 추적했습니다. 499개 언어 샘플의 소규모 NLP 기반 기능 세트는 정규화된 회귀를 사용하여 임상적으로 평가된 편집증에 대해 모델링
   - **인용 횟수**: 18회
   - **발행**: Schizophrenia Bulletin
   - **기관**:  Louisiana State University Department of Psychology, Louisiana State University Center for Computation and Technology, ...
   - [논문 링크](https://academic.oup.com/schizophreniabulletin/article/48/5/939/6615341)

---

### 🤔 Problem
- 정신 질환, 특히 정신병 환자에서의 편집증을 모니터링하기 위한 자연어 처리(NLP) 측정 도구의 개발에 초점
- NLP는 정신 질환 연구에서 중요한 개념임에도 불구하고 임상 적용에는 장애가 있음

### 💡 Motivation
- 정신 질환 연구에서 자연어 처리(NLP) 임상 적용을 위한 종합적인 심리측정 평가 필요
- 정신병 스펙트럼 장애의 다양한 측면을 '디지털 표현형화'하여 진단, 평가 및 치료 재구성

### 🛠️ Method
- Serious mental illness(SMI) 환자들로부터 스마트폰 기기로 촬영한 '비디오 셀카'에서 임상적으로 평가된 편집증을 추적하기 위한 자연어 처리 측정법 개발

### 🔬 Experiment
- 조현병 또는 양극성 장애를 앓고 있는 환자를 모집하여 일주일 동안 추적
- NLP procedure: Sentiment analysis
  - 편집증의 정의가 외부에서 자아로 향하는 위협이라는 점을 감안하여 'self-other'참조에 초점  
  \* 'Self-other' 참조는 개인(자아)과 다른 사람이나 대상(비자아) 사이의 관계를 언어적으로 어떻게 표현하는지 식별하는 것
  - 집을 떠난 상태, 낯선 사람들과 있는 상태, 혼자 있는 상태 여부에 따라 세 가지 조절 변수 고려
  - NLP 측정(평가 방법): 
    - test-retest reliability(using Intra-class Correlation Coeffcients; ICC)
    - 의심/공포에 대한 모바일 측정치와의 일치도
    - 우울증/불안에 대한 임상 평가와의 차이
    - 인구 통계 변수에서의 잠재적 편향성
- 환자 35명으로부터 499개의 언어 샘플로(영상에서 텍스트로 전사) 구성된 데이터셋을 정규화된 회귀를 사용하여 모델링
  - NLTK, Stanford CoreNLP 활용하여 전처리
  - SentimentR 패키지 사용하여 감정 분석 (-1 ~ 1, 부정/중립/긍정)
- 결과:
  - 통합 NLP 측정은 임상적으로 평가된 편집증이 인종과 성별에 따라 예측이 달라짐을 보임
![image](https://github.com/gyeom-yee/ai-paper-summaries/assets/78156719/00be20f0-7bcc-4a16-814e-9a8aaf823238)

### 🎯 Conclusion
- NLP 기반 편집증 측정은 일주일 동안 신뢰성과 본 논문의 기준 및 개념적 관련 측정치와 우수한 수렴성 가짐
- 부정적인 감정과 정신병리의 전반적인 측정과 특이성/상관성을 보임
- 한계: 표본의 규모가 크지 않고 인구통계학적 제약이 있음, 많은 참가자의 비디오 데이터가 불완전
  - 향후 더 넓은 범위의 continuum of symptom severity 샘플 연구 중요