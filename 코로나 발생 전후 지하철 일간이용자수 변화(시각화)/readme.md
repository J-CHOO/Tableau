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

##### 크기를 클릭! 사이즈 조절! -> 오 이제 각 차이가 큰역은 확실히 좀 보이기 시작했다.
![image](https://user-images.githubusercontent.com/95010590/143678025-934d07b3-a0a5-4d64-9683-a29ed01362e9.png)

### 첫번째 이슈발생(노선에서 호선명 A,B...로 구분된 가지 노선의 처리가 되지 않았다(2호선을 누르면 전부 다 보여야하는데 따로따로 보임))
![image](https://user-images.githubusercontent.com/95010590/143678170-1793de56-6489-49f6-92f2-12eeaca2dda9.png)
![image](https://user-images.githubusercontent.com/95010590/143678182-5fdad866-b180-4f95-b198-48158681d2d9.png)

### 가지노선 그룹화 작업(가지노선들을 메인노선의 이름만으로 보여지게 처리)
##### sub노선명을 우클릭 후 만들기 -> 그룹으로 들어간다
![image](https://user-images.githubusercontent.com/95010590/143678289-7f3991d4-2cfd-4d91-b7a4-3808dc6d877d.png)
##### Ctrl을 누른후 가지노선들을 모두 선택하여 그룹을 누른다
![image](https://user-images.githubusercontent.com/95010590/143678338-21a28612-4292-44be-8510-65b4b83840d3.png)
##### 그룹화명 부분에 메인노선의 이름을 적은 후 확인(1호선 말고 다른 노선들도 동일하게 작업)
![image](https://user-images.githubusercontent.com/95010590/143678385-69e39325-acbb-469f-a3de-7f2c67383894.png)

##### 자 이제 다시 마크를 바꿔보도록 하자. 첫번째 Lng부터 (중요!!) Sub노선명(그룹)은 색상만 적용이 되면 되므로 꼭 색상만 그룹으로 바꿔주도록한다
![image](https://user-images.githubusercontent.com/95010590/143678857-0b416b78-1f07-492f-8f11-17fb0d8128c8.png)
##### 두번째 Lng도 Sub노선명(그룹)으로 바꿔주도록한다.
![image](https://user-images.githubusercontent.com/95010590/143678884-6b22adc1-70a1-4672-a0f2-e18d300383c7.png)
##### 첫번째 이슈 해결!!
![image](https://user-images.githubusercontent.com/95010590/143678986-e75cf916-12c1-4516-b78a-8da84a3b4335.png)

### 두번째 이슈발생(환승역에서는 데이터가 원이 두개로 보인다.)
![image](https://user-images.githubusercontent.com/95010590/143679023-47a3a164-208c-4bc6-b776-4241de3ea79c.png)
##### 두번째 Lng 마크에서 합계(일간이용자수)에 우클릭-> 측정값을 평균으로 바꿔준다. (환승역에서 서로 다른 노선에 대해 평균으로 합쳐버린다)
![image](https://user-images.githubusercontent.com/95010590/143679096-dae305b2-18b7-428b-93a9-f69298445056.png)
##### 두번째 이슈 해결!!
![image](https://user-images.githubusercontent.com/95010590/143679112-bf5df2e8-c9fd-4309-b95d-aff197b22213.png)
### 디자인 작업
##### 맵 -> 배경맵 -> 일반으로 바꿔서 강도 보이고 좀더 지도를 컬러풀하게 바꿈
![image](https://user-images.githubusercontent.com/95010590/143679128-a149ea42-111a-47c6-99b4-f602727161ff.png)
##### 첫번째 Lng 마크에서 라인 크기를 조절하여 노선이 더 두드러지게 수정
![image](https://user-images.githubusercontent.com/95010590/143679164-889c77c1-ceb8-4c91-97ae-658e64c3d516.png)
##### 각 지하철 별로 색상을 맞춰준다.
##### 노선명 범례에서 우클릭 후 색상 편집
![image](https://user-images.githubusercontent.com/95010590/143679200-0a9b9e2c-25d9-495e-93d1-a4a5fe380790.png)
##### 색상적용 후 확인!!
![image](https://user-images.githubusercontent.com/95010590/143679218-79ea0fe5-55ca-4890-90e7-83395721b012.png)
### 첫번째 결과물
![image](https://user-images.githubusercontent.com/95010590/143679233-e483807d-ae6d-4740-a400-f7d4a0471c37.png)

### 세번째 이슈 발생(팀원들과 회의 후 일간 이용자 수 차이가 크게 보이는 역은 애초에 원래 사람이 많은 역이니까 차이가 당연히 큰게 아니냐는 문제를 제기, 그래서 이용자 변화율로 데이터를 변경하기로 했다.)

### 전처리 완료한 두번째 데이터 형태
![image](https://user-images.githubusercontent.com/95010590/143679544-ba85ddd3-edeb-410a-91ec-a3d8a9e8d287.png)

##### 위에 했던 과정을 똑같이 해서 데이터를 이용자변화율로 변경
![image](https://user-images.githubusercontent.com/95010590/143679651-12c1c5ca-159a-421a-ab0c-1494a3086470.png)

##### 각 역의 값의 변화 차이를 보기 위해 이용자변화율(평균)을 마크에 색상으로 하나 더 추가해주자
![image](https://user-images.githubusercontent.com/95010590/143679729-0a61c08d-61b5-4706-93c4-1432c6783605.png)

##### 변화율이 큰 값(많이 증가 했거나, 많이 감소했거나)은 원이 더 크게 보이게 하고싶다. 빨간게 잘 보이지가 않는다...
![image](https://user-images.githubusercontent.com/95010590/143679862-82c1ec8d-562f-4109-ad86-a6993e6f7438.png)

##### 평균(이용자변화율) 범례에서 크기 편집을 누른다 
![image](https://user-images.githubusercontent.com/95010590/143679929-80d9f0d7-7807-4e18-9832-81b3e2bd10af.png)

##### 크기 범위에서 '0에서' 클릭후 확인!
![image](https://user-images.githubusercontent.com/95010590/143679949-955f5c6a-811d-492a-8ac0-71e8a62df84d.png)

##### 이제 변화율이 큰 역은 명확히 보이기 시작했다!!
![image](https://user-images.githubusercontent.com/95010590/143680015-9a24d1a5-6c2e-4e1d-8b4b-b8cf7b457636.png)

##### 최종 완성본!!
![image](https://user-images.githubusercontent.com/95010590/143680030-e837b488-5e26-493a-abb6-92f31080e21e.png)
https://public.tableau.com/app/profile/.20303103/viz/4_16375655339720/1






