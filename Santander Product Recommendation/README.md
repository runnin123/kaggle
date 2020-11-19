https://www.kaggle.com/c/santander-product-recommendation/

## 1. 대회 개요
상품 추천을 받는 산탄데르 은행의 고객은 소수에 불과.   
고객들의 과거 행동 데이터 및 고객 정보 데이터를 통해 머신러닝 알고리즘 적용, 다음 달에 고객이 새롭게 구매할 상품을 예측

## 2. 데이터
1.5년간의 고객 정보 데이터, 보유 상품 데이터   
→ 고객의 2015-01-28 ~ 2016-05-28 기간 동안 고객의 성별, 나이, 거주지 등의 정보 데이터 및 신용카드, 저축계좌 등의 상품 보유 여부를 월별로 기록

### 2-1. 고객 정보 데이터   
fecha_dato 날짜   
ncodpers 고객 고유식별번호   
ind_empleado 고용지표(A: active, B: ex employed, F: filial, N: not employee, P: passive)   
pais_residencia 거주 국가   
sexo 성별   
age 나이   
fecha_alta 첫 계약 날짜    
ind_nuevo 신규 고객 지표(6개월 이내 신규 고객 = 1)   
antiguedad  은행 거래 누적 기간(월)   
indrel 고객 등급(99: 해당 달에 고객 1등급이 해제되는 1등급 고객)   
ult_fec_cli_1t 1등급 고객으로서 마지막 날짜   
indrel_1mes 월초 기준 고객 등급   
tiprel_1mes 월초 기준 고객 관계 유형(A: active, I: inactive, P: former customer, R: potential)   
indresi 거주 지표(S (Yes): 은행 위치 = 거주 국가, N: 불일치)   
indext 외국인 지표(S, N)   
conyuemp 배우자 지표(1: 은행 직원이 배우자)       
canal_entrada 고객 유입 채널   
indfall 고객 사망 여부(S, N)   
tipodom 주소 유형                
cod_prov 지방 코드    
nomprov 지방 이름               
ind_actividad_cliente 활발성 지표    
renta 가구 총수입
segmento 분류(01: VIP, 02: 개인, 03: 대졸)     

### 2-2. 고객 보유 상품 데이터
ind_ahor_fin_ult1 예금   
ind_aval_fin_ult1 보증   
ind_cco_fin_ult1 당좌 예금   
ind_cder_fin_ult1 파생 상품 계좌   
ind_cno_fin_ult1 급여 계정   
ind_ctju_fin_ult1 청소년 계정   
ind_ctma_fin_ult1 마스 특별 계정   
ind_ctop_fin_ult1 특정 계정   
ind_ctpp_fin_ult1 특정 플러스 계정   
ind_deco_fin_ult1 단기 예금   
ind_deme_fin_ult1 중기 예금   
ind_dela_fin_ult1 장기 예금   
ind_ecue_fin_ult1 e-계정   
ind_fond_fin_ult1 펀드   
ind_hip_fin_ult1 부동산 대출        
ind_plan_fin_ult1 연금   
ind_pres_fin_ult1 대출   
ind_reca_fin_ult1 세금   
ind_tjcr_fin_ult1 신용카드   
ind_valo_fin_ult1 증권   
ind_viv_fin_ult1 홈 계정   
ind_nomina_ult1 급여   
ind_nom_pens_ult1 연금    
ind_recibo_ult1 직불 카드

## 3. 평가 척도
MAP@7(Mean Average Precision: 예측 정확도의 평균들의 평균 값)   
→ 한 고객당 최대 7개의 금융 상품을 예측하는 것이 가능   
→ 순서에 영향을 받기 때문에 정답이 앞쪽에 존재하는 것이 더 높은 점수를 받을 수 있음
