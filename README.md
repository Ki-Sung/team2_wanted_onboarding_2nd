# wantedlab Free on Baording Data Analysis Class 2기
<img src="https://user-images.githubusercontent.com/80456601/128636455-a3d15a89-d8f1-4363-94f1-ac9a3e9e9188.png" width="80%" height="50%"/>
2021년 7~8월 원티드(wanted)에서 주관하는 데이터 분석 채용 연계형 프로젝트

### 참가 기업
자비스앤빌런즈, 푸시뉴스, 페이워크

### - 과정소개 
#### 일시: 2021년 07월 31일 ~ 2021년 08월 27일
1. Pre Project 제출 후 선발
2. Week1 수업 및 첫 번째 프로젝트
3. Week2 수업 및 두 번쨰 프로젝트
4. Week3 수업 및 세 번째 프로젝트
5. Week4 채용설명회 및 수료식
---
## 1. Week1 
### Week1 첫 번째 프로젝트
- 주제: 원티드 국민연금 DataBase를 이용해서 유니콘 기업 발굴하기 
- 데이터 출처: 원티드에서 제공한 **'company_nps_data.csv'**
- 프로젝트 발표일: 2021.08.07
- 발표자: 유현준(Team2 팀장)
- 팀원  
  - **유현준 (팀장)**: 데이터 파악 후 EDA, 팀원들의 모든 EDA 결과 취합, 첫 번째 프로젝트 최종 발표  
  - **김기성**: 데이터 파악 후 EDA, 현 유니콘 기업 매출과 직원수 조사, 유니콘 기업 5개 선정
  - **김한빈**: 데이터 파악 후 EDA, EDA 방향 설정
  - **맹광국**: 데이터 파악 후 EDA, 국민연금 세금 계산 기준 조사
  - **박선하**: 데이터 파악 후 EDA, 정규분포를 보이는 컬럼을 스케일링하여 스코어화 구현
  - **정상현**: 데이터 파악 후 EDA, ML 모델링으로 가능한지 파악 
  - **정서현**: 데이터 파악 후 EDA, 성장률 기준 Top10 기업 산출 
  - **최창효**: 데이터 파악 후 EDA, 1인당 매출액과 1인당 연금보혐료를 활용한 점수 계산  
  - **최현숙**: 데이터 파악 후 EDA, 기업 2년이상 유지된 곳, 최소 직원수 40명 이상 기준으로 유니콘 기업 선정
- 자세한 내용: [Ki-sung/wantedlab_free_onboarding/week1_branch](https://github.com/Ki-Sung/wantedlab_free_onboarding/tree/week1)
- 사용한 언어: [![Python Badge](http://img.shields.io/badge/-Python%20-blue?style=flat-square&&logoColor=yellow&logo=python&link=https://www.python.org/)](https://www.python.org/) [![Numpy Badge](http://img.shields.io/badge/-Numpy%20-013243?style=flat-square&&logoColor=white&logo=numpy&link=https://numpy.org/)](https://numpy.org/) [![Pandas Badge](http://img.shields.io/badge/-Pandas%20-150458?style=flat-square&logoColor=white&logo=pandas&link=https://pandas.pydata.org/)](https://pandas.pydata.org/) [![Matplotlib Badge](http://img.shields.io/badge/-Matplotlib%20-2350A9?style=flat-square&logoColor=white&logo=matplotlib&link=https://matplotlib.org/)](https://matplotlib.org/) [![Seaborn Badge](http://img.shields.io/badge/-Seaborn%20-212E50?style=flat-square&logoColor=white&logo=seaborn&link=https://seaborn.pydata.org/)](https://seaborn.pydata.org/) 
### 프로젝트 과정
1. DB구조 파악 및 Column별 검토
2. 분석에 필요한 Column 추가 및 데이터 전처리 
3. 가설 설정 및 검증 
  - 3-1. 가설 설정
    1) 유니콘으로 기대되는 기업은 높은 '성장성'을 나타내는 기업일 것이다.
    2) 유니콘으로 기대되는 기업은 '인적자원'을 중시하는 기업일 것이다.
  - 3-2. 가설 검증 
    1) '성장성'관련 지표: 연매출액 -> 3개의 세부지표 산출 및 점수 계산
    2) '인적자원'관련 지표: 월별 직원수, 인당 평균 연금보혐료
