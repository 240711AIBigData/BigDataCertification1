# 분석기법 적용
# 1. 분석기법
회귀분석
---
### 회귀분석
- 개념

  - 독립변수들이 종속변수에 영향을 미치는지 파악하는 분석방법

    - 독립변수 : 원인을 나타내는 변수 (x)
   
    - 종속변수 : 결과를 나타내는 변수 (y)
   
    - 잔차 : 계산값과 예측값의 차이 (오차 : 모집단 기준, 잔차 : 표본집단 기준)
 
- 회귀계수 추정 방법

  - **최소제곱법** : 잔차의 제곱합이 최소가 되는 회귀계수와 절편을 구하는 방법
 
- 회귀모형 평가

  - **R-square** : 총 변동 중에서 회귀모형에 의하여 설명되는 변동이 차지하는 비율 (0 ~ 1)

<br>

### 선형회귀분석의 가정
- 선형성 : 종속변수와 독립변수는 선형관계

- 등분산성 : 잔차의 분산이 고르게 분포

- 정상성(정규성) : 잔차가 정규분포의 특성을 지님

- 독립성 : 독립변수들간 상관관계가 없음

  - **다중공선성** : 독립변수들간 강한 상관관계가 나타나는 문제
 
<br>

### 회귀분석 종류
- 단순회귀 : 1개의 독립변수와 종속변수의 선형관계

- 다중회귀 : 2개 이상의 독립변수와 종속변수의 선형관계

- 다항회귀 : 2개 이상의 독립변수와 종속변수가 2차 함수 이상의 관계

- 릿지회귀(L2 규제) / 라쏘회귀(L1 규제) : 규제를 포함하는 회귀 모형

<br>

### 회귀 모형의 구축절차
- 독립변수, 종송변수의 설정

- 회귀 계수의 추정

- 회귀 계수들의 유의성 검정

- 모형의 유의성 검정

<br>

### 회귀 모형의 변수 선택 방법
- 전진선택법 : 변수를 하나씩 추가하면서 최적의 회귀방정식을 찾아내는 방법

- 후진제거법 : 변수를 하나씩 제거하면서 최적의 회귀방정식을 찾아내는 방법

- 단계별 선택법 : 전진선택법 + 후진제거법으로 변수를 추가할 때 벌점 고려

  - AIC (아카이케 정보 기준)
 
    - 편향과 분산이 최적화되는 지점 탐색
   
    - 자료가 많을수록 부정확
   
  - BIC (베이즈 정보 기준)
 
    - AIC 를 보완했지만 AIC 보다 큰 패널티를 가지는 단점
   
<br>

로지스틱 회귀분석
---
### 로지스틱 회귀분석
- 종속변수가 **범주형 데이터**를 대상으로 성공과 실패 2개의 집단을 분류하는 문제에 활용

  - 오즈 (Odds)
 
    - 성공할 확률과 실패할 확률의 비
   
    - **Odds = 성공확률(P) / 실패확률(1-P)**
   
  - 로짓(logit) 변환
 
    - 오즈에 자연로그(자연상수 e가 밑)를 취하는 작업
   
    - 독립변수 X가 **n 증가하면 확률이 eⁿ** 만큼 증가
   
<br>

의사결정나무
---
### 의사결정나무(Decision Tree)
- 여러 개의 분리 기준으로 최종 분류 값을 찾는 방법

  - 분류(범주형)에서의 분할 방법
 
    - CHAID 알고리즘 : 카이제곱 통계량
   
    - CART 알고리즘 : **지니지수** 활용 (1 - ∑P²)
   
    - C4.5/C5.0 알고리즘 : **엔트로피지수** 활용 (- ∑P(log P))
   
  - 회귀(연속형)에서의 분할 방법
 
    - CHAID 알고리즘 : **ANOVA F통계량**
   
    - CART 알고리즘 : **분산감소량**
   
<br>

### 의사결정나무의 과적합 방지 방안
- **정지규칙** : 분리를 더 이상 수행하지 않고 나무의 성장을 멈춤

- **가지치기** : 일부 가지를 제거하여 과대적합을 방지

<br>

### 지니지수와 엔트로피지수의 계산
|동전 5개 중 앞면 3개, 뒷면 2개 라고 가정|
|:-:|
|<br>앞면 &nbsp;&nbsp;&nbsp;&nbsp; 뒷면 &nbsp;&nbsp;&nbsp;&nbsp; 앞면 &nbsp;&nbsp;&nbsp;&nbsp; 뒷면 &nbsp;&nbsp;&nbsp;&nbsp; 앞면 <br> &nbsp;|
- 앞면 확률 = 3/5 , 뒷면 확률 = 2/5
  
