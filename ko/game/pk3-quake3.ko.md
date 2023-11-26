{
"날짜":"2023-11-01",
   "keywords":[
"pk3",
"pk3 파일",
"pk3 quake 3 엔진 게임 데이터 파일",
"pk3 파일을 여는 방법",
"파일",
"pk3 파일 확장자",
"확대",
"파일"
],
   "author":{
"display_name":"샤킬 파이즈"
},
"draft":"false",
"toc":true,
"title":"PK3 파일 형식 - Quake 3 엔진 게임 데이터",
   "description":"PK3 Quake 3 엔진 게임 데이터 파일 형식과 PK3 파일을 생성하고 열 수 있는 API에 대해 알아보세요.",
"linktitle":"PK3",
   "menu":{
      "docs":{
         "identifier":"game-pk3-quake3",
"parent":"게임"
}
},
"lastmod":"2023-11-01"
}

## .PK3 파일이란?

PK3 파일은 _Quake 3 Arena_, _Return to Castle Wolfenstein_ 및 기타 여러 게임과 같이 **Quake 3 Engine**을 활용하는 게임에서 사용되는 파일 형식입니다. PK3의 "PK"는 "Packed" 또는 "Package"를 나타내고 "3"은 이 파일 형식의 세 번째 버전을 나타냅니다. PK3 파일은 기본적으로 맵, 텍스처, 모델, 사운드, 스크립트 및 기타 리소스를 포함한 다양한 유형의 게임 데이터를 포함할 수 있는 아카이브 파일입니다. PK3 파일은 컨테이너처럼 작동하며 본질적으로 ZIP 파일이며 일반 Zip 압축 풀기 도구를 사용하여 파일을 열고 내용에 액세스할 수 있습니다.

## PK3 - Quake 3 엔진 게임 데이터

PK3 파일에 대한 추가 정보는 다음과 같습니다.

1. **압축:** PK3 파일은 일반적으로 공간을 절약하고 로딩 시간을 개선하기 위해 압축됩니다. 사용되는 압축 알고리즘은 ZIP 형식과 유사합니다.
    








2. **구성:** PK3 파일은 게임 자산을 구성하기 위해 폴더와 하위 폴더로 계층적으로 구성됩니다. 이러한 자산에는 지도(.bsp 확장자), 텍스처(.jpg 또는 .tga 확장자), 사운드(.wav 확장자) 및 기타 여러 가지가 포함될 수 있습니다.
    








3. **용도:** 게임 개발자는 PK3 파일을 사용하여 게임 자산을 효율적으로 패키지하고 배포합니다. 이 형식을 사용하면 모더와 매퍼가 해당 게임에 대한 사용자 정의 콘텐츠를 쉽게 만들 수 있습니다. 플레이어는 PK3 파일을 생성하거나 설치하여 게임의 모양, 게임 플레이 또는 기타 측면을 수정할 수도 있습니다.
    








4. **모딩:** PK3 파일은 **Quake 3 엔진 기반 게임** 모딩 커뮤니티에서 중요한 역할을 합니다. 모더는 게임 경험을 변경하기 위해 새로운 텍스처, 모델, 지도 및 기타 게임 자산이 포함된 사용자 정의 PK3 파일을 만들 수 있습니다.

## 퀘이크 3 엔진

Quake 3 엔진은 **id Software**에서 개발한 게임 엔진입니다. 이에 대한 몇 가지 유용한 정보는 다음과 같습니다.

1. **창작**: id Software에서 개발하여 1999년에 출시한 Quake 3 엔진은 "Quake III Arena" 게임에 사용되었습니다.
    








2. **게임플레이**: 빠르게 진행되는 멀티플레이어 중심의 1인칭 슈팅 게임플레이로 유명합니다.
    








3. **오픈 소스**: id Software는 2005년에 Quake 3 엔진용 소스 코드를 출시하여 다양한 모드와 독립형 게임에 사용하게 되었습니다.
    








4. **기술적 발전**: 곡면, 셰이더 및 인상적인 조명 효과를 포함하여 당시로서는 상당한 그래픽 발전을 도입했습니다.
    








5. **네트워킹**: 강력한 네트워킹 코드로 잘 알려져 있으며 원활하고 응답성이 뛰어난 온라인 멀티플레이어 경험을 제공하도록 설계되었습니다.
    








6. **모딩 커뮤니티**: 엔진의 오픈 소스 특성으로 인해 수많은 사용자 제작 모드와 전체 전환이 가능한 활발한 모딩 커뮤니티가 탄생했습니다.
      









7. **상업적 성공**: "Quake III Arena"는 상업적 성공을 거두었으며 엔진의 라이선스 가용성으로 인해 다른 게임 개발자들 사이에서 인기를 얻었습니다.
        










8. **멀티플랫폼**: Quake 3 엔진은 멀티플랫폼으로 설계되었으며 Windows, Linux 및 macOS용 게임에 사용되었습니다.

## PK3 파일을 여는 방법

**.PK3** 파일의 확장자를 **.ZIP** 파일로 변경한 다음 다음을 포함하는 Zip 압축 해제 도구를 사용할 수 있습니다.

- **7-Zip**(Windows)
- **WinRAR**(윈도우)
- **PeaZip** (윈도우, 리눅스)
- **Unarchiver**(macOS)
- **RAR**(크로스 플랫폼)

## 참고자료
* [id Tech 3](https://en.wikipedia.org/wiki/Id_Tech_3)