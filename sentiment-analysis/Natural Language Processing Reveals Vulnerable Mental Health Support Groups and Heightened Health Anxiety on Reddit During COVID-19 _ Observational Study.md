# Natural Language Processing Reveals Vulnerable Mental Health Support Groups and Heightened Health Anxiety on Reddit During COVID-19: Observational Study
   - **저자**: D. Low, Laurie Rumker, Tanya Talkar, J. Torous, G. Cecchi, Satrajit S. Ghosh
   - **발표일**: 2020-07-19
   - **인용 횟수**: 247회
   - **키워드**: COVID-19, mental health, psychiatry, infodemiology, infoveillance, infodemic, social media, Reddit, ADHD, eating disorders, anxiety, suicidality
   - **개요**: COVID-19 기간 동안 Reddit의 정신 건강 지원 그룹에서 나타난 건강 불안과 변화를 분석한 연구입니다.
   - **발행**: Journal of medical Internet research
   - **기관**: URCI Mental Health Department, Brest Medical University Hospital / IMT Atlantique, Lab-STICC UMR CNRS 6285 / ...
   - [논문 링크](https://dx.doi.org/10.2196/22635)

---

### 🤔 Problem
- 자연어 처리(NLP)를 활용하여 Reddit에서 발견되는 세계 최대 규모의 정신 건강 지원 그룹 15개와 팬데믹 초기 단계의 비정신 건강 그룹 11개의 변화를 특성화하기 위한 것

### 💡 Motivation
- 코로나19 팬데믹이 정신건강에 영향을 미친다고 하지만, 팬데믹 초기 단계의 다양한 유형의 정신건강 문제를 가진 사람들이 어떻게 영향 받았는지 명확하지 않음

### 🛠️ Method
- Reddit 게시물에서 다양한 언어적 특징 추출 및 분석
- 자연 언어 처리(NLP), 감정 분석, TF-IDF 기법 등 사용
- 특정 멘탈 헬스 관련 서브레딧과 비멘탈 헬스 서브레딧 비교


### 🔬 Experiment
- Dataset:
  - 15개의 특정 멘탈 헬스 커뮤니티 서브레딧, 2개의 광범위한 멘탈 헬스 서브레딧, 11개의 비멘탈 헬스 서브레딧에서 게시물 추출
- Feature Extraction (특정 게시물을 특징짓는 단어와 구 포착)
  - LIWC, 감정 분석, TF-IDF n-gram / 각종 정신질환 관련 어휘집 수동으로 구축(자살, 경제적 스트레스, 고립, ...)
- 분석 방법: 추세 분석, 이진 분류, 차원 축소, 클러스터링 등 다양한 기계 학습 방법 적용
  - 추세 분석: TF-IDF를 제외한 모든 피처 사용
  - 분류 / 지도 차원 축소 / 비지도 클러스터링: 모든 피처 사용
    - 이진 분류
      - 세 가지 선형 모델: Stochastic Gradient Descent linear classifier (SGD) with L1 penalty, SGD with elastic net penalty, linear support vector machine
      - 두 개의 더 복잡한 트리 앙상블 분류기: extra trees, gradient boosting trees
    - 비지도 클러스터링: SpectralClustering
- Supervised ML을 사용하여 게시물을 각각의 지원 그룹으로 분류하고 중요한 특징을 해석하여 언어에서 다양한 문제가 어떻게 나타나는지 파악
- 한 토픽 모델링과 비지도 클러스터링과 같은 비지도 방법을 적용하여 팬데믹 이전과 기간 동안 Reddit 전체에서 우려되는 사항을 발견
![image](https://github.com/gyeom-yee/ai-paper-summaries/assets/78156719/9c45bc36-2a75-4afd-8c0d-32cfb97fb78b)

### 🎯 Conclusion
- 커뮤니티를 구분하는 언어적 특징과 팬데믹 기간 동안 언어 사용이 어떻게 변화했는지를 이해함으로써 임상 환경에서 평가할 수 있는 몇 가지 중요한 가설을 통해 치료에 도움을 줄 수 있음
- 중요한 것은 여러 분석에서 건강 불안과 자살률 증가
- 한계: 공식적으로 문서화된 임상 진단을 받은 참가자가 없었음, 선택 편향이 존재할 수 있으므로 관찰 연구 설계의 한계가 있음