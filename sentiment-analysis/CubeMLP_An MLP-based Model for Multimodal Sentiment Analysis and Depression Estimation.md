# CubeMLP: An MLP-based Model for Multimodal Sentiment Analysis and Depression Estimation
- **저자**: Hao Sun, Hongyi Wang, Jiaqing Liu, Yen-Wei Chen, Lanfen Lin
- **발표일**: 2022-10-10
- **키워드**: multimodal processing, multimodal fusion, multimodal interaction, multimedia, MLP, sentiment analysis, depression detection
- **개요**: 다중 모달 데이터를 사용하여 인간의 정신 상태를 예측하는 데 중점을 두는 다중 모달 감정 분석 및 우울증 추정
- **인용 횟수**: 22회
- **발행**: ACM Transactions on Asian and Low-Resource Language Information Processing (TALLIP)
- **기관**: Zhejiang University, Ritsumeikan University
- [논문 링크](https://dl.acm.org/doi/abs/10.1145/3503161.3548025)

---

### 🤔 Problem
- feature-mixing관점의 멀티모달 접근 방식 분석
- Multimodal feature-processing 프레임워크인 CubeMLP 소개

### 💡 Motivation
- 멀티모달 접근 방식을 특징 혼합 관점에서 탐구
- 컴퓨터 비전 작업에서 주목할 만한 성공을 거둔 MLP 기반에 영감

### 🛠️ Method
- CubeMLP: MLP Multimodal feature-processing 프레임워크
  - Transfomer의 self-attention 매커니즘은 상당한 메모리 필요
  - 이를 대체하기 위한 MLP로만 구성된 구조 관심
- 데이터셋:
  - 감정 분석 데이터셋: : CMU-MOSI, CMU-MOSEI
  - 우울증 추정 데이터셋: AVEC2019

### 🔬 Experiment
- 실험 방법:
  1) CubeMLP는 세 개의 독립적인 MLP 유닛 구성 (𝐿, 𝑀, 𝐷) / 각 유닛은 두 개의 affine transformations을 가짐
  2) 모든 관련 모달리티 피처를 입력으로 받아들여 세 축에 걸쳐 혼합
     - 첫 번째 MLP 유닛은 L축의 피처를 sequential-mixing
     - 두 번째 MLP 유닛은 M축의 피처를 Modality-mixing (𝑡: 발화 단어, 𝑎: 음향 톤, 𝑣: 사람의 표정)
     - 세 번째 MLP 유닛은 D축의 피처를 channel-mixing
![image](https://github.com/gyeom-yee/ai-paper-summaries/assets/78156719/3901d2c3-593d-4c35-b255-b9fb6c63f028)
![image](https://github.com/gyeom-yee/ai-paper-summaries/assets/78156719/0c9bb6b0-1516-4917-8663-44c3eb43818f)
  3) 특징 추출 후, 혼합된 멀티모달 특징 평탄화하여 예측
     - 멀티모달 감성 분석: 평균 절대 오차(MAE) 손실 비용 계산
     - 우울증 감지: 일치 상관 계수(CCC) 손실 비용 계산
![image](https://github.com/gyeom-yee/ai-paper-summaries/assets/78156719/51aeaee9-0ba1-4ac6-85fa-be7b0c5b6692)
![image](https://github.com/gyeom-yee/ai-paper-summaries/assets/78156719/99f2c925-3236-4e67-8f40-90857689c94a)

### 🎯 Conclusion
- CubeMLP는 계산 부담을 낮추면서도 감정 분석과 우울증 감지에서 SOTA급 성능 달성 가능
- MLP의 효율성과 멀티모달 처리 능력을 향상시키기 위해 넓은 범위의 제거 연구와 시각적 분석 수행