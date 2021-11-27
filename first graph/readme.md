# 코로나 19 발생 전후 서울 지하철 일간이용자수 변화
### 처음 계획한 UI(대구지하철 예시)
![20211127_173911](https://user-images.githubusercontent.com/95010590/143674536-39c769ce-9a6a-4d8d-be98-13820831f49b.jpg)

### 전처리 완료한 데이터 형태
![데이터 형태](https://user-images.githubusercontent.com/95010590/143674749-138966f1-8f88-45cb-884f-94f8edcc7b31.jpg)

### 테블로에 csv 데이터 넣기
##### 데이터 csv 파일을 끌어다 넣어준다
![파일 넣기](https://user-images.githubusercontent.com/95010590/143674857-8d2d33a8-6eb9-40ea-8966-98cf2c24f52e.jpg)

### 좌표 맵핑하여 지하철 노선모양 만들기
##### 위도, 경도를 이용해 맵핑을 해야 하므로 Lat,Lng의 데이터 유형을 위도, 경도로 바꿔준다
![20211127_175441](https://user-images.githubusercontent.com/95010590/143674979-dda3a59c-cc48-4a99-ace0-79f0f3eb99ed.jpg)

##### sub노선명을 두번 마크에 끌어다 넣어주고 하나는 색상 구분을 위해 동그라미 부분을 클릭한후 색상으로 바꿔준다 (처음에는 역명으로 그냥 구분해보려 했으나 태블로에서 왼쪽을 기준으로 가장 가까운역을 그냥 이어버려서 라인 모양이 이상하게 나왔다, 그래서 후에 '순번' 데이터를 추가하여 각 노선별 역에 번호를 부여하여 지하철의 노선 형태의 모양을 만들었다.)
![6](https://user-images.githubusercontent.com/95010590/143675227-a81a32e3-653c-4a17-9abb-d64cdfaa819d.jpg)

##### 역명을 왼쪽 마우스로 꾹 눌러 밖으로 끌어서 없애준후, 순번을 마크에 넣고 경로로 바꿔준후, 오른쪽 마우스 클릭하여 차원으로 변경!!
![7](https://user-images.githubusercontent.com/95010590/143675476-15968c6e-b05b-4378-9d26-7917595de9d7.jpg)
![8](https://user-images.githubusercontent.com/95010590/143675477-d982626b-e6ee-4bd9-ba2e-a3373e3309c1.jpg)
##### 쨘! 지하철노선 모양 완성
![9](https://user-images.githubusercontent.com/95010590/143675478-27c976af-74c2-4cb5-936a-4ff51419f3fe.jpg)

### 역별 지하철 일간이용자수 시각화
##### Lng를 끌어서 열에다가 하나 더 추가해준다
![10](https://user-images.githubusercontent.com/95010590/143675714-80c16574-3814-4318-9049-7fca37003354.jpg)

##### 두번째 Lng의 마크에서 체크표시 되어있는 부분을 눌러 원으로 바꾼다
![11](https://user-images.githubusercontent.com/95010590/143675797-26962152-11f5-4327-95ea-09b606e454d2.jpg)

##### 마크에 역명과 일간이용자수차이를 넣고 각각 레이블과 크기로 바꿔준다
![12](https://user-images.githubusercontent.com/95010590/143677430-ce7db1d2-a463-4dbc-94e0-fa9abb3a0065.jpg)

##### 두번째 Lng에 오른쪽마우스를 눌러 '이중축'을 설정해주면 노선 라인위에 각 역별로 이용자수 차이가 원으로 보여지게 된다
![13](https://user-images.githubusercontent.com/95010590/143677517-2ec0dce6-f89f-4a1e-94e9-ce3567988b6a.jpg)
![14](https://user-images.githubusercontent.com/95010590/143677520-6139b668-6e41-4ef6-a8b4-adacb1a423b7.jpg)

##### 원이 시각적으로 더 잘 보이게 하기위해 색상을 주황색으로, 테두리까지 넣어줬다.
![15](https://user-images.githubusercontent.com/95010590/143677699-b03b143d-92e3-4acf-8c75-ddb67058b2f0.jpg)
![16](https://user-images.githubusercontent.com/95010590/143677703-21dcf702-efd0-4746-acb8-1609e5f52287.jpg)

##### 하지만 원이 아직 이용자수 차이를 확연히 보여주지 않으므로, 차이가 큰 역을 더 돋보이게 하기위해 크기를 조정해준다.
##### 옆에 일간이용자수차이 범례에서 오른쪽마우스를 눌러 크기 편집에 들어간다.
![17](https://user-images.githubusercontent.com/95010590/143677794-05be5622-3fe6-47d8-bc36-4d1e2720ee43.jpg)
##### 크기범위를 0에서부터로 변경해준 후 확인!!
![18](https://user-images.githubusercontent.com/95010590/143677856-74a398c0-b7af-485d-98e8-479ee7f87d73.jpg)
##### 크기가 조절이 되었다. 하지만 좀 작네?!
![19](https://user-images.githubusercontent.com/95010590/143677857-9ec99a71-baf5-4cd4-ba3e-8f2bd42a2c5b.jpg)

##### 오 이제 각 차이가 큰역은 확실히 좀 보이기 시작했다.
![image](https://user-images.githubusercontent.com/95010590/143677978-7289f51f-8168-406b-946e-234471dabd48.png)
