# 코로나 19 발생 전후 서울 지하철 일간이용자수차이
### 처음 계획한 UI(대구지하철 예시)
![20211127_173911](https://user-images.githubusercontent.com/95010590/143674536-39c769ce-9a6a-4d8d-be98-13820831f49b.jpg)

### 전처리 완료한 데이터 형태
![데이터 형태](https://user-images.githubusercontent.com/95010590/143674749-138966f1-8f88-45cb-884f-94f8edcc7b31.jpg)

### 테블로에 csv 데이터 넣기
##### 데이터 csv 파일을 끌어다 넣어준다
![파일 넣기](https://user-images.githubusercontent.com/95010590/143674857-8d2d33a8-6eb9-40ea-8966-98cf2c24f52e.jpg)

##### 위도, 경도를 이용해 맵핑을 해야 하므로 Lat,Lng의 데이터 유형을 위도, 경도로 바꿔준다
![20211127_175441](https://user-images.githubusercontent.com/95010590/143674979-dda3a59c-cc48-4a99-ace0-79f0f3eb99ed.jpg)

##### sub노선명을 두번 마크에 끌어다 넣어주고 하나는 색상 구분을 위해 동그라미 부분을 클릭한후 색상으로 바꿔준다 (처음에는 역명으로 그냥 구분해보려 했으나 태블로에서 왼쪽을 기준으로 가장 가까운역을 그냥 이어버려서 라인 모양이 이상하게 나왔다, 그래서 후에 '순번' 데이터를 추가하여 각 노선별 역에 번호를 부여하여 지하철의 노선 형태의 모양을 만들었다.)
![6](https://user-images.githubusercontent.com/95010590/143675227-a81a32e3-653c-4a17-9abb-d64cdfaa819d.jpg)

##### 순번을 경로로 바꿔준후, 오른쪽 마우스 클릭하여 차원으로 변경!!
![7](https://user-images.githubusercontent.com/95010590/143675476-15968c6e-b05b-4378-9d26-7917595de9d7.jpg)
![8](https://user-images.githubusercontent.com/95010590/143675477-d982626b-e6ee-4bd9-ba2e-a3373e3309c1.jpg)\
##### 쨘! 지하철노선 모양 완성
![9](https://user-images.githubusercontent.com/95010590/143675478-27c976af-74c2-4cb5-936a-4ff51419f3fe.jpg)
