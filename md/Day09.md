## 9일차 학습
- 빅데이터 학습
    1. OPEN API 기반 크롤링 실습
    2. 통계 분석 리뷰
    3. 머신러닝 실습


#### 데이터 분석 실습

##### OPEN API 기반 크롤링 실습
1. [공공데이터포탈](https://data.go.kr)에서 API 인증키 및 데이터 가져옴
    - 국가 공공기관에서 무료 제공하는 데이터 타입
    - 한국관광공사 관광빅데이터 GW API 사용
        - https://www.data.go.kr/tcs/dss/selectApiDataDetailView.do?publicDataPk=15101972
2. http 프로토콜로 요청해야함, https로 요청하면 ssl 오류발생
    
    ```python
    ## 반복문으로 처리
    korTouristData = []
    year = 2023
    month = 12

    for day in tqdm(range(1, 32)):
        requsetYmd = f'{year}{month}{day:02d}'
        data = getKorTouristData(requsetYmd)
        # 해당 날짜에 데이터가 없을수 있음
        if xmltodict.parse(data)['response']['body']['items'] == None : 
            resultList = []
        else :
            resultList = xmltodict.parse(data)['response']['body']['items']['item']

        korTouristData = korTouristData + resultList
    ```
    100%|██████████| 31/31 [01:22<00:00,  2.66s/it]
3. 가져온 데이터를 dataFrame으로 변환 후 엑셀파일로 저장

![touristData엑셀파일](https://github.com/king-dong-gun/python_bigdata_analyze/assets/160683545/74e0b0b2-8aa5-4dcd-9fca-03bfc76bf8cb)

##### 와인 품질 데이터 통계 분석
1. 데이터 준비
2. 데이터 병합 (ex > 레드와인, 화이트와인 병합)
3. 데이터 탐색
4. 데이터 모델링
5. 결과 시각화


