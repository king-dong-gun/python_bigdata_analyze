## 3일차 학습
- 빅데이터 학습

### 빅데이터 학습

#### 데이터 분석 실습

##### 제주도 핫플레이스 웹크롤링 및 분석
- 지도 시각화
    - 카카오 API 사용, https://developers.kakao.com/
    1. 위 사이트 들어간 후 회원가입
    2. 내 에플리케이션 >> 에플리케이션 추가하기 
    3. REST API 키 복사
```python
url = f'https://dapi.kakao.com/v2/local/search/keyword.json?query={shopName}'

header = { 'Authorization' : 'myKey'} # 본인 키 사용 // 깃헙 업로드 전 삭제 필요

places = requests.get(url, headers=header).json()['documents']
places
```



##### 스타벅스 입지 분석
- 웹크롤링, 데이터 수집, 지도 시각화, 분석
- 서울 열린데이터 광장 Open  API 서비스로 인구통계 데이터 수집

1. [스타벅스 코리아 웹사이트](https://www.starbucks.co.kr)
2. [열린데이터 광장 OPEN API]((https://data.seoul.go.kr/))



