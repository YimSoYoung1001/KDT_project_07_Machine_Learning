# _KDT05-Machine Learning Project_

경북대학교 KDT(Korea Digital Training) 빅데이터 전문가 양성과정 5기 : ML(Machine Learning) 3팀입니다

임소영 : [깃허브 링크](https://github.com/YimSoYoung1001)  
박희진 : [깃허브 링크](https://github.com/ParkHeeJin00)  
이승민 : [깃허브 링크](https://github.com/winmin94)  
명노아 : [깃허브 링크](https://github.com/noah2397)

![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
![Visual Studio Code](https://img.shields.io/badge/Visual%20Studio%20Code-0078d7.svg?style=for-the-badge&logo=visual-studio-code&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black)
![PyCharm](https://img.shields.io/badge/pycharm-143?style=for-the-badge&logo=pycharm&logoColor=black&color=black&labelColor=green)  
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white)
![SciPy](https://img.shields.io/badge/SciPy-%230C55A5.svg?style=for-the-badge&logo=scipy&logoColor=%white)

<hr/>

#### 개발환경

| 패키지 이름 | 버전   | 사용 커맨드(Version command) |
| ----------- | ------ | ---------------------------- |
| Python      | 3.8.18 | python --version             |
| jupyter     | 1.0.0  | pip show jupyter             |
| ipython     | 8.12.2 | pip show ipython             |
| notebook    | 7.0.6  | pip show notebook            |
| numpy       | 1.24.3 | pip show numpy               |
| pandas      | 2.0.3  | pip show pandas              |
| matplotlib  | 3.7.2  | pip show matplotlib          |
| statsmodels | 0.14.0 | pip show statsmodels         |

<hr/>

### KDT(Korea Digital Training)-ML(Machine Learning)

<hr/>

#### 사용한 데이터 사이트(수정 전)

1. [KBO 홈페이지](https://www.koreabaseball.com/Default.aspx)
2. [Daum 스포츠-야구](https://sports.daum.net/record/kbo/team?season=2023)
3. [구글공유 PPT](https://docs.google.com/presentation/d/1iw8iwN1F_FjeJlKNg46WBwOhtqjZGTJt9zUaESa8WAY/edit)

<hr/>

###### 주제 : 야구 통계 분석

- 목차

* 1. 배경
* 2. (임소영)
* 3. (박희진)
* 4. (명노아)
* 5. (이승민)

###### 역할 분담

|          역할 | 참여인원                       |
| ------------: | ------------------------------ |
|      주제선정 | 임소영, 박희진, 명노아, 이승민 |
|          코딩 | 임소영, 박희진, 명노아, 이승민 |
|          발표 | 임소영, 박희진, 명노아, 이승민 |
|       git관리 | 임소영, 박희진, 명노아, 이승민 |
|   Readme 작성 | 임소영, 박희진, 명노아, 이승민 |
|      PPT 제작 | 임소영, 박희진, 명노아, 이승민 |
| PPT 관리,병합 | 임소영, 박희진, 명노아, 이승민 |

### 소주제 개요(개인 항목)

<details>
  <summary>
    임소영(RandomForest와 Boosting을 활용한 데이터 분석)       
  </summary>

### DecisionTree         
**1. 데이터 전처리 실시**
- 데이터 전처리로 결측치, 중복값, 이상값 확인을 실시했습니다.
- 이상값 제거까지 실시했으나 과대적합의 문제점을 해결하기 위해 복원하였습니다.     

**2. 데이터셋 준비**
- 최고의 성능을 내는 random_state 값 구하기
- STD scaler를 활용한 스케일링 진행

**3. 학습 및 평가**             
- DecisionTree : 과대적합이 발생하여 튜닝 진행
- [ 튜닝1 ] DecisionTree + 파라미터 조정
- [ 튜닝2 ] DecisionTree + GridSearchCV          

**4. 예측값 구하기 및 성능 평가**
- 튜닝을 실시한 2가지 모델에 대해 예측값을 구하고 성능을 평가함
- 성능 평가 요소 (R2 score, MSE, MAE)

**5. 모델 저장 (.pkl 형식)**
- 둘 중 성능이 좋은 '튜닝1'모델을 최종 모델로 저장함

**6. Decision Tree 시각화**
- 저장된 모델에서 decision tree를 시각화 함            


### Boosting

**1. 데이터 전처리 실시**
- 데이터 전처리로 결측치, 중복값, 이상값 확인을 실시했습니다.
- 이상값 제거까지 실시했으나 과대적합의 문제점을 해결하기 위해 복원하였습니다.     

**2. 데이터셋 준비**
- 최고의 성능을 내는 random_state 값 구하기
- STD scaler를 활용한 스케일링 진행

**3. 학습 및 평가**             
- AdaBoostRegressor  |  GradientBoostingRegressor  |  HistGradientRegressor              
- 위 3가지 모델끼리 비교 하여 가장 점수차이가 적고 점수대가 높은 모델 채택함
- 앞서 만든 Decision tree 모델과 boosting 모델을 결합한 모델을 만들었음
- [모델1] GradientBoostingRegressor
- [모델2] Decision Tree + AdaBoostRegressor 
- [모델3] Decision Tree + AdaBoostRegressor + GridSearchCV

**4. 예측값 구하기 및 성능 평가**
- 위 3가지 모델에 대하여 예측값을 구해서 성능평가를 실시함
- 성능 평가 요소 (R2 score, MSE, MAE)

**5. 모델 저장 (.pkl 형식)**
- 셋 중 성능이 좋은 '모델2'를 최종 모델로 저장함
</details>



</hr>

<details>
  <summary>
    명노아(소주제)
  </summary>

</details>

</hr>

<details>
  <summary>
    이승민(소주제)
  </summary>

</details>

</hr>

<details>
  <summary>
    박희진(소주제)
  </summary>

</details>
<hr/>

###### 출처/데이터

| 관련 자료명 | URL |
| :---------: | --- |