- 지니지수 : **1 - (3/5)² - (2/5)² = 12/25**

- 엔트로피지수 : -3/5log(3/5) - 2/5log(2/5)

<br>

인공신경망
---
### 인공신경망
- 인간의 뇌 구조를 모방한 퍼셉트론을 활용한 추론모델

  - 단층 신경망 : 입력층과 출력층으로 구성 (단일 퍼셉트론)
 
  - 다층 신경망 : 입력층과 출력층 사이에 1개 이상의 은닉층 보유 (다층 퍼셉트론)
 
    - 은닉층 수는 **사용자가 직접 설정**
   
<br>

### 활성화 함수
- 인공신경망의 선형성을 극복 (**XOR 문제 해결**)

  - 시그모이드 함수
 
    - 0 ~ 1 사이의 확률 값을 가지며, 로지스틱 회귀 분석과 유사
   
  - 소프트맥스 함

    - 출력 값이 여러 개로 주어지고 목표 데이터가 다범주인 경우 활용
   
  - 하이퍼볼릭 탄젠트(Tanh) 함수
 
    - **-1 ~ 1 사이 값**을 가지며, 시그모이드 함수의 최적화 지연을 해결
   
  - ReLU 함수
 
    - **기울기 소실문제를 극복**
   
    - max(0, x)

<br>

### 인공신경망의 과적합 방지방안
- 규제 : **라쏘(L1) 규제, 릿지(L2) 규제**

- **드롭아웃(Dropout)** : 일부 퍼셉트론을 비활성화시켜 학습

- 조기종료 : 특정 지점에서 학습 미리 종료

- 모델의 복잡도 줄이기 : 은닉층의 퍼셉트론 수 감소

- 데이터 증강 : 데이터에 변형을 주어 데이터 수 증가

- 배치 정규화 : 각 출력마다 정규화

<br>

### 인공신경망 학습 방법
- 순전파(피드포워드)

  - 정보가 전방으로 전달

- **역전파** 알고리즘

  - 가중치를 수정하여 오차를 줄임 (합성함수의 곱 활용)
 
- 경사하강법

  - 경사의 내리막길로 이동하여 오차가 최소가 되는 최적의 해를 찾는 기법 (편미분 활용)
 
- 기울기 소실 문제

  - 다수의 은닉층에서 **시그모이드 함수 사용** 시, 학습이 제대로 되지 않는 문제

<br>

서포트벡터머신
---
### 서포트벡터머신(SVM)
- 마진이 최대가 되는 초평면을 찾아 선형이나 비선형 분류, 회귀에서 활용 가능한 다목적 모델

  - 하이퍼플레인(초평면) : 데이터를 구분하는 기준이 되는 경계
 
  - 서포트벡터 : 클래스를 나누는 하이퍼플레인과 가까운 위치의 샘플
 
  - 마진 : 하이퍼플레인과 서포트벡터 사이의 거리
 
  - **커널함수** : 저차원 데이터를 고차원 데이터로 변경하는 함수
 
<br>

### 서포트벡터머신(SVM)의 유형
- 하드마진분류 : 오류 비허용

- 소프트마진분류 : 마진 내 어느 정도 오류 허용

<br>

연관성분석
---
### 연관분석
- 항목들간의 조건-결과로 이루어지는 패턴을 발견하는 기법 (**장바구니 분석**)

- 특징

  - 결과가 단순하고 분명 (IF ~ THEN ~)
 
  - 품목 수가 증가할수록 계산량이 기하급수적으로 증가
 
  - **Apriori 알고리즘**을 활용하여 연관분석을 수행
 
- 순차패턴

  - 연관분석에 **시간 개념을 추가**하여 품목과 시간에 대한 규칙 찾는 기법
 
<br>

### 연관분석의 지표 (*지신향*)
- *지*지도 : N(A∩B)/전체 = P(A∩B)

  - A와 B 두 품목이 동시에 포함된 거래 비율
 
- *신*뢰도 : P(A∩B)/P(A)

  - A 품목이 거래 될 때 B 품목도 거래될 확률 (**조건부 확률**)
 
- *향*상도 : P(A∩B)/P(A)P(B)

  - A 품목과 B 품목의 상관성
 
    - (향상도 > 1 : 양의 상관관계, 향상도 = 1 : 상관없음, 향상도 < 1 : 음의 상관관계)

<br>