4. 유니콘 기업 최종 선정 
### 프로젝트 결과
1. 유니콘 기업인지 여부를 판단하기 위한 기준을 3년으로 설정 (연매출액 등 지표에 대한 의미있는 변화추이 파악, 중소벤처기업부에서 선정한 거대신생기업의 평균 업력이 3.7년인 점을 고려)
2. 결론 도출을 위해 **"1) 유니콘으로 기대되는 기업은 높은 '성장성'을 나타내는 기업일 것이다.**, **2) 유니콘으로 기대되는 기업은 '인적자원'을 중시하는 기업일 것이다.** 설정
3. 가설 검증을 위해 첫 번째, 연매출액 점수(CAGR, 매출평균 및 지속성장 여부에 따른 "연매출액 점수") 산출 후 설정, 상위 25개의 회사 ID를 추출 
4. 25개 회사 추출 후, 가설 검증을 위해 두 번째, 월별 직원수 기준(최소 직원수 40명 이상, 현존 유니콘 기업 조사 후 참고) 설정, 10개의 회사 ID 추출  (**137755, 470994, 297175, 405759, 403470, 232218, 132156, 127366, 133493, 404804**)
5. 10개 회사 추출 후, 인당 연금보험료 계산 후 최종 5개 유니콘 기업 선정
6. 최종 5개 유니콘 기업은 **127366, 132156, 232218, 297175, 470994**
---
## 2. Week2
### Week2 두 번째 프로젝트
- 주제: Jobis & Villains에서 제공한 데이터로 **1)고객의 결제여부에 영향을 미치는 요인이 무엇인가?**, **2)고객의 수수료 결제금액의 합을 높히기 위해서 어떻게 해야 하는가?** 의 2가지 목표로 프로젝트 진행
- 데이터 출처: 자비스앤빌런스에서 제공한 **'jobis_3o3.csv'**
- 프로젝트 발표일: 2021.08.14
- 발표자: 정상현
- 팀원  
  - **유현준 (팀장)**: 데이터 파악 후 EDA, 전체 Feature간 상관관계 파악, 고객 결제 여부에 따른 특성 비교, 결제여부를 위한 결제비율 지표 산출  
  - **김기성**: 데이터 파악 후 EDA, 자비스앤빌런스 기업조사, 소득 년도별 소득건수와 수수료 결제비율 비교 분석, 상관관계가 있는 Feature들을 위주로 Regression modeling 시도 
  - **정상현**: 데이터 파악 후 EDA, XGB 분류 모델 사용, income 사업 변수 및 소득 데이터 분석, 나이별 데이터로 비교 분석, 두 번쨰 프로젝트 최종 발표 
  - **최창효**: 데이터 파악 후 EDA, 결제여부 기준으로 고객 분류, income 사업 변수 및 소득 데이터 분석
