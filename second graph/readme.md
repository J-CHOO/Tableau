# 지하철역 요일별 실시간 승차량 정보 서비스
### 처음 계획한 UI(한국철도공사 출처)
![image](https://user-images.githubusercontent.com/95010590/143765308-46b9f4f6-e418-46e0-bc27-ba172c415d57.png)
##### 요일대 별로 시간을 나누어서 사용자가 본인이 원하는 시간의 승차량 정보를 알 수 있게 해준다.

### 우리가 쓸 지하철 노선 이미지
![img_subway](https://user-images.githubusercontent.com/95010590/143765377-debf294e-c18e-4deb-9ba0-2313dd8607d2.png)
##### 여기에 이제 우리가 각 역별로 데이터를 담기 위해서는 노선위에 좌표를 찍어주어야 한다.

### 노선도 위에 좌표 맵핑하기
![image](https://user-images.githubusercontent.com/95010590/143822704-5fb4e7f4-01bd-4730-b71a-b6b892e7ef74.png)
##### 먼저 좌표를 찍기 위해서는 태블로에 배경맵 이미지를 불러와야하는데, 이거도 불러올려면 데이터가 있어야 하므로 일단 이미지파일의 최대 최소 픽셀값을 Sample 좌표값으로 넣어준다.

![image](https://user-images.githubusercontent.com/95010590/143823507-98f672a6-1da0-440f-83be-f84344f37208.png)
##### X를 열에 Y를 행에다가 넣어준후
![image](https://user-images.githubusercontent.com/95010590/143823570-a10123b8-5346-467d-ada5-e059ce171e1c.png)
##### 맵 -> 배경이미지 -> sheet1을 클릭
![image](https://user-images.githubusercontent.com/95010590/143823633-f3ca9926-8983-4ffb-b669-546c68a86e6d.png)
##### 이미지 추가
![image](https://user-images.githubusercontent.com/95010590/143823703-a21e595a-98a5-42c0-962a-345121f7f102.png)
##### 찾아보기 -> 노선도 이미지 열기
![image](https://user-images.githubusercontent.com/95010590/143823816-242bccae-d8f0-4066-a827-394998ef39cc.png)
##### X 오른쪽 : 1086, Y 왼쪽 : 919 입력후 확인
![image](https://user-images.githubusercontent.com/95010590/143824101-4dbbcc03-a759-4ded-b4f8-642f97565498.png)
##### 찍고싶은 역위에 우클릭 후 주석추가 -> 지점을 눌러준 후 확인.
![image](https://user-images.githubusercontent.com/95010590/143824177-20311b6e-fbdb-4912-a697-29188798f4dd.png)
##### 그러면 이렇게 역 위에 좌표가 나오는데 이걸 일일히 엑셀파일에 하나씩 입력해준다.(시간이 좀 많이 든다)
![image](https://user-images.githubusercontent.com/95010590/143824383-fb45119b-c23d-440a-87f8-acb361ed2ae0.png)
##### 이렇게 완성한 노선도 좌표작업 완료!
