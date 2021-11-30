#서울 버스 지역별 승차량 시각화
###(시간대별)
#### 전처리 한 데이터
![image](https://user-images.githubusercontent.com/95010590/143970280-25c9a7b6-709e-4744-9b43-2880b33f67e2.png)
##### '버스시간대'데이터를 넣어준다.
![image](https://user-images.githubusercontent.com/95010590/143970404-6d7969d7-c443-4ab3-9483-36551b41fd8b.png)
##### 시트 1로 간 후에 지역에 우클릭 -> 지리적 역할에서 시군구를 클릭!
![image](https://user-images.githubusercontent.com/95010590/143970572-51862bdd-cee2-4cbc-bad7-d270bf248c57.png)
##### 왼쪽에 지역을 마크에 끌어다준다. 근데?! 오른쪽 아래에 보면 '25개의 알 수 없는 항목'이라면서 인식을 하지 못한다. (이유: 지역데이터에서 그냥 강남구라고 되어 있지 않고 서울특별시 강남구라고 나와 있어서 바로 강남구를 인식을 하지 못한다.) 그래서 '25개의 알 수 없는 항목'를 클릭해서 설정을 해준다.
![image](https://user-images.githubusercontent.com/95010590/143972373-f39c547b-aa83-4ac4-b321-ebb5549ca012.png)
##### 위치 편집을 눌러준다.
![image](https://user-images.githubusercontent.com/95010590/143972440-1c8cf755-daf9-47a6-8646-9ba5e4c6d3ca.png)
##### 주/시/도를 서울특별시로 맞춰주고
![image](https://user-images.githubusercontent.com/95010590/143974645-a354e325-4f23-46cc-8caa-26b2a3b880e9.png)
##### 위치 일치를 하나씩 해당구에 맞게 바꿔준다.
![image](https://user-images.githubusercontent.com/95010590/143974722-761b0a64-d261-4c7a-839c-54aa81312f1a.png)
##### 그러면 이렇게 해당 구에 점이 찍히게 된다.
![image](https://user-images.githubusercontent.com/95010590/143974965-3e9bdbec-6fb7-4563-8999-c5e08f652874.png)
##### 마크에서 맵으로 바꿔준다.
![image](https://user-images.githubusercontent.com/95010590/143977060-9d13d1b5-6574-4a1a-8650-be6d629e2654.png)
##### 위에 맵에서 맵 계층을 눌러준다.
![image](https://user-images.githubusercontent.com/95010590/143977147-e5bd5de4-d8f6-4920-b137-8149c12813e3.png)
##### 투명도를 100%로 맞춰주어 서울시 지도 빼고는 다 지워주도록 한다.
![image](https://user-images.githubusercontent.com/95010590/143977218-b3b85a21-6a94-40f6-abf9-7b3187512a3c.png)
##### 지도 색상을 회색으로 바꿔준 후 이제 지도 위에 원으로 승차량을 표현하기 위해 열에 경도를 하나 복사해준다.
![image](https://user-images.githubusercontent.com/95010590/143977412-47a39205-a070-4b44-8c81-9c7549159e33.png)
