{
"날짜": "2023-09-27",
  "keywords": [
"cfg",
"cfg 파일",
"cfg 머겐 구성 파일",
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
"title": "CFG 파일 형식 - MUGEN 구성 파일",
  "description":"CFG MUGEN 구성 파일 형식과 CFG 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
"linktitle": "CFG MUGEN",
  "menu": {
    "docs": {
      "identifier": "game-cfg-mugen",
"parent": "게임"
}
},
"lastmod": "2023-09-27"
}

## .CFG 파일이란?

MUGEN과 관련된 CFG 파일은 "MUGEN 구성 파일"을 나타냅니다. **MUGEN**은 Elecbyte에서 개발한 맞춤형 2D 격투 게임 엔진입니다. 사용자는 CFG 파일을 포함한 다양한 구성 파일을 편집하여 자신만의 캐릭터와 스테이지를 만들고 게임의 동작과 규칙을 수정할 수도 있습니다.

MUGEN `.cfg` 파일에서 찾을 수 있는 내용에 대한 기본 개요는 다음과 같습니다.

1. **시스템 구성**: CFG 파일에는 게임 엔진의 일반적인 동작과 관련된 설정이 포함되는 경우가 많습니다. 여기에는 화면 해상도, 사운드 설정, 입력 구성(키보드, 조이스틱 또는 컨트롤러 매핑) 등이 포함됩니다.
    








2. **캐릭터 및 스테이지 기본값**: 캐릭터 및 스테이지의 기본 설정을 정의할 수 있습니다. 예를 들어 게임이 시작될 때 로드되는 캐릭터와 단계를 지정할 수 있습니다.
    








3. **게임 플레이 옵션**: MUGEN `.cfg` 파일은 라운드 시간 제한, 데미지 스케일링 등과 같은 다양한 게임 플레이 옵션을 제어할 수도 있습니다.
    








4. **디버깅 및 개발**: 고급 사용자는 디버깅 및 개발 목적으로 '.cfg' 파일을 사용할 수 있습니다. 이러한 설정은 디버깅 정보가 화면에 표시되는 방식을 제어하거나 기타 개발 관련 동작을 정의할 수 있습니다.
    








5. **스크린팩 구성**: 스크린팩은 게임의 모양과 느낌을 바꾸는 시각적 테마입니다. `.cfg` 파일은 어떤 스크린팩이 사용되는지 지정하고 다양한 요소를 구성할 수 있습니다.
    








6. **AI 행동**: MUGEN을 사용하면 전투에서 컴퓨터 제어 캐릭터(AI)가 행동하는 방식을 정의할 수 있습니다. `.cfg` 파일에는 AI 난이도 및 동작과 관련된 설정이 포함될 수 있습니다.

## MUGEN 구성 파일

MUGEN CFG(구성) 파일은 맞춤형 격투 게임 세계의 제작자에게 중요한 구성 요소입니다. 이는 게임의 기본 규칙을 형성할 수 있는 권한을 부여합니다. 여기에는 각 라운드가 지속되는 시간, 컴퓨터로 제어되는 상대가 제시하는 도전 수준, 게임 속도, 콤보가 손상에 영향을 미치는 정도 등의 요소가 포함됩니다.

또한 CFG 파일을 사용하면 제작자는 화면 해상도와 같은 게임의 디스플레이 설정을 결정하고 MUGEN이 게임 플레이 중에 음향 효과와 음악을 재생할지 여부를 결정할 수 있습니다. MUGEN의 복잡함에 정통한 사람들에게 이 파일은 독특한 게임 경험을 만들기 위해 다양한 게임 관련 설정을 조정할 수 있는 가능성을 제공합니다.

기본적으로 `mugen.cfg`로 알려진 MUGEN의 기본 CFG 파일은 프로그램의 데이터 폴더에 있습니다. 이 파일 내에서 게임 설정을 직접 편집하는 것이 가능하지만 일반적으로 먼저 백업 복사본을 만드는 것이 좋습니다. 이 예방 조치를 통해 의도하지 않은 변경으로 인해 게임 경험이 중단되는 것을 방지하고 필요한 경우 MUGEN을 원래 설정으로 쉽게 되돌릴 수 있습니다.

## MUGEN - 게임 엔진

MUGEN은 Elecbyte가 개발한 다재다능하고 사용자 정의가 가능한 2D 격투 게임 엔진입니다. "MUGEN"이라는 이름은 "Mugen Ultimate Game Engine"을 의미합니다. 1999년에 처음 출시된 이후 엔진을 사용하여 자신만의 2D 격투 게임을 디자인하고 개발하는 전용 사용자 및 제작자 커뮤니티를 확보했습니다.

MUGEN의 주요 기능과 측면은 다음과 같습니다.

1. **사용자 정의 가능한 캐릭터:** MUGEN을 사용하면 사용자는 자신의 캐릭터("파이터" 또는 "스프라이트"라고도 함)를 만들고 게임에 가져올 수 있습니다. 제작자는 이러한 캐릭터에 대한 고유한 동작 세트, 애니메이션 및 특수 공격을 디자인할 수 있으므로 다양한 프랜차이즈 또는 원본 창작물의 거의 모든 캐릭터를 포함할 수 있습니다.
    








2. **스테이지:** 사용자는 캐릭터 외에도 전투가 진행되는 스테이지를 만들고 맞춤 설정할 수도 있습니다. 이러한 스테이지는 상호작용적인 요소와 독특한 배경을 가질 수 있습니다.
      









3. **스크린팩:** 스크린팩은 메뉴, 캐릭터 선택 화면, 라이프 바 등 게임의 전반적인 모습을 바꾸는 시각적 테마입니다. 사용자는 자신만의 스크린팩을 만들고 공유하여 게임에 독특한 모양과 느낌을 부여할 수 있습니다.
    








4. **사운드 및 음악:** 제작자는 게임에 음향 효과와 배경 음악을 추가하여 전반적인 게임 경험을 향상시킬 수 있습니다.
    








5. **스크립팅:** 고급 사용자는 내장된 스크립트 언어를 사용하여 복잡한 캐릭터 동작, 독특한 게임 메커니즘 및 특수 효과를 만들 수 있습니다.

## CFG 파일을 여는 방법?

MUGEN CFG 파일은 다양한 텍스트 편집기로 액세스할 수 있는 일반 텍스트 문서입니다. Windows에서는 Microsoft 메모장이나 워드패드를 사용할 수 있고, macOS 사용자는 이러한 목적으로 Apple TextEdit을 사용할 수 있습니다. 이러한 편집기를 사용하면 사용자는 CFG 파일 내의 구성 설정을 쉽게 보고 수정할 수 있습니다.

CFG 파일을 열거나 참조하는 프로그램

- 엘렉바이트 무겐
- 메모장
- 텍스트편집

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
* [Mugen(게임 엔진)](https://en.wikipedia.org/wiki/Mugen_(game_engine))
