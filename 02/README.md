# 📍 데이터분석 계획
# 1. 분석 방안 수립
분석 로드맵 설정
---
### 분석 대상과 방법
|방법\대상|Known|UnKnown|
|-|:-:|:-:|
|Known|**최적화<br>(Optimization)**|**통찰<br>(Insight)**|
|UnKnown|**솔루션<br>(Solution)**|**발견<br>(Discovery)**|

<br>

### 분석 기획 방안
|-|과제 중심적 접근|장기적 마스터 플랜|
|:-:|:-:|:-:|
|목적|**빠르게** 해결|**지속적 분석 원인** 해결|
|1차 목표|Speed & Test|Accuracy & Deploy|
|과제 유형|Quick & Win|Long Term View|
|접근 방식|Problem Solving|Problem Definition|

<br>

### 의사결정을 가로막는 요소
- 고정 관념, 편향된 생각

- **프레이밍 효과**

  - 동일 상황임에도 개인의 판단, 결정이 달라짐
 
<br>

분석 문제 정의
---
### 하향식 접근 방법
- 문제가 주어지고 해답을 찾기 위해 진행

- **문제 탐색** → 문제 정의 → 해결방안 → **타당성 검토**

  - (1) **문제 탐색**
 
    - 빠짐없이 문제를 도출하고 식별하며, 솔루션 초점 보다는 가치에 초점
   
    - 비즈니스 모델 캔버스 단순화 측면
   
      - **업무, 제품, 고객, 규제와 감사, 지원인프라** (*지원인프라 업무* 중에 *고객*이 *제품*을 *규제와 감사* 했다)

    - 관점
   
      - 거시적 관점 : **STEEP** (사회, 기술, 경제, 환경, 정치)
     
      - 경쟁자 확대 관점 : 대체자, 경쟁자, 신규 진입자
     
      - 시장의 니즈 탐색 관점 : 고객, 채널, 영향자
     
  - (2) **타당성 검토**
 
    - 경제적 타당성 : **비용대비 편익** 분석관점 접근
   
    - 데이터 타당성 : **데이터 존재여부, 분석역량** 필요
   
    - 기술적 타당성 : 역량 확보 방안 사전에 수립

<br>

### 상향식 접근 방법
- **문제 정의 자체가 어려**울 때, 사물을 그대로 인식하는 **What 관점**

- 주로 **비지도 학습**

<br>

### 디자인 싱킹
- 사용자에 **공감**으로 시작해서 아이디어 **발산/수렴** 과정을 통한 **피드백**으로 발전하는 과정

- 공감하기 → 문제 정의 → 아이디어 도출 → 프로토타입 → 테스트

<br>

데이터 분석 방안
---
### 분석 방법론의 구성요소
- **절차, 방법, 도구와 기법, 템플릿과 산출물**

<br>

### 분석 과제에서 고려해야할 5가지 요소
- **데이터 크기, 속도, 데이터 복잡도, 분석 복잡도, 정확도/정밀도**

  - 정확도(Accuracy)와 정밀도(Precision)는 **Trade-Off 관계**
 
<br>

### 프로젝트 관리 지식 체계 10가지 영역
- *통*합, *범*위, *시*간(일정), *원*가(비용), *품*질, 인적*자*원, *의*사소통, *리*스크(위험), *조*달, *이*해관계자

  - (*이범통*이 *의자*에서 *시원*한 *조리품*을 먹었다)
 
<br>

### 우선순위 선정
- 전략적 중요도 : 전략적 필요성, 시급성

- 실행 용이성 : 투자 용이성, 기술 용이성

<br>

### ROI 관점
- **시급성** 관점

  - 비즈니스 효과(Retrun) - **Value**
 
- **난이도** 관점

  - 투자비용 요소(Investment) - Volumn, Variety, Velocity

<br>

