# 제조 AI 실제 (Manufacturing AI Practical)

대학원 2학기 **제조 AI 실제** 과목의 주차별 실습 과제를 정리한 저장소입니다.
CWRU(Case Western Reserve University) 모터 베어링 진동 실데이터와 공개 데이터셋을 활용해 패턴인식·특징 추출부터 딥러닝 기초까지 실습합니다.

## 폴더 구조

```
manufacturing-ai-practical/
├── README.md
├── 2주차/
│   ├── manufacturing_ai_lab2_1.ipynb   # 실습 2-1: 좋은 특징(Good Feature)과 클래스 분리성
│   ├── manufacturing_ai_lab2_2.ipynb   # 실습 2-2: 제약 조건(Constraints)과 일반화
│   ├── cwru_normal.mat                 # CWRU 정상(Normal) 베어링 진동 데이터
│   └── cwru_fault.mat                  # CWRU 결함(Inner Race Fault) 베어링 진동 데이터
└── 3주차/
    ├── linear_regression.ipynb         # 실습 3-1: 선형회귀 (Linear Regression)
    ├── logistic_regression.ipynb       # 실습 3-2: 로지스틱 회귀 (Logistic Regression)
    └── mnist_nn_classification.ipynb   # 실습 3-3: 신경망 분류 (Neural Network, MNIST)
```

## 주차별 실습 내용

| 주차 | 파일 | 주제 | 핵심 개념 |
| :---: | --- | --- | --- |
| 2주차 | `manufacturing_ai_lab2_1.ipynb` | 좋은 특징(Good Feature)의 정의와 클래스 분리성(Separability) 체감 | 패턴/특징의 정의, 나쁜 특징(Mean, 순간값) vs 좋은 특징(RMS, 고주파 스펙트럼 비율), Fisher 분리도 지수, Logistic Regression 분류 성능 비교 |
| 2주차 | `manufacturing_ai_lab2_2.ipynb` | 제약 조건(Constraints)에 따른 일반화(Generalization)와 문제 난이도 비교 | 데이터/환경 제약(노이즈 제거), 모델 제약(선형 구조·L2 정규화·가우시안 가정), 작업 제약(회귀 → 2진 분류 단순화) |
| 3주차 | `linear_regression.ipynb` | TensorFlow를 활용한 선형회귀 | `Dense(1)`, MSE / SGD, 가중치·절편 학습, 샘플 수·잡음의 영향 |
| 3주차 | `logistic_regression.ipynb` | 로지스틱 회귀로 Iris 이진 분류(Setosa vs 나머지) | 시그모이드, 표준화(StandardScaler), Binary Crossentropy, 결정 경계(Decision Boundary) 시각화 |
| 3주차 | `mnist_nn_classification.ipynb` | 신경망을 활용한 MNIST 손글씨 숫자 분류 | 다층 신경망(ReLU·Softmax), One-hot 인코딩, Adam, 과적합(Overfitting) 관찰 |

## 데이터

- **CWRU Bearing Dataset** (2주차): Case Western Reserve University에서 공개한 모터 베어링 진동 데이터셋
  - `cwru_normal.mat` — 정상 상태 진동 신호
  - `cwru_fault.mat` — 내륜 결함(Inner Race Fault) 진동 신호
  - 노트북과 같은 폴더에 두고 상대 경로로 불러옵니다.
- **Iris / MNIST** (3주차): `scikit-learn`과 `tensorflow.keras.datasets`에 내장되어 있어 별도 파일 없이 자동으로 불러옵니다.

## 실행 방법

1. 저장소를 클론합니다.
   ```bash
   git clone https://github.com/gukim1991/manufacturing-ai-practical.git
   cd manufacturing-ai-practical
   ```
2. 필요한 패키지를 설치합니다.
   ```bash
   # 2주차
   pip install numpy scipy matplotlib scikit-learn jupyter
   # 3주차 (TensorFlow 추가)
   pip install tensorflow
   ```
3. 해당 주차 폴더의 노트북을 Jupyter Notebook 또는 Google Colab에서 열어 실행합니다.
   - 2주차: Colab에서 실행할 경우 `.mat` 파일을 함께 업로드하세요.
   - 3주차: Iris·MNIST 데이터는 자동으로 불러오므로 별도 업로드가 필요 없습니다.

## 진행 현황

- [x] 2주차 — 좋은 특징과 분리성 / 제약 조건과 일반화
- [x] 3주차 — 선형회귀 · 로지스틱 회귀 · 신경망 분류(MNIST)
- [ ] 4주차
