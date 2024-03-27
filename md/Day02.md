## 2일차 학습
- 빅데이터 학습

### 빅데이터 학습

#### 데이터 분석 기초 (Day01 ~)

##### Pandas 학습 (Day01 ~)

2. Pandas 내용 통합(merge, concat) 

    ![concat결과](https://github.com/king-dong-gun/python_bigdata_analyze/assets/160683545/440c879a-468d-467a-8489-4f058e336a60)

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

#### MAC OS seaborn ssl 인증문제 확인
```python
URLError: <urlopen error [SSL: CERTIFICATE_VERIFY_FAILED] certificate verify failed: unable to get local issuer certificate (_ssl.c:1000)>
```
이라는 인증 문제가 나타난다.
```shell
1. Finder에서 사용하고 있는 파이썬 파일 찾기
2. 파이썬 파일 내의 'install Certific Command' 파일 클릭
3. 터미널이 실행되면서 파이썬 인증서 설치
4. 설치 완료 후 VS Code 다시 실행하고 모두 실행
5. 해결!!!!
```

#### Selenium
- 웹브라우저 제어 라이브러리
- 크롬 드라이버 필수

    1. 현재 크롬 브라우저 버전 확인 
    
    ![현재 크롬 브라우저 버전 확인](https://github.com/king-dong-gun/python_bigdata_analyze/assets/160683545/6de21831-d269-4b90-88ca-72118d009fdc)

    2. https://googlechromelabs.github.io/chrome-for-testing/#stable 버전에 맞게 설치


    
    
    3. 연동확인 
    
    
    ![셀리니움 연동 확인](https://github.com/king-dong-gun/python_bigdata_analyze/assets/160683545/811a5163-8bfc-4c14-9a53-863b3dcc17c7)


```python
from selenium import webdriver
## 웹드라이버에서 크롬을 실행
driver = webdriver.Chrome()
```


