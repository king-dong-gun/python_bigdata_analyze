## 2일차 학습
- 빅데이터 학습

### 빅데이터 학습

#### 데이터 분석 기초 (Day01 ~)

##### Pandas 학습 (Day01 ~)

2. Pandas 내용 통합(merge, concat) 
    ![concat결과]()

3. Pivot 테이블


##### Pandas 2.0 이상 문제 확인
- 두 데이터를 합치기 위한 append() 함수 제거됨
    - https://pandas.pydata.org/docs/whatsnew/v2.0.0.html

- pd.concat() 함수로 대체

#### Numpy
행렬이나 다차원 배열을 쉽게 처리할 수 있도록 도와주는 계산관련 라이브러리, 사용빈도는 낮음
Scipy는 과학쪽에 특화된 계산관련 라이브러리
- DF에서 수치적으로 처리할 항목을 numpy로 변경한 다음, 계산 처리 후 다시 DF로 변경

#### Matplotlib / Seaborn
Matplotlib, Seaborn은 데이터 시각화 라이브러리
- Matplotlib >> 기본
- Seaborn >> Matplotlib 확장버전