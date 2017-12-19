## 다음의 순서로 시작합니다.

* 1. 회원가입&nbsp;&nbsp;&rarr;&nbsp;&nbsp;2. 로그인&nbsp;&nbsp;&rarr;&nbsp;&nbsp;3. Workspace 이동&nbsp;&nbsp;&rarr;&nbsp;&nbsp;4. Workspace 및 Application 생성


## SKT Asset 목록
- Sketch 에는 아래와 같은 SKT 의 유용한 API 가 쓰기 편하게 내장되어 있습니다. 이를 활용하여 나만의 서비스를 만들어 보세요 


Asset |  상세내용
------|----------
[ThingPlug IoT ](https://sketch.sktiot.com/app/guide/manual/node_thingplug) | IoT Device 로 부터 정보를 가져오거나 명령을 내릴 수 있습니다.
[T map](https://sketch.sktiot.com/app/guide/manual/node_tmap)| 경로 찾기, 주소 좌표 변환 등을 수행 할 수 있습니다.
[BaaS](https://sketch.sktiot.com/app/guide/manual/node_tbaas) | 서버 구축에 필요한 DB를 제공하며 추가로 POI (Points of Interest), File upload 기능을 수행 할 수 있습니다.
[Weather Planet](https://sketch.sktiot.com/app/guide/manual/node_weather) | Weather Planet을 활용하여 날씨 정보를 받아 볼 수 있습니다.
[MQTT](https://sketch.sktiot.com/app/guide/manual/node_mqtt)| Sketch 자체 MQTT 브로커를 통해 Publish/Subscribe 방식의 통신을 사용 할 수 있습니다.
[Variable Node](https://sketch.sktiot.com/app/guide/manual/node_variable) | 작은 단위의 데이트를 빠르게 저장/조회 하는 Key/Value 저장소를 제공합니다.
[SMS Node](https://sketch.sktiot.com/app/guide/manual/node_sms)| Sketch 결과를 SMS/LMS 문자메시지로 보낼 수 있습니다.
[Safe Http](https://sketch.sktiot.com/app/guide/manual/node_safehttp)| 보안을 적용한 Http node로써 Header에 접근 권한 token이 필요합니다.

## SketchSensor App 연동
- Android용 SketchSensor App을 설치하여 Sketch로 Sensor Data를 보낼 수 있습니다.
- Android App은 주기적으로 Sensor Data를 수집해서 Sketch에 JSON 형태로 보냅니다.


## Sketch 작업
- 초기 Application 생성 메뉴에서 **Mobile 센서값 연동** 템플릿을 선택하여 생성합니다.
- 템플릿에서 할 

## App 설치 요구사항 및 권한 사용
- 최소 OS: Android Lollipop 5.0 (API level 21)
- 권한 사용:
  - GPS 위치 권한: 현재 위치 발송 (필수 아님)
  - 마이크 녹음 권한: 소음 측정 (필수 아님)

## App 설치 및 사용 절차
- 먼저 아래 그림과 같이 출처를 알수 없는 앱 설치를 허용합니다.
- 아래 APK Link에서 App을 다운 받은 후 실행하면 먼저 권한체크를 수행하며 동의 없이도 사용 가능합니다.
- 기본적으로 1초 주기로 휴대폰의 센서값을 수집합니다.
- 중앙 SEND Tab으로 이동해서 Sketch 작업장의 Application 도메인을 입력합니다. (예: abc.sketchwork.io)
- 
- 센서 수집 및 Sketch 발송 주기, 팝업 표시 등은 우측 SETTINGS Tab에서 변경 가능합니다.


## T map 개요
- T map을 이용하면 특정주소나 경로를 입력해서 지도에 표시할 수 있습니다.
- 추가로 주소 &rarr; 위도/경도 좌표 변환이나 신/구 주소 변환도 가능합니다.

## T map 이용을 위한 작업
- 먼저 https://developers.skplanetx.com 에서 회원 가입을 합니다. 
- **개발 → 앱 등록 및 키 발급** 메뉴를 통해 사용이 가능하고, 가입시 T map service에 체크 하셔야 합니다.
- App등록이 완료되면 Log in ID &rarr; 마이 앱으로 이동하여 해당 App Key를 확인할 수 있습니다.
- T map 관련 노드에 App Key를 입력하여 좌표변환, 신/구 주소 변환, 지도에 주소 또는 경로 표시를 할 수 있습니다. 


## Weather Planet 개요
- SK Planet의 Weather Planet API를 사용하여 위치기반 날씨 데이터를 쉽게 읽어올 수 있습니다.
- Weather Planet은 고해상도 기상관측망을 통해서 수집된 정보를 바탕으로 날씨정보를 제공하는 서비스입니다.
- Weather Planet Open API를 이용하여 개발자들은 손쉽게 자신의 웹 및 모바일 서비스에 날씨 예보 및 특보 정보 뿐만 아니라 위성, 레이더, 낙뢰, 태풍 등의 지도기반 서비스를 사용자들에게 제공할 수 있습니다.

## Weather Planet 이용을 위한 작업
- https://developers.skplanetx.com 에서 회원 가입 후, **개발 &rarr; 앱 등록 및 키 발급** 메뉴를 통해 API를 사용할 수 있습니다.
- 가입시 Weather Planet Service에 체크 되었는지 확인 하시면 됩니다.
- 먼저 https://developers.skplanetx.com 에서 회원 가입을 합니다. 
- **개발 &rarr; 앱 등록 및 키 발급** 메뉴를 통해 사용이 가능하고, 가입시 Weather Planet service에 체크 하셔야 합니다.
- App등록이 완료되면 Log in ID &rarr; 마이 앱으로 이동하여 해당 App Key를 확인할 수 있습니다.
- Weather Planet 노드에 App Key와 위도/경도 정보만 입력하면 해당 위치의 날씨를 받아 볼 수 있습니다.


## T map을 이용하는 샘플을 설명합니다. 

1. 초기 Application 생성메뉴에서 "T map" 템플릿을 선택하여 생성합니다. 

2. 제공되는 플로우 샘플1 은,  지도상의 특정지점을 노드로 입력받고, 이를 지도상에 보여주는 웹페이지를 제공합니다. 

3. 주소부분에 원하는 주소를 입력하세요 

4. 브라우져 새창을 열고, 도메인주소. ( userDomainName.sketchwork.io/template ) 를 입력합니다. 

**BACKUP**
간단하고 빠르게, 휴대폰의 다양한 센서값을 읽어올 수 있습니다.
상세 내용은 아래를 참고하세요..



## Mobile Sketch Sensor 개요
- Mobile Sensor App을 이용하여 휴대폰 센서값을 Designer Flow에서 확인 할 수 있습니다.
- Android OS Lollipop 5.0부터 지원하며, 간단하게 Domain URL만 입력하면 사용 가능합니다.
 
## T BaaS 이용을 위한 작업
- 아래 링크를 통해 APK를 다운 받은 후 실행하면, 위치 및 Mic 
- 먼저 developers.sktelecom.com에서 계정을 만든 다음 신규 프로젝트를 추가한 후 Service -> BaaS를 신청하면 SKT BaaS에 접속해서 사용 가능합니다.
- 정상적으로 설치가 되었으면 이제 Feature Node에서 T-BaaS를 사용할 수 있습니다. 생성된 프로젝트에서 BaaS Service -> Setting을 클릭하면 필요한 Rest Key를 확인할 수 있습니다.
![](https://tde.sktelecom.com/wiki/download/attachments/146290440/tdevelopers-dashboard.jpg?version=1&modificationDate=1511099700097&api=v2)
Dashboard -> Service 클릭
![](https://tde.sktelecom.com/wiki/download/attachments/146290440/tdevelopers-service.png?version=2&modificationDate=1511100721105&api=v2)
BaaS 신청 클릭
 
## Feature Node를 통한 T BaaS 사용
- SK API아래에 있는 T Baas DB에 TDC Key (Rest Key) 를 입력하면 기본적인 CRUD (Create, Read, Update, Delete) 동작을 수행할 수 있습니다.
- Feature Node의 Method명은 Rest type으로 구분되어 있으며, GET - Read, POST - Create, PUT - Update, DELETE - Delete로 매핑됩니다.
- 각 Method별로 사용 가능한 Action과 예제가 정해져 있고, 사용자 편의를 위해 예제를 복사할 수 있는 Copy Guide 버튼이 있습니다.