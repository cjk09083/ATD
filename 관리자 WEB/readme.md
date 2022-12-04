# ATD 관리자 페이지 (WEB)
<div>
<img src="https://img.shields.io/badge/HTML-E34F26?style=flat-square&logo=HTML5&logoColor=white"/>
<img src="https://img.shields.io/badge/Javascript-F7DF1E?style=flat-square&logo=javascript&logoColor=black"/>
<img src="https://img.shields.io/badge/PHP-777BB4?style=flat-square&logo=PHP&logoColor=white"/>
<img src="https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=MySQL&logoColor=white"/>
</div>

## 목적 
- 회원, 농장에 관한 모든 정보 관리 
- 농장에 설치된 기기 종류별 (악취측정기/음수투약기/방역인증기/기상측정기/분뇨정보수집기) 관리 페이지 제공

## 기능

### 메인
- 설치/연동/단절 된 농장 정보 요약 표시
<div align="center" >
<img src="https://github.com/cjk09083/ATD/blob/main/관리자%20WEB/1.%20메인.PNG" width="90%"/>
</div></br>


### 장비관리
- 농장에 설치된 기기들의 목록 및 최신 정보 모니터링
<div align="center" >
<img src="https://github.com/cjk09083/ATD/blob/main/관리자%20WEB/2.%20장비관리%20-%20악취측정기.PNG" width="90%"/>
</div></br>

### 데이터목록, 그래프
- 선택한 농장의 상세 데이터 목록 관리
<div align="center" >
<img src="https://github.com/cjk09083/ATD/blob/main/관리자%20WEB/2-2.%20데이터목록%20-%20악취측정기.PNG" width="90%"/>
</div></br>

- 선택한 항목의 기간별 그래프 확인
<div align="center" >
<img src="https://github.com/cjk09083/ATD/blob/main/관리자%20WEB/2-3%20통계%20(온도).PNG" width="90%"/>
</div></br>


### 사용자, 사업장, 지역 관리
- 서버에 등록된 사용자, 사업장, 지역코드 정보를 관리
<div align="center" >
<img src="https://github.com/cjk09083/ATD/blob/main/관리자%20WEB/3.%20사용자관리.PNG" width="90%"/>
</div></br>
<div align="center" >
<img src="https://github.com/cjk09083/ATD/blob/main/관리자%20WEB/4.%20사업장관리.PNG" width="90%"/>
</div></br>

### CS 작업 관리
- 사용자가 WEB 혹은 APP에서 등록한 작업 내역을 관리 
<div align="center" >
<img src="https://github.com/cjk09083/ATD/blob/main/관리자%20WEB/6.%20CS%20관리.PNG" width="90%"/>
</div></br>


### 실시간 데이터
- 원하는 지역별 농장의 실시간 데이터를 모니터링
<div align="center" >
<img src="https://github.com/cjk09083/ATD/blob/main/관리자%20WEB/7.%20실시간데이터.PNG" width="90%"/>
</div></br>

### 지역별 데이터
- vwolrd MAP API를 활용해 농장 위치와 정보를 지도에 표시
<div align="center" >
<img src="https://github.com/cjk09083/ATD/blob/main/관리자%20WEB/8.%20지역별%20데이터%20-%20상세.PNG" width="90%"/>
</div></br>


## 주요 문제점 및 해결방법
- 농장별 최신데이터를 조회할때 농장 데이터가 누적되어있는 원본 DB Table을 Select해 1초 이상의 딜레이가 발생 </br>
=> 농장별 최신데이터만을 저장하는 Temp Table을 생성 후  농장에서 데이터가 업로드될때 Temp Table을 업데이트하도록 변경, 이후 최신 데이터가 필요할땐 Temp table만 조회하도록 하여 딜레이 해결

- 모든 데이터를 조회해서 리스트, 차트를 활성화 후 페이지를 로딩해서 딜레이 발생
=> 빈 페이지를 로딩후 딜레이가 필요한 javscript, php를 비동기로 실행해 이후 리스트와 차트를 로딩  