#### 💡 맥주를 구매할 때 치킨을 구매하는 확률에 대한 신뢰도와 향상도
|거래코드|품목|거래 횟수|
|:-:|:-:|:-:|
|1|맥주|10|
|2|치킨|20|
|3|햄버거|70|
|4|맥주, 치킨|20|
|5|맥주, 햄버거|30|
|6|치킨, 햄버거|10|
|7|맥주, 치킨, 햄버거|40|

- 맥주의 구매 확률 = (10 + 20 + 30 + 40) / 200 = 0.5

- 치킨의 구매 확률 = (20 + 20 + 10 + 40) / 200 = 0.45

- 맥주와 치킨의 지지도 = (20 + 40) / 200 = 0.3

- 맥주 → 치킨의 **신뢰도 = 0.3 / 0.5 = 0.6**

- 맥주와 치킨의 **향상도 = 0.3 / (0.5 * 0.45) = 0.3 / 0.225 = 1.33**

  - 맥주와 치킨의 향상도가 1보다 크므로 **양의 상관관계**를 가짐

<br>

군집분석
---
### 군집분석
- 비지도 학습으로 데이터들 간 거리나 유사성을 기준으로 군집을 나누는 분석

<br>

### 거리측도
- (1) 연속형 변수 (*맨체*스터 *유*나이티드)

  - ***유*클리디안 거리** : 두 점 사이의 직선 거리
 
  - ***맨*하튼 거리** : 각 변수들의 차이의 단순 합
 
  - ***체*비셰프 거리** : 변수 거리 차 중 최댓값
 
  - 표준화 거리 : 유클리디안 거리를 표준편차로 나눔
 
  - 민코우스키 거리 : 유클리드, 맨하튼 거리를 일반화한 거리
 
  - 마할라노비스 거리 : 표준화 거리에서 변수의 상관성 고려

