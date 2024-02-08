# AVEC 2019 workshop and challenge: state-of-mind, detecting depression with AI, and cross-cultural affect recognition
   - **저자**: F. Ringeval, Björn Schuller, M. Valstar, N. Cummins, R. Cowie, Leili Tavabi, Maximilian Schmitt, Sina Alisamir, S. Amiriparian, Eva-Maria Messner, Siyang Song, Shuo Liu, Ziping Zhao, Adria Mallol-Ragolta, Zhao Ren, M. Soleymani, M. Pantic
   - **발표일**: 2019-10-15
   - **키워드**: Affective Computing, State-of-Mind, Cross-Cultural Emotion
   - **개요**: 정신 상태, 인공지능을 사용한 우울증 탐지, 그리고 문화 간 감정 인식에 관한 연구
   - **인용 횟수**: 258회
   - **발행**: ACM Transactions on Asian and Low-Resource Language Information Processing (TALLIP)
   - **기관**: Université Grenoble Alpes CNRS, University of Augsburg, University of Nottingham, Queen’s University Belfast, University of Southern California, Tianjin Normal University, Imperial College London, University of Ulm.
   - [논문 링크](https://dl.acm.org/doi/abs/10.1145/3347320.3357688)

---

### 🤔 Problem
- 멀티모달 정보 처리를 위한 공통 벤치마크 테스트셋을 제공함으로써 건강 및 감정 인식 시스템 발전
- 정신 상태, 인공지능을 이용한 우울증 감지, 그리고 문화 간 감정 인식의 자동 분석 방법론 비교

### 💡 Motivation
- 다양한 분야의 여러 커뮤니티, 특히 시청각 멀티미디어 커뮤니티와 표현 행동을 연구하는 심리 및 사회 과학 커뮤니티의 통합

### 🛠️ Method
- 상태 인식, 우울증 평가, 문화 간 감정 인식을 위한 서브 챌린지 개발
- 평가지표: 
  - Concordance Correlation Coefficient (CCC): 재현성 지표인 CCC는 규모와 양이온의 변화에 편향되지 않고 단일 통계 측정값에 정밀도와 정확도에 대한 정보를 모두 포함하기 때문에 가장 적합
  - Root Mean Squared Error (RMSE)

### 🔬 Experiment
- 건강과 감정 분석에 초점을 맞춘 세 가지 서브 챌린지
  - State-of-Mind Sub-challenge (SoMS):  인간의 state-of-mind(SOM)의 지속적인 적응에 초점을 맞춘 과제
  - Detecting Depression with AI Sub-challenge (DDS): 환자들이 AI로 완전히 운영되는 가상 에이전트와 상호작용하는 오디오비주얼 녹화를 통해 우울증의 심각성 수준(PHQ-8 설문지 기반)을 평가하는 과제
  - Cross-cultural Emotion Sub-challenge (CES): 오디오비주얼 녹화를 통해 "in-the-wild"에서 수집된 감정 차원을 추론하는 과제
- 데이터셋: 
  - Extended Distress Analysis Interview Corpus (E-DAIC): 불안, 우울증, 외상 후 스트레스 장애와 같은 심리적 장애 상태의 진단을 지원하기 위해 고안된 반임상 인터뷰가 포함된 WOZ-DAIC의 확장 버전
  - 오디오 및 비디오 녹음, Google Cloud의 음성 인식 서비스를 사용하여 자동으로 전사된 텍스트, 광범위한 설문 응답

### 🎯 Conclusion
- SoMS에서는 정적 점수로 시스템을 학습시키고 동적 보기로 평가했을 때
기분 수준을 가장 잘 예측
- DDS에서는 인터뷰를 수행하는 가상 에이전트가 전적으로 AI에 의해 구동될 때 우울증 수준(PHQ-8)을 예측하는 것이 WoZ 설정에 비해 더 어려움을 보임
- CES에서는 비디오 서술자가 오디오 서술자에 비해 더 나은 성능을 보이며, 특히 얼굴 표현의 보편성이 강조되며 음향에 차이가 있는 언어의 분석에 오디오 디스크립터 이용이 어려움을 보여줌