|ROI 관점|
|-|
|![image](https://github.com/user-attachments/assets/9002d354-edc4-4057-b907-41c18d670fc1)|

- **시급성 중요시 : 3 → 4 → 2**

- **난이도 중요시 : 3 → 1 → 2**

#### 💡 3과 2는 앞 뒤로 고정하고 가운데만 변경

<br>

### 분석 방법론 모델
- 폭포수 모델

  - 이전 단계가 완료되어야 다음 단계 진행 (Top-Down)
 
- 나선형 모델

  - 여러 개발과정 거쳐 점진적으로 완성
 
  - **위험요소 제거** 초점
 
- 프로토타입 모델

  - 일부분(프로토타입)을 우선 개발하고 보완
 
- 애자일

  - **일정한 주기**를 가지고 프로토타입을 **끊임없이 수정**하여 고객의 Needs 반영
 
<br>

### KDD 분석 방법론
- 데이터 선택 → **전처리** → **변환** → 마이닝 → 결과 평가

  - 전처리 : 이상값, 잡음 식별 및 데이터 가공
 
  - 변환 : **변수 선택 및 차원 축소**
 
<br>

### Crisp-DM 분석 방법론 (*업데데*이트*모델평가전*)
- *업*무 이해 → *데*이터 이해 → *데*이터 준비 → ***모델*링** → ***평가*** → *전*개

  - **모델링 단계에서 모델 평가** 수행하고 **평가 과정 단계에서 모델 적용성 평가** 수행
 
  - 평가 → 전개에서 **위대한 실패** 발생 가능
 
<br>

### 빅데이터 분석 방법론 (*PPADD*)
- ***P*lanning (분석기획)** 

  - 비즈니스 이해 및 범위 설정
 
  - 프로젝트 정의 및 계획 수립
 
  - 프로젝트 위험계획 수립 (***회*피, *전*이, *완*화, *수*용**)
 
- ***P*reparing (데이터 준비)**

  - 필요 데이터 정의
 
  - 데이터 스토어 설계
 
  - 데이터 수집 및 정합성 점검
 
- ***A*nalyzing (데이터 분석)** : 추가적인 데이터 확보 필요 시, 데이터 준비 단계로 다시 진행

  - 분석용 데이터 준비
 
  - 텍스트 분석
 
  - 탐색적 분석
 
  - 모델링
 
  - 모델 평가 및 검증
 
  - 모델 적용 및 운영방안 수립
 
- *D*eveloping (시스템 구현)

  - 설계 및 구현
 
  - 시스템 테스트 및 운영
 
- *D*eploying (평가 및 전개)

  - 모델 발전계획 수립
 
  - 프로젝트 평가 및 보고
 
<br>

### 분석 거버넌스 체계 구성요소 (*시조프로마인드데*)
- *조*직, *프로*세스, *시*스템, *데*이터, 분석관련 교육 및 *마인드* 육성 체계

<br>

### 데이터 분석 수준 진단
- **분석 준비도** (*IT문데기인파*)

  - 분석 업무 *파*악
 
    - 사실 분석, 예측, 시뮬레이션, 최적화, 분석 업무 정기적 개선
   
  - 분석 *인*력 및 조직
 
    - 분석 전문가, 관리자, 조직, 경영진 이해
   
  - 분석*기*법
 
    - 적합한 기법 사용, 분석기법 라이브러리/평가/개선
   
  - 분석*데*이터
 
    - 데이터 관리, 외부데이터 활용, 기준데이터 관리(MDM)
   
  - 분석*문*화
 
    - 의사결정, 회의에서 활용, 공유 및 협업 문화
   
  - *IT* 인프라
 
    - 운영 시스템 통합, 환경

<br>

- **분석 성숙도**

  - **CMMI 모델** 기반 (1~5단계) (*도활확최*)
 
    - 비즈니스 / 조직, 역량 / IT 부문 관점으로 구분
   
      - *도*입 : 환경, 시스템 구축
     
      - *활*용 : 업무에 적용
     
      - *확*산 : 전사 차원 관리, 공유
     
      - *최*적화 : 혁신, 성과향상에 기여

<br>

### 데이터 분석 성숙도 모델 (*도준정확* 4사분면부터 시계방향(역순)으로 암기)
|데이터 분석 성숙도 모델|
|-|
|![image](https://github.com/user-attachments/assets/81bf32e3-85ff-4eea-8baa-df12f979c465)|

- *준*비형 : 낮은 준비도, 낮은 성숙도

  - 데이터, 인력, 조직, 분석업무, 분석기법 적용 안되어 사전 준비 필요
 
- *정*착형 : 낮은 준비도, 높은 성숙도

  - 인력, 조직, 분석업무, 분석기법 등을 제한적으로 사용
 
- *도*입형 : 높은 준비도, 낮은 성숙도

  - 조직 및 인력 등 준비도는 높으나, 분석업무 및 기법 부족
 
- *확*산형 : 높은 준비도, 높은 성숙도

  - **6가지 분석 구성요소를 모두 갖추고** 있으며, 지속적 확산 가능

<br>

### 분석 지원 인프라 방안 수립
- 확장성을 고려한 **플랫폼** 구조 적용 (중앙집중적 관리)

<br>

### 데이터 거버넌스
- (1) 데이터 거버넌스

  - 전사 차원에서 데이터에 대해 표준화된 관리 체계 수립
 
  - 구성요소 : ***원*칙, *조*직, *프*로세스**
 
  - 중요 관리대상
 
    - 마스터 데이터 : 자료 처리에 기준이 되는 자료
   
    - 메타데이터 : 다른 데이터를 설명해주는 데이터
   
    - 데이터 사전 : DB에 저장된 정보를 요약
   
- (2) 데이터 거버넌스 체계

  - 데이터 표준화 : 메타데이터 및 사전 **구축**
 
  - 데이터 관리 체계 : **효율성**을 위함
 
  - 데이터 저장소 관리 : **저장소** 구성
 
  - 표준화 활동 : **모니터링, 표준 개선 활동**
 
<br>

### 빅데이터 거버넌스
- 데이터 거버넌스 체계 + 빅데이터 효율적 관리, 데이터 최적화, 정보보호, 데이터 카테고리별 관리책임자 지정 등을 포함

<br>






