- 자세한 내용: [Ki-sung/wantedlab_free_onboarding/week2_branch](https://github.com/Ki-Sung/wantedlab_free_onboarding/tree/week2)
- 사용한 언어: [![Python Badge](http://img.shields.io/badge/-Python%20-blue?style=flat-square&&logoColor=yellow&logo=python&link=https://www.python.org/)](https://www.python.org/) [![Numpy Badge](http://img.shields.io/badge/-Numpy%20-013243?style=flat-square&&logoColor=white&logo=numpy&link=https://numpy.org/)](https://numpy.org/) [![Pandas Badge](http://img.shields.io/badge/-Pandas%20-150458?style=flat-square&logoColor=white&logo=pandas&link=https://pandas.pydata.org/)](https://pandas.pydata.org/) [![Matplotlib Badge](http://img.shields.io/badge/-Matplotlib%20-2350A9?style=flat-square&logoColor=white&logo=matplotlib&link=https://matplotlib.org/)](https://matplotlib.org/) [![Seaborn Badge](http://img.shields.io/badge/-Seaborn%20-212E50?style=flat-square&logoColor=white&logo=seaborn&link=https://seaborn.pydata.org/)](https://seaborn.pydata.org/) [![Sklearn Badge](http://img.shields.io/badge/-Sklearn%20-F7931E?style=flat-square&logoColor=black&logo=scikit-learn&link=https://scikit-learn.org/stable/)](https://scikit-learn.org/stable/)
### 프로젝트 과정
1. EDA - 각 컬럼 파악 
2. 고객 결제여부에 영향을 미치는 요인과 총 결제금액 합의 개선을 위한 분석 
3. Income 사업 변수 및 소득 데이터 분석 
4. AGE 변수 분석 
5. Refund 변수 분석 
6. Year 변수 분석과 결제금액 총합계 증대방안
### 프로젝트 결과
1. EDA 분석 결과 결제여부는 약한 상관관계가 있는 사업소득 유무를 제외하면, 상관관계가 있는 변수는 없는 것으로 판단, 단 결제금액을 보면 상식적으로 생각하는 것처럼 사업소득, 기타소득, 환급액과 수수료에 상관관계가 존재함을 확인
2. 머신러닝 분류 (XGB 분류) 모델을 통해 지불여부에 대해 데이터 학습하고 feature importance한 결과 여기서 가장 중요한 feature는 사업소득, 나이, 근로소득, 환급액, 기타 소득으로 결과 도출 
3. 최종결과 2020년에 총 결제율과 결제데이터의 수는 크게 하락하였으나 결제금액의 평균값과 총합계가 급증하였고, 2020년에 사업소득이 2,793,000에서 39,934,000 범위(최상위)에 해당하는 고객은 다른해에 비해 약 2.9배 증가하였다.
4. 사업소득 최상위 그룹은 26세 이상 고객의 비율이 다른 사업소득 그룹보다 높고, 남성의 비율이 다른 사업소득 그룹보다 높다, 이 기준에 해당하는 고객이 가장 많이 쓰는 플랫폼에서 해당 그룹을 타게팅하여 마케팅할 경우 결제 금액 총합계의 증대를 예상할 수 있다. (전체 데이터에서도 26세에서 29세사이가 결제금액의 합이 제일 높다.)
### 아이디어 제시 
- 환급액의 2주에서 4주후에 지급된다. 그런데 토스에서 주식을 판 돈을 단기 대출의 개념으로 소정의 이자로 바로 쓸 수 있다. 프리랜서들의 경우 급전이 필요한 경우가 많고, 심리학적으로 금액에 큰 차이가 없다면 대체로 사람들은 돈을 바로 받는 경우를 선호한다. 그러므로, 환급금을 자비스앤빌런즈에서 바로 입금하고 소정의 이자를 결제 창 전에 선택하여 수수료에 추가하는 방향으로 서비스를 추가하면 총 결제 금액의 합을 증대시키는데 도움이 될 것이다. 이때 수수료는 환급금액을 기준으로 고액은 몇 %로 표기하는 것이 심리적 부담이 적을 것이고, 천원 단위 이하의 수수료는 **"2000원만 추가하시면 바로 환급금을 받으실 수 있습니다. 받으시겠습니까?"** 등으로 금액으로 표기하기 하는 것이 결제유도에도 도움이 될 것으로 생각한다. 이때 금액을 설정하면서 AB테스트를 활용하여 조정할 필요가 있다.
---
## 3. Week3
### Week3 세 번째 프로젝트 <해당 과정에 참여했던 회사 "푸쉬뉴스"와 "페이워크"의 참여 포기로 지난 기수에 진행했던 모두의 주차장 프로젝트로 대체>
- 주제: 모두의 주차장 앱 이용자 별 향후 이용건수 예측 
- 데이터 출처: 모두의 주차장 이용 DB
- 프로젝트 발표일: 2021.08.21
- 발표자: 김기성
- 팀원  
  - **유현준 (팀장)**: 데이터 파악 후 EDA, 모델링에 필요한 Feature 설정, MSE와 MAE 점수 도출
  - **김기성**: 데이터 파악 후 EDA, 모두의 주차장 어플 서비스와 기업조사, 각 컬럼 데이터 EDA, 탐색한 컬럼을 연결하여 분석, 세 번쨰 프로젝트 최종 발표
  - **정상현**: 데이터 파악 후 EDA, XGB 분류 모델 시도, MAE, MSE 점수 도출, Feature importance를 바탕으로 코호트 분석 시도
  - **최창효**: 데이터 파악 후 EDA, 주 데이터와 외부데이터 분석 후 merge, model baseline 설정(날짜와 요일별로 이용량이 달라질 것이다.), MSE, MAE 점수 도출
- 자세한 내용: [Ki-sung/wantedlab_free_onboarding/week3_branch](https://github.com/Ki-Sung/wantedlab_free_onboarding/tree/week3)
- 사용한 언어: [![Python Badge](http://img.shields.io/badge/-Python%20-blue?style=flat-square&&logoColor=yellow&logo=python&link=https://www.python.org/)](https://www.python.org/) [![Numpy Badge](http://img.shields.io/badge/-Numpy%20-013243?style=flat-square&&logoColor=white&logo=numpy&link=https://numpy.org/)](https://numpy.org/) [![Pandas Badge](http://img.shields.io/badge/-Pandas%20-150458?style=flat-square&logoColor=white&logo=pandas&link=https://pandas.pydata.org/)](https://pandas.pydata.org/) [![Matplotlib Badge](http://img.shields.io/badge/-Matplotlib%20-2350A9?style=flat-square&logoColor=white&logo=matplotlib&link=https://matplotlib.org/)](https://matplotlib.org/) [![Seaborn Badge](http://img.shields.io/badge/-Seaborn%20-212E50?style=flat-square&logoColor=white&logo=seaborn&link=https://seaborn.pydata.org/)](https://seaborn.pydata.org/) [![Sklearn Badge](http://img.shields.io/badge/-Sklearn%20-F7931E?style=flat-square&logoColor=black&logo=scikit-learn&link=https://scikit-learn.org/stable/)](https://scikit-learn.org/stable/)
### 프로젝트 과정
1. 모두의 주차장 어플과 서비스 소개 
2. 데이터 탐색과 EDA 
3. 모델링 구축 및 검증 
4. 마무리 및 개선점
5. 느낀점
### 프로젝트 결과 
1. 가입일을 살펴본 결과 가입자수는 꾸준히 증가하고 있다.
2. D_TYPE의 정보를 파악해본 결과 USER ID와 1대1로 매칭이 되어 해당 데이터는 User와 관련된 고객 등급이지 않을까 추측 된다.
3. Goods_Type도 파악해본 결과 결제일과 1대N으로 매칭되어 해당 데이터는 주차 이용권 정보로 추측이 된다. 
4. 결제 날짜별 요일별 데이터와 Goods_type에 따라 데이터가 유의미해 보인다.
5. 결제 요일별 Goods_type은 각 타입마다 다르다, A타입은 주말의 사용빈도가 높고, B타입은 금요일의 사용이 높다.
6. LabelEcoding과 OnehotEncoding 후 MSE, MAE 점수가 각각 0.054, 0.083으로 결과가 도출되었다.
### 개선점 과 느낀점
1. 이번 프로젝트 발표가 EDA중심으로 진행이 되었다. 모델링 분석과 코호트 분석이 부재하여 논리적인 분석과 추후 액션플랜이 부재, 이를 보강해야 함.
2. 정확한 모델링 구축에 실패하였다. 모델링에 사용하는 선형회귀, 랜덤포레스트 등 어디에 적용을 해야하는지 사전지식이 부족함, 예측 모델링 분석에 필요한 사항의 공부가 필요
