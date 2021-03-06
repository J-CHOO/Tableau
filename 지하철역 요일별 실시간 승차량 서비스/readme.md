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
##### Microsoft Excel 클릭하여 '전체호선'파일을 불러와준다.
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
##### 그리고 삽입을 누르면 밑에 합계(피벗 필드 값)이 뜨게 된다. 클릭해주자
![image](https://user-images.githubusercontent.com/95010590/143855098-5e65fab0-ec46-44da-b69a-2defa3e6f255.png)
##### 마지막으로 앞에 "역 전체 이용객수 :"를 붙여주고 확인
![image](https://user-images.githubusercontent.com/95010590/143855216-24d7c9ad-4600-4014-8bdc-83239ca78cd2.png)
##### 쨘!훨씬 깔끔해졌다
![image](https://user-images.githubusercontent.com/95010590/143855343-ff78541e-6a8a-4d95-96cd-3ea0bab06b37.png)

### 요일별로 구분하기(필터)
##### 다시 2번째 시트로 간다.
![image](https://user-images.githubusercontent.com/95010590/143855586-ca138439-8386-4901-8c2a-9c91fa2510c9.png)
##### 요일 별로 구분하기 위해서 '요일'을 필터에 넣는다.
![image](https://user-images.githubusercontent.com/95010590/143855726-a4791118-4ffa-453e-881f-7007725fe402.png)
##### 그러면 필터가 뜨게 되는데, 전체를 선택하고 확인 눌러준다.
![image](https://user-images.githubusercontent.com/95010590/143855848-06f5af34-6733-41bc-a1a5-8947d661c90d.png)
##### 이렇게 왼쪽에 필터가 뜨면 우클릭 후 필터 표시를 눌러준다.
![image](https://user-images.githubusercontent.com/95010590/143855976-6dc1f775-34f8-47d1-9e61-c4a709584593.png)
##### 옆에 오른쪽에 필터 범례가 뜨면 저기 세모를 눌러준다.
![image](https://user-images.githubusercontent.com/95010590/143856619-f66a09a7-5721-4cd7-9ccc-2351177fa686.png)
##### 단일 값(목록)으로 바꿔준다.
![image](https://user-images.githubusercontent.com/95010590/143856507-17cea753-fd42-47d1-9522-80bbf60f4602.png)
##### 이제 요일별로 선택하여 그래프를 볼 수 있게 되었다.
![image](https://user-images.githubusercontent.com/95010590/143856737-d7cf64cb-a1f8-457f-bf48-a48ee9e56b13.png)
![image](https://user-images.githubusercontent.com/95010590/143856776-db5be1a3-6b33-4544-99bd-821ec59856cd.png)

### 첫번째 이슈!!(실시간 요일 적용)
#### 팀원들과 회의를 하던 중, 우리가 노선도에 마우스를 올렸을때 당일에 해당하는 요일을 실시간으로 바로 적용해서 보여주는게 더 좋겠다고 말이 나왔다. 그래서 계속 고민을 하던 중 태블로 자체에서 이용할 수 있는 계산필드를 이용하기로 했다.

### 조건식을 걸어서 요일을 구분하기
##### 요일에서 우클릭, 만들기 -> 계산된 필드를 클릭한다
![image](https://user-images.githubusercontent.com/95010590/143857392-82cfd4c3-2e6f-4831-9839-b96706ea7572.png)
##### 함수설명
![image](https://user-images.githubusercontent.com/95010590/143857824-58e88073-6c95-498c-87b9-470634d0765c.png)
![image](https://user-images.githubusercontent.com/95010590/143857953-7ef9835c-e1c7-458b-b978-95f9f071d580.png)
![image](https://user-images.githubusercontent.com/95010590/143858021-bcf92e11-b425-49fc-8051-a2e8ea2746d3.png)
##### (여러가지 시도를 해봤었는데, 내가 현재 작업하고 있는 로컬의 시간과 태블로 서버의 시간이 달라서 로컬과 웹이 결과가 계속 다르게 나왔었다. 우리는 태블로 퍼블릭 서버에 저장해서 웹페이지를 가져다 쓸거였기 때문에 서버시간에 맞춰줘야 우리가 생각하는 결과물이 나왔기에 DATEADD함수로 서버시간에서 9시간을 더해 한국시간과 맞춰주었었다.)
##### 이렇게 함수식을 작성하여 해당 요일에 맞는 숫자를 나오게 해서 해당 요일만 필터에 적용되도록 하였다.(IF식이 끝난 후에는 꼭 END를 붙여줘야한다!!)
![image](https://user-images.githubusercontent.com/95010590/143858536-835ec690-33ee-44f6-bab8-5fbd549af57d.png)
##### 계산 필드를 만들어 준후 옆에 필터를 전체로 맞춰준후
![image](https://user-images.githubusercontent.com/95010590/143858744-ba7dcf00-c677-47c1-a9e5-acc33a84dac9.png)
##### '오늘요일필터'를 필터로 요일 위쪽에 갖다 넣어준다.
![image](https://user-images.githubusercontent.com/95010590/143858905-37c9923c-c25b-4e45-8820-57395ced21ca.png)
##### 참으로 체크 후 확인!!
![image](https://user-images.githubusercontent.com/95010590/143859286-77475785-4a2a-4055-bc68-28ea59731ba3.png)
##### 해당 요일로 그래프가 나오게 설정이 되었다.
![image](https://user-images.githubusercontent.com/95010590/143859375-f4c819a2-2648-4474-87c9-d66816dc763d.png)
### 마무리 디자인작업
##### 피벗 필드 값으로 나오는 지저분한 머리글도 지워주고, 역명도 아까 도구설명에서 표시가 되었으니 지워주도록 한다.
![image](https://user-images.githubusercontent.com/95010590/143859616-c6221298-a788-46f2-819b-028ec4750f4f.png)
![image](https://user-images.githubusercontent.com/95010590/143859654-58e5f59e-884c-4130-8fab-84cabf1b613b.png)
![image](https://user-images.githubusercontent.com/95010590/143859697-3b12350a-042b-4119-9cee-291b51e4d1c2.png)
##### 시트 1에 저 숫자축도 필요가 없으므로 위아래 다 없애준다.
![image](https://user-images.githubusercontent.com/95010590/143859968-81d6305f-3a03-41d1-9b47-23543a6c960d.png)
##### 밑에 승..,하..로 나오는게 좀 짤리므로 별칭을 바꿔준다.
![image](https://user-images.githubusercontent.com/95010590/143860103-5fd9bcf8-26fd-4f93-a587-cb69f1d3b73d.png)
##### 시트 2번으로 가서 오른쪽에 승차, 하차라고 나오는 범례, 승차를 눌러주고 세모클릭 -> 별칭 편집에 들어가준다.
![image](https://user-images.githubusercontent.com/95010590/143860340-d704c28a-b41a-4a87-ac66-455992ce233e.png)
##### 별칭 편집에서 '승'이라고만 적어준다. (하차도 똑같이)
![image](https://user-images.githubusercontent.com/95010590/143860477-12191052-845c-4634-af17-1660a5a0059f.png)
##### 그리고 '06:00 이전' 컬럼이 젤 왼쪽으로 가야하므로 꾹 눌러서 젤 왼쪽으로 옮겨준다.
![image](https://user-images.githubusercontent.com/95010590/143860693-e1ca3f77-35ad-4178-b350-748b433d625e.png)

### 최종완성본
![image](https://user-images.githubusercontent.com/95010590/143860772-499b4f24-046a-4781-85b7-48a167488437.png)
https://public.tableau.com/app/profile/.20303103/viz/6_16372981661790/1










