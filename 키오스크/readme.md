# ATD 키오스크
<div>
<img src="https://img.shields.io/badge/HTML-E34F26?style=flat-square&logo=HTML5&logoColor=white"/>
<img src="https://img.shields.io/badge/Javascript-F7DF1E?style=flat-square&logo=javascript&logoColor=black"/>
<img src="https://img.shields.io/badge/PHP-777BB4?style=flat-square&logo=PHP&logoColor=white"/>
<img src="https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=MySQL&logoColor=white"/>
</div>

## 목적
- 키오스크 기기에서 담당지역 축산농장 모니터링 및 관리 
- Google, vworld, Kakao, Naver Map 구현

## 기능
### 농장별 최신 상태 모니터링
<div align="center" >
<img src="https://github.com/cjk09083/ATD/blob/main/현장사진/키오스크-1.jpg" width="45%"/>&nbsp;
<img src="https://github.com/cjk09083/ATD/blob/main/키오스크/1.%20농가별현황%20-%20메인.png" width="45%"/>
</div></br>

### 농장의 기상/악취 정보 차트로 출력
<div align="center" >
<img src="https://github.com/cjk09083/ATD/blob/main/키오스크/3.%20농가별현황%20-%20기상%20차트.png" width="45%"/>&nbsp;
<img src="https://github.com/cjk09083/ATD/blob/main/키오스크/3.%20농가별현황%20-%20악취%20차트.png" width="45%"/>&nbsp;
</div></br>

### 농장의 연도별 비교 분석 결과 출력
<div align="center" >
<img src="https://github.com/cjk09083/ATD/blob/main/키오스크/4.%20농가별현황%20-%20데이터%20분석.png" width="45%"/>&nbsp;
<img src="https://github.com/cjk09083/ATD/blob/main/키오스크/4.%20농가별현황%20-%20데이터%20분석2.png" width="45%"/>&nbsp;
</div></br>

### 지도상에 각 농장 위치와 상태 출력
- VWOLRD 지도 활용 => Kakao, Naver Map으로 변경
<div align="center" >
<img src="https://github.com/cjk09083/ATD/blob/main/키오스크/5.%20축산%20지도.png" width="60%"/>
</div></br>


## 주요 문제점 및 해결방법
- Kakao Map 사용시 Kiosk(터치스크린)에서 터치를 인식 못하는 문제 발견</br>
=> User-Agent를 Android로 변경해 모바일기기로 인식하도록 업데이트해서 해결

- Kiosk 서버에서 농장 서버의 데이터를 참조하려고 하니 웹 크로스 도메인 에러(CORS policy) 발생</br>
=> 농장 서버에 Post할때 Ajax(jsonp) + Callback + 파라미터 암호화 를 사용하여 해결
