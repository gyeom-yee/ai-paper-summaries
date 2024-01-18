# Sentiment Analysis and Affective Computing for Depression Monitoring
   - **저자**: C. Zucco, B. Calabrese, M. Cannataro
   - **발표일**: 2017-11-01
   - **인용 횟수**: 94회 (24.01 기준)
   - **키워드**: depression, ehealth, sentiment analysis, affective computing, multimodal acquisition
   - **개요**: 우울증 감지 및 모니터링을 위한 감정 분석과 감성 컴퓨팅 방법론의 적용에 대해 논의한 연구
   - **발행**: IEEE
   - **기관**: Department of Medical and Surgical Sciences University "Magna Græcia"
   - [논문 링크](https://dx.doi.org/10.1109/BIBM.2017.8217966)

---

### 🤔 Problem
- mental disorders는 현재 의료진의 정보에 기반한 평가와 함께 자가 보고에 의존
- 정신 질환 임상 진단을 위해 설문지에 국한되지 않는 객관적인 방법 필요

### 💡 Motivation
- Sentiment and affective sensing technology는 객관적인 평가를 위한 효과적인 도구와 시스템을 제공함으로써 이러한 목표 달성에 도움을 줌

### 🛠️ Method
- polarity detection: 텍스트 T가 입력으로 주어졌을 때, 그 내용에 따라 T가 긍정/부정/중립 의견을 포함하는지 판단하고 그 내용이 얼마나 긍정/부정적인지 강도 파라미터를 도출 (리뷰, 정치 같은 여론 분석에 많이 쓰임)
- SA 맥락에서 널리 쓰이는 기본 감정 정의: 플루치크, 아놀드, 에크먼 이론

![기본 감정 정의](./img/image.png)

- Ⅰ. Sentiment Analysis (SA): 
  - "Given an input text T and a list $E = [E_1, ··· , E_k]$ of basic emotions type determine, on the basis of its content, whether the text $T$ contains one or more of the emotions $E_i$ for $i = 1 ··· k$ and what is the respective strength $s_i$ ."

<!-- ![SA](./img/sa.png) -->

- Ⅱ. Affective Computing (AC): 
  - 멀티모달 생체신호 수집 기반
  - 표정, 말투, 제스처, 움직임 등 신체적 측면 관련
  - 생리적 신호, 갈바닉 피부 반응(GSR), 호흡, 심박수(HR), 뇌파, 심전도, 근전도, 시선 추적

<!-- ![AC](./img/ac.png) -->

- Ⅲ. 우울증 감지 및 모니터링
  - 진단 및 통계 메뉴얼: [19]
  - 설문지에서 벗어난 객관화(우울증과 연관된 신체적 신호 초점)
    - 스트레스 수준, 머리 움직임, 음성 및 표정
    - 가장 많이 추출된 음향 특징: Pitch, 기본 주파수(F0), Formants, Power Spectral Density (PSD), Speaking Rate, Mel Frequency Cepstral Coefficients (MFCC)
    - 표정 감정 추출: Ekman의 emotional facial action coding system (EFACS)
  - 이미지 및 이모티콘 멀티모달 분석: [33]
  - PTSD, 우울증, 조울증, 계절성 정서 장애(SAD) 모니터링에 트위터 사용 및 다른 사례: [35~39]

### 🔬 Experiment
1) 람다 아키텍쳐 기반 우울증 모니터링 시스템: 텍스트, 멀티모달 소스 수신 후 실시간 연산 후 사용자의 기분에 따라 적합한 활동 제시  
※ 서로 다른 소스 융합 기법: Feature level fusion, Matching score level fusion, Decision level
2) 기분 평가를 위해 오프라인 계산(Analysis Box, Batch layer + speed layer) 수행
3) 일관된 정보로 병합된 Result (Serving layer)를 의사 제공

<!-- ![Architecture of the proposed system for depression monitoring](./img/Architecture%20of%20the%20proposed%20system%20for%20depression%20monitoring.png) -->
![Workflow for data acquisition and analysis](./img/Workflow%20for%20data%20acquisition%20and%20analysis.png)

### 🎯 Conclusion
- 우울증 상태 모니터링을 위한 SA 및 AC 방법론 기반 통합 멀티 모달 시스템 예비 설계 제시
- 향후 연구에서 최종 시스템과 결과 테스트 및 검증 예정

---