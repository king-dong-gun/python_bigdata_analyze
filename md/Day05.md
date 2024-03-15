## 3일차 학습
- 빅데이터 학습

### 빅데이터 학습

#### 데이터 분석 실습

##### 제주도 핫플레이스 웹크롤링 및 분석
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
- 지도 시각화
1. 데이터 불러오기
2. 카카오 OpenAPI 로 장소 검색한 데이터들 엑셀로 저장
3. 인스타그램 크롤링한 정보와 카카오 API로 주소 검색결과정보를 병합(merge)
4. 병합한 데이터를 folium 라이브러리로 지도로 시각화
![제주도 핫플레이스 시각화](https://github.com/king-dong-gun/python_bigdata_analyze/assets/160683545/90ca5c2a-83dd-45e3-b57a-8a09d4f404b3)



##### 스타벅스 입지 분석
- 웹크롤링, 데이터 수집, 지도 시각화, 분석
- 서울 열린데이터 광장 Open  API 서비스로 인구통계 데이터 수집

1. [스타벅스 코리아 웹사이트](https://www.starbucks.co.kr)
2. [열린데이터 광장 OPEN API]((https://data.seoul.go.kr/))



