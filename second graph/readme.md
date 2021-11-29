# 지하철역 요일별 실시간 승차량 정보 서비스
### 처음 계획한 UI(한국철도공사 출처)
![image](https://user-images.githubusercontent.com/95010590/143765308-46b9f4f6-e418-46e0-bc27-ba172c415d57.png)
##### 요일대 별로 시간을 나누어서 사용자가 본인이 원하는 시간의 승차량 정보를 알 수 있게 해준다.

### 우리가 쓸 지하철 노선 이미지
![img_subway](https://user-images.githubusercontent.com/95010590/143765377-debf294e-c18e-4deb-9ba0-2313dd8607d2.png)
##### 여기에 이제 우리가 각 역별로 데이터를 담기 위해서는 노선위에 좌표를 찍어주어야 한다.

### 노선도 위에 좌표 맵핑하기
##### 먼저 좌표를 찍기 위해서는 태블로에 배경맵 이미지를 불러와야하는데, 이거도 불러올려면 데이터가 있어야 하므로 일단 이미지파일의 최대 최소 픽셀값을 Sample 좌표값으로 넣어준다.
![image](https://user-images.githubusercontent.com/95010590/143822704-5fb4e7f4-01bd-4730-b71a-b6b892e7ef74.png)
##### X를 열에 Y를 행에다가 넣어준후
![image](https://user-images.githubusercontent.com/95010590/143823507-98f672a6-1da0-440f-83be-f84344f37208.png)
##### 맵 -> 배경이미지 -> sheet1을 클릭
![image](https://user-images.githubusercontent.com/95010590/143823570-a10123b8-5346-467d-ada5-e059ce171e1c.png)
##### 이미지 추가
![image](https://user-images.githubusercontent.com/95010590/143823633-f3ca9926-8983-4ffb-b669-546c68a86e6d.png)
##### 찾아보기 -> 노선도 이미지 열기
![image](https://user-images.githubusercontent.com/95010590/143823703-a21e595a-98a5-42c0-962a-345121f7f102.png)
##### X 오른쪽 : 1086, Y 왼쪽 : 919 입력후 확인
![image](https://user-images.githubusercontent.com/95010590/143823816-242bccae-d8f0-4066-a827-394998ef39cc.png)
##### 찍고싶은 역위에 우클릭 후 주석추가 -> 지점을 눌러준 후 확인.
![image](https://user-images.githubusercontent.com/95010590/143824101-4dbbcc03-a759-4ded-b4f8-642f97565498.png)
##### 그러면 이렇게 역 위에 좌표가 나오는데 이걸 일일히 엑셀파일에 하나씩 입력해준다.(시간이 좀 많이 든다)
![image](https://user-images.githubusercontent.com/95010590/143824177-20311b6e-fbdb-4912-a697-29188798f4dd.png)
##### 이렇게 완성한 노선도 좌표작업 완료!
![image](https://user-images.githubusercontent.com/95010590/143824383-fb45119b-c23d-440a-87f8-acb361ed2ae0.png)

### 좌표 적용 후 노선도
##### 위에서와 똑같이 X, Y값을 넣어준 후 배경맵 이미지 적용한 후 마크에 역명을 넣어주게 되면 이렇게 우리가 원하는 역에 좌표값이 들어가게 된다.
![image](https://user-images.githubusercontent.com/95010590/143826064-096e610c-0af7-4e44-a995-8a019d91bb25.png)
##### 원크기가 좀 크므로 살짝 줄여준다
![image](https://user-images.githubusercontent.com/95010590/143826310-1ddbf198-2759-4d27-b1a0-89e0d7798d0d.png)

### 지하철역 요일별 시간에 따른 승하차수 그래프 그리기
#### 전처리 완료한 데이터(지하철역 요일별 시간에 따른 승하차수 데이터)
![image](https://user-images.githubusercontent.com/95010590/143829145-97c2df81-c50b-42dd-856e-c39d2b51e6e5.png)

##### 새 시트를 추가해준다.
![image](https://user-images.githubusercontent.com/95010590/143829268-c45c98af-be81-4239-b385-debaf7941a35.png)
##### 데이터를 새로 또 추가해야 하므로, 위에 데이터 -> 새 데이터 원본을 눌러준다.
![image](https://user-images.githubusercontent.com/95010590/143829385-69393dea-041f-4ffb-9ff4-ab78c6386baa.png)





