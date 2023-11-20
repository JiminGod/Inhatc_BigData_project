# 스팀 게임 데이터 분석
```
kaggle에서 받은 Game Recommendations on Steam의 데이터 셋을 이용하여 데이터 분석 및 시각화를 진행하였습니다.
```

## 분석한 내용
1. 연도 별 릴리즈된 게임의 수 증가확인
2. 운영 체제 호환성 비교
3. 할인율에 따른 가격 시각화
4. 스팀덱 호환성 여부
5. 가격 분포 시각화
6. 리뷰어들의 추천게임 비율 (전체게임으로 분석)
7. 유저별 활동과 리뷰 수 관계 분석
8. 리뷰가 많은 게임들의 추천 비율
```
8-1. 리뷰수가 많은 상위 15개의 게임의 is_recommended 수치
8-2. 게임별 리뷰를 남긴 유저들의 플레이 시간 합
8-3. 각 게임들의 연도별 리뷰수 추이
```


## 데이터 셋 구성
- games.csv
```
   app_id                              title date_release   win    mac  linux  \
0   13500  Prince of Persia: Warrior Within™   2008-11-21  True  False  False   
1   22364            BRINK: Agents of Change   2011-08-03  True  False  False   
2  113020       Monaco: What's Yours Is Mine   2013-04-24  True   True   True   
3  226560                 Escape Dead Island   2014-11-18  True  False  False   
4  249050            Dungeon of the ENDLESS™   2014-10-27  True   True  False   

          rating  positive_ratio  user_reviews  price_final  price_original  \
0  Very Positive              84          2199         9.99            9.99   
1       Positive              85            21         2.99            2.99   
2  Very Positive              92          3722        14.99           14.99   
3          Mixed              61           873        14.99           14.99   
4  Very Positive              88          8784        11.99           11.99   

   discount  steam_deck  
0       0.0        True  
1       0.0        True  
2       0.0        True  
3       0.0        True  
4       0.0        True  
(50796, 13)
```
- users.csv
```
    user_id  products  reviews
0   7089523       359        0
1  13509147       156        1
2   8443010       329        4
3   4631165       176        3
4   4967668        98        2
(13784085, 3)
```
- recommendations.csv
```
    app_id  helpful  funny        date  is_recommended  hours  user_id  \
0   975370        0      0  2022-12-12            True   36.3    49618   
1   304390        4      0  2017-02-17           False   11.5     2482   
2  1085660        2      0  2019-11-17            True  336.5   243365   
3   703080        0      0  2022-09-23            True   27.4   248653   
4   526870        0      0  2021-01-10            True    7.9    22898   

   review_id  
0          0  
1          1  
2          2  
3          3  
4          4  
(38347614, 8)
```
