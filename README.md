# SmartValve
<div>
<img src="https://img.shields.io/badge/Arduino-00979D?style=flat-square&logo=Arduino&logoColor=white"/>
<img src="https://img.shields.io/badge/HTML-E34F26?style=flat-square&logo=HTML5&logoColor=white"/>
<img src="https://img.shields.io/badge/Javascript-F7DF1E?style=flat-square&logo=javascript&logoColor=black"/>
<img src="https://img.shields.io/badge/PHP-777BB4?style=flat-square&logo=PHP&logoColor=white"/>
<img src="https://img.shields.io/badge/MySQL-4479A1?style=square-square&logo=MySQL&logoColor=white"/>
</div>

## LoRa 통신기반 자가발전형 원격 수로 모니터링 시스템

<div align="center">
<img src="https://github.com/limdongsun0814/SmartValve/assets/118763659/a58dff5a-1be6-4e09-b170-86d9c80c4e69" width="53%"/>&nbsp;  
<img src="https://github.com/limdongsun0814/SmartValve/assets/118763659/04c9fd51-edb8-4b6f-8368-300c43f5a145" width="45%"/>
</div></br>


## 목적
- 수로에 흐르는 물을 이용해 자가발전 
- 수로와 게이트웨이 간의 LoRa를 사용해 연결하고 데이터 송수신 하는 시스템 
- 수로의 상태를 홈페이지에서 모니터링하고 원격 제어 및 고장 판별

## 담당 
- 아두이노의 수로 모터 제어와 센서(유량, 압력, 온도) 정보 유선 통신(RS485)
- LoRa 무선 통신(LoRa)
- KC 인증 (전자파적합성인증 - 한국전자통신연구원)
- 회로 설계 (PSIM)

## 기능

### 1. 수로에서 흐르는 물로 발전기를 돌려 아두이노와 센서들을 동작시킬 전력 충전
 - 수로 내에 수차와 발전기를 연결, 발생하는 전력을 변환하여 배터리에 충전
<div align="center">
<img src="https://github.com/limdongsun0814/SmartValve/assets/118763659/793a145c-8213-4098-a841-dc5aa5e1eedf" width="40%"/>&nbsp;  
<img src="https://github.com/limdongsun0814/SmartValve/assets/118763659/42afd971-80b2-4a13-9da4-aca0fdf34d1a" width="40%"/>
</div></br>

### 2. 수로에서 측정한 정보를 서버와 연동
 - 수로에 설치된 아두이노와 사무실에 설치된 아두이노간의 LoRa 통신 연결 (무자격으로 사용 가능한 923.1MHz 대역 사용)
 - 사무실에 설치된 아두이노에서 서버로 정보 업로드 (Wifi HTTP)
 - 홈페이지에서 밸브 OPEN량을 0~100%로 조절하면 통신이 역순으로 수로에 도달해 수로의 수문에 달린 모터 제어 
 
영상) 수로 밸브를 50%-> 1% 로 제어 (사진&영상/밸브 제어 50 to 1.mp4)
<div align="center">
<img src="https://github.com/limdongsun0814/SmartValve/blob/main/%EC%82%AC%EC%A7%84%26%EC%98%81%EC%83%81/%EB%B0%B8%EB%B8%8C_%EC%A0%9C%EC%96%B4_50_to_1.gif" width="70%"/>
</div></br>

### KC 인증 (전자파적합성인증) - 제어보드 / 전자파테스트 / 충격테스트
<div align="center">
 <img src="https://github.com/limdongsun0814/SmartValve/blob/main/%EC%82%AC%EC%A7%84%26%EC%98%81%EC%83%81/%EC%A0%9C%EC%96%B4%EB%B0%95%EC%8A%A4%20%EB%82%B4%EB%B6%80.png" width="30%"/>&nbsp;  
<img src="https://github.com/limdongsun0814/SmartValve/blob/main/%EC%82%AC%EC%A7%84%26%EC%98%81%EC%83%81/%EC%A0%84%EC%9E%90%ED%8C%8C%20%ED%85%8C%EC%8A%A4%ED%8A%B8.PNG" width="30%"/>&nbsp;  
<img src="https://github.com/limdongsun0814/SmartValve/blob/main/%EC%82%AC%EC%A7%84%26%EC%98%81%EC%83%81/%EC%B6%A9%EA%B2%A9%20%ED%85%8C%EC%8A%A4%ED%8A%B8.PNG" width="30%"/>
</div>

### 회로도
![회로도](https://github.com/limdongsun0814/SmartValve/assets/118763659/175d570f-4040-4af7-9296-117ee4b9f90c)
</br>
