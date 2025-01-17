{
"날짜": "2023-09-27",
  "keywords": [
"cfg",
"cfg 파일",
"cfg 소스 엔진 구성 파일",
"cfg 파일이 무엇인가요?",
"cfg 파일을 여는 방법",
"파일",
"cfg 파일 확장자",
"확대"
],
  "author": {
"display_name": "샤킬 파이즈"
},
"draft": "false",
"toc": true,
"title": "CFG 파일 형식 - 소스 엔진 구성 파일",
  "description":"CFG 소스 엔진 구성 파일 형식과 CFG 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
"linktitle": "CFG Source Engine",
  "menu": {
    "docs": {
      "identifier": "game-cfg-sourceengine",
"parent" : "game"
}
},
"lastmod": "2023-09-27"
}

## .CFG 파일이란?

Half-Life 2와 같은 게임에서 볼 수 있듯이 **Valve의 소스 엔진** 컨텍스트의 CFG 파일은 구성 파일 역할을 합니다. 이 파일은 일반 텍스트 명령 목록을 통해 다양한 게임 내 설정을 변경하는 데 사용됩니다. 이러한 명령은 일반적으로 한 줄에 하나씩 배열되며 게임의 측면을 사용자 정의하는 역할을 합니다.

플레이어와 서버 관리자에게는 '.cfg' 파일에 지정된 변경 사항을 적용하기 위한 몇 가지 옵션이 있습니다.

1. **수동 실행**: 사용자는 CFG 파일 내에서 명령을 수동으로 실행할 수 있습니다. 이는 게임의 개발자 콘솔에 각 명령을 하나씩 입력한다는 의미입니다. 이 방법을 사용하면 어떤 설정을 언제 변경하는지 정밀하게 제어할 수 있습니다.
    





2. **자동 실행**: 또는 플레이어가 자동 실행을 선택할 수도 있습니다. 여기에는 `.cfg` 파일을 적절한 게임 디렉토리에 배치하는 것이 포함됩니다. `autoexec.cfg`와 같은 특정 `.cfg` 파일은 게임이 시작될 때 자동으로 실행됩니다. 이렇게 하면 게임을 시작할 때마다 수동 입력이 필요 없이 지정된 설정이 적용됩니다.

## 밸브 소스 엔진

간단히 **소스 엔진**이라고도 하는 Valve 소스 엔진은 Valve Corporation에서 개발한 매우 다재다능하고 널리 사용되는 게임 엔진입니다. 이는 많은 인기 비디오 게임의 기반이 되었으며 수많은 성공적인 타이틀의 원동력이 되었습니다. Valve Source Engine에 대한 몇 가지 주요 사항은 다음과 같습니다.

1. **역사**: Source 엔진은 2004년 Valve의 게임 "Counter-Strike 1.6" 출시와 함께 처음 소개되었습니다. 이후 여러 업데이트와 개정을 거쳤으며 최신 버전은 Source 2.0으로 알려져 있습니다.
    





2. **주요 게임**: Source Engine은 다음을 포함하되 이에 국한되지 않고 비평가들의 호평을 받는 다양한 게임에서 활용되었습니다.
    





- "Half-Life 2" 및 해당 에피소드
- "포털"과 "포털 2"
- "팀 포트리스 2"
- "레프트 4 데드"와 "레프트 4 데드 2"
- "카운터 스트라이크: 소스" 및 "카운터 스트라이크: 글로벌 오펜시브"
- "도타 2"
3. **특징**:
    





- **유연성**: Source Engine은 개발자가 1인칭 슈팅 게임부터 퍼즐 게임까지 다양한 게임 장르를 만들 수 있는 유연성으로 유명합니다.
- **물리학**: 사실적인 개체 상호 작용과 환경 효과를 가능하게 하는 강력한 물리 엔진이 포함되어 있습니다.
- **모딩 지원**: 엔진은 강력한 모딩 지원을 통해 수많은 사용자 생성 콘텐츠와 게임 모드를 만들 수 있습니다.
- **멀티 플레이어 기능**: Source Engine은 싱글 플레이어 및 멀티 플레이어 게임을 개발하는 데 사용되었으며 온라인 게임 플레이를 위한 광범위한 네트워킹 기능을 제공합니다.
    





4. **그래픽**: Source Engine은 진화하는 하드웨어 기능을 따라잡기 위해 수년에 걸쳐 그래픽 업데이트를 받았습니다. HDR(High Dynamic Range) 조명 및 동적 그림자와 같은 고급 렌더링 기술을 지원합니다.

## CFG 파일을 여는 방법?

Microsoft Visual Studio Code와 같은 텍스트 편집기나 원하는 다른 텍스트 편집기를 사용하여 `.cfg` 파일을 열고 수정할 수 있는 옵션이 있습니다. 이러한 텍스트 편집기는 '.cfg' 파일 내의 일반 텍스트 명령을 보고 편집할 수 있는 사용자 친화적인 인터페이스를 제공하므로 필요에 따라 설정을 사용자 정의할 수 있습니다.

CFG 파일을 열거나 참조하는 프로그램은 다음과 같습니다.

- 마이크로소프트 비주얼 스튜디오 코드
- 메모장
- 텍스트편집
- 모든 텍스트 편집기

## 기타 CFG 파일

**.cfg** 파일 확장자를 사용하는 다른 파일 형식은 다음과 같습니다.

**설정**
- [CFG - Celestia 구성 파일](/ko/settings/cfg-celestia/)
- [CFG - Citrix 서버 연결 파일](/ko/settings/cfg-citrix/)
- [CFG - MAME 구성 파일](/ko/settings/cfg-mame/)
- [CFG - LightWave 구성 파일](/ko/settings/cfg-lightwave/)

**게임**
- [CFG - Wesnoth 마크업 언어 파일](/ko/game/cfg-wesnoth/)
- [CFG - MUGEN 구성 파일](/ko/game/cfg-mugen/)
- [CFG - 소스 엔진 구성 파일](/ko/game/cfg-sourceengine/)

**시스템 및 기타**
- [CFG - CFG 파일](/ko/system/cfg/)
- [CFG - Cal3D 모델 구성 파일](/ko/misc/cfg-cal3d/)

## 참고자료
* [소스(게임 엔진)](https://en.wikipedia.org/wiki/Source_(game_engine))

