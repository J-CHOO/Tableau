# 서울 버스 지역별 승차량 시각화
### (시간대별)
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
##### 마크에 두번째 경도에서 원으로 바꿔준다.
![image](https://user-images.githubusercontent.com/95010590/143989038-874857d9-8e14-4c40-9d00-0eb2d007b7bb.png)
##### 그리고 마크에 지역을 색으로 구분되게 하나 추가해주고, '시간대평균(명)'을 두개 넣어 하나는 크기를 구별할수 있게 크기로 바꿔준다.
![image](https://user-images.githubusercontent.com/95010590/144007623-57cd5f90-047c-46a5-ac9f-bc02118641a2.png)
##### 위에 두번째 경도에서 우클릭하여 이중축을 눌러준다
![image](https://user-images.githubusercontent.com/95010590/144007778-e0f6d3a7-4f41-4952-8ca5-78a722a31182.png)
##### 쨘 이러면 이제 구별로 구분된 지도위에 값이 나오는 원이 올라가게 된다.
![image](https://user-images.githubusercontent.com/95010590/144007977-bbabc390-bf71-4c93-a9c4-15f10bb72d72.png)
##### 원의 크기도 좀 조정해 주고, 옆에 지역 범례는 없애주자.
![image](https://user-images.githubusercontent.com/95010590/144008136-da660e9d-d949-4e95-8f7c-d6003631c7c6.png)
![image](https://user-images.githubusercontent.com/95010590/144008225-6c3be25d-0173-4298-be0a-7df23b85de14.png)
##### 그 다음 필터로 시간대 별로 볼 수있게 만들어주기 위해, 왼쪽에 '시간대'를 필터 자리로 넣어주자.
![image](https://user-images.githubusercontent.com/95010590/144008449-0782a8c5-19c7-4c97-aa7c-2de1b04e7e4b.png)
##### 전체를 눌러준 후 확인!
![image](https://user-images.githubusercontent.com/95010590/144008550-a8251fc0-5488-437e-9b55-22331e73679d.png)
##### 필터에 우클릭 후 필터 표시
![image](https://user-images.githubusercontent.com/95010590/144008611-db885730-24de-4372-90f2-3e54d386f2db.png)
##### 우측에 필터범례에서 세모눌러주고, 단일 값(슬라이더)로 변경해준다.
![image](https://user-images.githubusercontent.com/95010590/144008810-f3844dc0-f286-4591-92ce-e8dcdb6af567.png)
##### 그러면 슬라이더를 왔다갔다 땡길때 마다 원의 크기가 바뀌는걸 확인할 수 있다.
![image](https://user-images.githubusercontent.com/95010590/144008926-ce8b931f-7662-4317-b01a-ae94c7452ece.png)
![image](https://user-images.githubusercontent.com/95010590/144008992-488ea71e-cc0c-4863-8727-bdebb3ab3085.png)
##### 원 안에 숫자가 보이면 더 좋을 거 같아서, 시간대평균을 한번 더 마크에 끌고와서, 레이블로 바꿔준다
![image](https://user-images.githubusercontent.com/95010590/144009133-ca0c7cc6-16ee-4f78-bda7-341109f860a7.png)
##### 그리고 저기 레이블을 눌러서 설정창을 띄워준다.
![image](https://user-images.githubusercontent.com/95010590/144009192-2e605bcd-e7ce-4541-898d-c20692dc52d8.png)
##### 설정창에서 맞춤 -> 세로(가운데)로 설정해준다.
![image](https://user-images.githubusercontent.com/95010590/144009394-49b4ab63-d636-4735-9036-92d54d2af206.png)
##### 첫번째 결과물 완성!!
![image](https://user-images.githubusercontent.com/95010590/144009457-ddf95417-855c-4de9-a57d-9fa902a5f4d5.png)

### 첫번째 이슈 발생(팀원들과 회의후에 팀원들이 원으로 하는거보다는 구별로 구별해놓은 저 지도에 색깔을 넣어서 보여주는게 더 시각적으로 깔끔하고 나아보인다고하여 수정에 들어감)