|연속형 변수의 거리 측도|
|-|
|![image](https://github.com/user-attachments/assets/77e16fbf-9a2d-47c1-a6c3-b13e09d713ee)|


- (2) 범주형 변수 (*자코*)

  - ***자*카드 유사도**
 
  - ***코*사인 유사도**

<br>

### 계층적 군집분석
- 거리측정 방법

  - 최단 연결법(단일 연결법) : 군집간 가장 가까운 데이터
 
  - 최장 연결법(완전 연결법) : 군집간 가장 먼 데이터
 
  - 평균 연결법 : 군집의 모든 데이터들의 평균
 
  - 중심 연결법 : 두 군집의 중심
 
  - 와드 연결법 : 두 군집의 편차 제곱합이 최소가 되는 위치
 
- 덴드로그램

  - 계층적 군집화를 시각적으로 나타내는 Tree 모양의 그래프

|덴드로그램|
|-|
|![image](https://github.com/user-attachments/assets/542532e6-5066-4397-a667-4e33d0366586)|
|- 거리를 15에서 나누면 3개의 클러스터, 25에서 나누면 2개의 클러스터로 나눌 수 있음|

<br>

### K평균 군집화 (K-means Clustering)
- 비계층적 군집화 방법으로 거리 기반

  - (1) 특징
 
    - 안정된 군집은 보장하나 최적의 보장은 어려움
   
    - 한번 군집에 속한 데이터는 **중심점이 변경되면 군집이 변할 수 있음**
   
  - (2) 과정
 
    - 군집의 개수 K개 설정 (**Elbow Method를 활용** 최적의 K 설정)
   
    - 초기 중심점 설정
   
    - 데이터들을 가장 가까운 군집에 할당
   
    - 데이터의 평균으로 중심점 재설정
   
    - 중심점 위치가 변하지 않을 때까지 '군집 할당 및 중심점 재설정' 과정 반복
   
  - (3) K-medoids 군집화
 
    - K평균 군집화의 이상치에 민감함을 대응하기 위한 군집방법
   
    - 일반적으로 실현된 것이 **PAM**(Partitioning Around Medoid)
   
<br>

### DBSCAN
- 비계층적 군집화 방법으로 밀도기반

- **군집 개수 지정할 필요 없음**

- 노이즈와 이상치에 강함

<br>

### 기타 비계층적 군집분석
- 퍼지군집화 - 확률 기반

  - 각 데이터가 특정 군집에 속할 확률을 각각 계산해가며 군집화
 
- EM알고리즘 - 분포 기반

  - Likelihood의 기댓값을 계산하는 E단계와 기댓값 최대화 추정값을 계산하는 M단계 반복
 
- 자기조직화지도(SOM) - 그래프 기반

  - **신경망을 활용**하여 차원축소를 통해 지도로 형상화하여 군집화하는 방법
 
<br>

---

<br>

# 2. 고급 분석기법
범주형 자료 분석
---
### 분할표
- 여러 개의 범주형 변수를 기준으로 관측치를 기록하는 표

- **오즈비(Odds Ratio)**

|오즈비|
|-|
|![image](https://github.com/user-attachments/assets/b236e7b6-4a33-4dbc-941f-58676dce7333)|

<br>

|-|심장질활 True|심장질활 False|합|
|:-:|:-:|:-:|:-:|
|알콜중독 True|14 (0.7)|6 (0.3)|20|
|알콜중독 False|10 (0.2)|40 (0.8)|50|

- Odds Ratio = (0.7 / 0.3) / (0.2 / 0.8) = 9.33

<br>

다변량 분석 (→ 차원축소)
---
### 요인분석 (Factor Analysis)
- 다수 변수들을 상관관계를 분석하여 소수의 요인으로 축약하는 기법

  - (1) 요인추출방법
 
    - 주성분분석(PCA) : 전체 분산을 토대로 요인을 추출, 가장 많이 사용
   
    - 공통요인분석 : 공통분산만을 토대로 요인을 추출
   
  - (2) 요인회전
 
    - 직각회전 : **VARIMAX**, QUARTIMAX, EQUIMAX
   
    - 사각회전 : OBLIMIN, PROMAX

<br>

시계열 분석
---
### 시계열 분석
- 시간의 흐름에 따라 관찰된 자료의 특성을 파악하여 미래를 예측 (주가데이터, 기온데이터)

<br>

### 정상성
- 시계열 예측을 위해서는 **모든 시점에 일정한 평균과 분산**을 가지는 정상성을 만족해야 함

- 정상시계열로 변환 방법

  - **차분** : 현 시점의 자료를 이전 값으로 빼는 방법
 
  - 지수변환, 로그변환
 
<br>

### 백색 잡음
- 시계열 모형의 오차항을 의미하며 원인은 알려져 있지 않음

- 평균이 0이면 가우시안 백색잡음

<br>

### 시계열 모형
- 자기회귀(AR) 모형

  - 자기자신의 과거 값이 미래를 결정하는 모형
 
  - 부분자기상관함수(PACF)를 활용하여 p+1 시점 이후 급격 감소하면 AR(p) 모형 선정
 
- 이동평균(MA) 모형

  - 이전 백색잡음들의 선형결합으로 표현되는 모형
 
  - 자기상관함수(ACF)를 활용하여 q+1 시차 이후 급격히 감소하면 MA(q) 모형 선정
 
- 자기회귀누적이동평균(ARIMA) 모형

  - AR 모형과 MA 모형의 결합
 
  - **ARIMA(p, d, q)**
 
    - p 와 q 는 AR 모형과 MA 모형이 관련 있는 차수
   
    - **d 는 정상화시에 차분 몇 번 했는지** 의미
   
    - d = 0 이면, ARMA 모델

<br>

### 분해시계열
- 시계열에 영향을 주는 일반적인 요인을 시계열에서 분리해 분석하는 방법 (*추*운 *계절*의 *순환*이 *불규칙*하다)

  - *추세* 요인 : 장기적으로 증가, 감소하는 추세
 
  - *계절* 요인 : 계절과 같이 고정된 주기에 따라 변화
 
  - *순환* 요인 : 알려지지 않은 주기를 갖고 변화 (**경제 전반, 특정 산업**)
 
  - *불규칙* 요인 : 위 3 가지로 설명 불가한 요인

<br>

베이지안 기법
---
### 베이즈 정리
- P(A|B) = P(B|A)P(A) / P(B) = P(A∩B) / P(B)

<br>

#### 💡 연습문제
> A 대학 입시에 응시한 남학생과 여학생의 비율이 60%와 40%이고 <br>
> 남학생의 합격률은 30%, 여학생의 합격률은 50% 이다. <br>
> 이때, A 대학에 합격한 신입생 중 남학생을 고를 확률은?

|우도표|합격률|불합격률|-|
|:-:|:-:|:-:|:-:|
|남학생|0.6 * 0.3 = 0.18|0.6 * 0.7 = 0.42|0.6|
|여학생|0.4 * 0.5 = 0.20|0.4 * 0.5 = 0.20|0.4|

- P(A|B) = P(남학생|합격한 신입생) = P(A∩B) / P(B) = 0.18 / 0.38 = 0.47

<br>

### 나이브베이즈 분류
- **나이브(독립) + 베이즈 이론**을 기반으로 범주에 속할 확률 계산

<br>

딥러닝 분석
---
### DNN (심층 신경망)
- 은닉층이 2개 이상으로 구성된 인공신경망

<br>

### CNN (합성곱 신경망)
- **Convolution Layer**와 **Pooling Layer**를 활용하여 이미지에서 패턴을 찾는 신경망

  - (1) 구조
  
    - Input - Convolution Layer - Pooling Layer - Flatten - Fully Connected Layer
   
  - (2) 개선된 CNN 모델
  
    - R-CNN, Fast CNN, Faster CNN, **YOLO**, EfficientNet

<br>

### RNN (순환 신경망)
- 순차적인 데이터 학습에 특화된 순환구조를 가지는 신경망

  - (1) **장기의존성 문제**
 
    - 은닉층의 과거 정보가 전달되지 못하는 형상
   
  - (2) 장기의존성 극복 모델
 
    - **LSTM** : Forget Gate, Input Gate, Output Gate
   
    - **GRU** : Reset Gate, Update Gate

<br>

### 오토인코더
- 입력 데이터를 인코더로 압축한 후에 디코더로 형태를 재구성하는 비지도 학습 신경망

  - VAE
 
    - **확률분포**를 학습하여 데이터 생성
   
  - GAN
 
    - 생성기와 판별기의 경쟁을 유사한 데이터를 생성 (**적대적 훈련**)
   
  - DCGAN
 
    - GAN + CNN 으로 안정적으로 학습

<br>   

#### 💡 오토 인코더는 생성형 AI의 기반 모델

<br>

비정형 데이터 분석
---
### 텍스트 마이닝
- (1) 통계적 기반

  - TDM
 
    - 문서에서 등장하는 단어들의 빈도를 행렬로 표현
   
  - TF-IDF
 
    - TF : 1개의 문서 내에서 특정 단어의 출현 빈도
   
    - IDF : 특정 단어가 전체 문서에 등장하는 정도
   
- (2) 단어 수준 기반

  - **Word2Vec** : 거리를 기반으로 벡터로 표현
 
    - CBOW : 앞, 뒤 단어로 주어진 단어를 유추
   
    - Skip-Gram : 중심단어에서 주변단어 예측
   
  - FastText : 하나의 단어를 여러 개로 잘라서 벡터로 계산
 
  - ELMo : 양방향 언어 모델을 적용

<br>

### 트랜스포머
- RNN 의 느린 속도와 병렬처리 불가 단점을 개선한 Attention 모델

  - 구성요소 : Positional Encoding, Self-Attention, Feed Forward Network
 
  - 주요 모델
 
    - BERT : 구글 개발, 인코더 구조, 문장 중간 빈칸 학습, 양방향
   
    - GPT : OpenAI 개발, 디코더 구조, 이전 단어로 다음 단어 예측, 일방향
   
<br>

### 기타 비정형 데이터 분석
- 유전자 알고리즘

  - **최적화** 필요한 문제의 해결책
 
  - 택배차량 어떻게 배치, 최대 시청률 얻으려면 어떤 프로그램을 어떤 시간대에 방송?
 
- 감정분석

  - 감정(긍정/부정) 분석
 
  - 후기를 바탕으로 원하는 것 발견
 
- 소셜 네트워크 분석

  - 사람간의 관계 SNS 상 사용자들 관계 속 영향력 높은 사람 찾기
 
<br>

앙상블 분석
---
### 앙상블
- 여러 개의 예측 모형들을 조합하는 기법으로 **전체적인 분산을 감소**시켜 성능 향상 가능

  - 보팅(Voting)
 
    - 다수결 방식으로 최종 모델을 선택
   
  - 배깅(Bagging)
 
    - 복원추출에 기반을 둔 **붓스트랩**을 생성하여 모델을 학습 후에 보팅으로 결합
   
    - 복원추출을 무한히 반복할 때 특정 하나의 데이터가 선택되지 않을 확률 : **36.8%**
   
  - 부스팅(Boosting)
 
    - 잘못된 분류 데이터에 큰 가중치를 주는 방법, 이상치에 민감
   
    - 종류 : AdaBoost, GBM, XGBoost, Light GBM
   
  - 랜덤포레스트
 
    - 배깅에 의사결정트리를 추가하는 기법으로 **성능이 좋고 이상치에 강한 모델**

<br>
   
#### 💡 보팅, 배깅, 랜덤포레스트는 병렬처리가 가능하며, 부스팅은 병렬처리 불가

<br>

비모수 통계
---
### 비모수검정
- 모집단에 대한 아무런 정보가 없을 때

- 관측 자료가 특정 분포를 따른다고 가정 불가

- 두 관측 값의 순위나 차이로 검정

- **부호검정, 순위합검정, 만-휘트니 U검정, 크러스컬-윌리스 검정**

<br>

