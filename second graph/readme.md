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
##### Microsoft Excel 클릭하여 파일을 불러와준다.
![image](https://user-images.githubusercontent.com/95010590/143829772-54a3b034-6570-4611-b72c-27a38977bc7f.png)

#### (중요!!)데이터를 보면 시간대별로 컬럼이 각각 다 따로 놀고있는데, 나중에 그래프를 그릴때 시간에 대한 정보를 모두 한번에 보여줘야 하므로 '피벗' 기능으로 시간 컬럼들을 모두 묶어준다.
##### 모든 시간 컬럼을 Shift를 눌러서 모두 선택해주고, 우클릭 후 '피벗'을 눌러준다.
![image](https://user-images.githubusercontent.com/95010590/143830389-47d11643-6865-44ab-9ed8-922ef7d44a60.png)
##### 그러면 이렇게 피벗 컬럼으로 시간 컬럼이 모두 묶이게 된다.
![image](https://user-images.githubusercontent.com/95010590/143830530-9136ec70-c27b-494c-a654-cfd9ac403309.png)

##### 이제 데이터 정리가 끝이 났으면, 시트 2로 가준다.
![image](https://user-images.githubusercontent.com/95010590/143830676-b6b7e2c8-8949-4049-a554-540eee54024c.png)

##### 열에 피벗 필드명(시간을 피벗으로 묶은 컬럼), 구분(승차, 하차)으로 넣어주고 행에 역명, 호선, 피벗 필드 값(각 시간대 '인원수' 데이터)를 넣어준다.
![image](https://user-images.githubusercontent.com/95010590/143832435-1128576c-1980-4a34-a74e-41edc05a582b.png)
##### 승차, 하차가 색으로 구분이 되었으면 좋겠다. 마크에 구분을 넣어 색상으로 바꿔준다.
![image](https://user-images.githubusercontent.com/95010590/143832571-22d4bddd-d652-4acd-978e-09075591858f.png)
##### 쨘! 파란색이 승차, 주황색이 하차로 그래프가 구별이 되었다.
![image](https://user-images.githubusercontent.com/95010590/143833131-76386ba1-e9de-400d-b2ae-b46edc688f4a.png)
##### 지저분한 머리글은 없애주도록 하자.
![image](https://user-images.githubusercontent.com/95010590/143833093-0212d8fc-c4aa-4e06-a7d8-b4949e54c654.png)
##### 쨘! 색도 빨간색으로 바꿔주었다.
![image](https://user-images.githubusercontent.com/95010590/143846862-6c5e40f2-1c8c-48d9-8079-0d05f068eb88.png)

### 노선도 위 각 역 좌표안에 그래프 넣어주기
##### 첫번째 시트에서 마크에 도구설명을 눌러준다
![image](https://user-images.githubusercontent.com/95010590/143852999-f8bf9047-3888-4068-b9d4-37069ceb76c9.png)
##### 도구 설명 편집에서 삽입 -> 시트 -> 시트 2를 눌러준다.
![image](https://user-images.githubusercontent.com/95010590/143853214-a68bbe79-b9d2-42ed-a9a7-34e2ab45898f.png)
##### 엔터로 위에 역명과 구분해주고 확인!
![image](https://user-images.githubusercontent.com/95010590/143853357-432bd056-0f83-4c20-b81a-e1e0140eb99b.png)
##### 역위에 마우스를 올리면 뭔가 나오기는 하지만, 뷰가 너무 커서 표시할수 없단다...
![image](https://user-images.githubusercontent.com/95010590/143853525-07aef696-13b6-4fdc-9b9e-89f3ae63e51b.png)
##### 다시 도구 설명으로가서 maxwidth값과 maxheight값을 둘다 1000으로 바꿔준다.
![image](https://user-images.githubusercontent.com/95010590/143853762-6b16a4f3-b35e-4b05-9aa5-b49e7e3daea2.png)
##### 오 정상적으로 그래프가 다 나온다. 
![image](https://user-images.githubusercontent.com/95010590/143853932-2c22d1c9-2d29-40f2-8b9f-686c7efd7137.png)

#### 그다음 역명의 크기도 좀 키우고, 좌표는 딱히 필요가 없는 정보므로 없애버리고, 그 역의 총 승하차인원을 정보로 넣어보자
##### 먼저 도구설명으로 가서, 역명을 이름만 나올수 있게 '역명:'는 지워버리고 <역명>만 남겨주고 글자크기를 20으로 키워준다.
![image](https://user-images.githubusercontent.com/95010590/143854368-60edcfc2-f2cd-4975-9d25-cedf9646aea9.png)
##### 그리고 X,Y 좌표는 없애주고, 잠깐 나가서 위에 데이터 전체호선을 누르고 '피벗 필드 값'을 마크에 추가해준다.
![image](https://user-images.githubusercontent.com/95010590/143854651-541af392-ea12-4a53-8a2d-86dfd355f0d5.png)
#### 그리고 삽입을 누르면 밑에 합계(피벗 필드 값)이 뜨게 된다. 클릭해주자










