{
"날짜":"2023-01-04",
   "keywords":[
"업",
"UP 파일",
"ups 패치 파일",
"UPS 파일을 여는 방법",
"파일",
"UPS 파일 확장자",
"확대",
"파일"
],
   "author":{
"display_name":"샤킬 파이즈"
},
"draft":"false",
"toc":true,
"title":"UPS 파일 형식 - UPS 패치 파일",
   "description":"UPS 파일을 생성하고 열 수 있는 UPS 패치 파일 형식과 API에 대해 알아보세요.",
"linktitle":"UPS",
   "menu":{
      "docs":{
         "identifier":"game-ups",
"parent" : "game"
}
},
"lastmod":"2023-01-04"
}

## .UPS 파일이란?

**Universal Patching System**을 의미하는 UPS 파일은 비디오 게임이나 기타 소프트웨어의 데이터를 수정하거나 변경 사항을 적용하는 데 사용되는 패치 파일 유형입니다. UPS 파일은 일반적으로 에뮬레이션 커뮤니티에서 오래된 비디오 게임의 ROM(읽기 전용 메모리)에 패치나 수정 사항을 적용하는 데 사용됩니다.

## UPS 패치 파일

UPS 패치 파일의 작동 방식은 다음과 같습니다.

1. **원본 데이터:** 수정하려는 비디오 게임이나 소프트웨어의 원본 ROM 파일로 시작합니다. 이 ROM에는 게임의 코드와 데이터가 포함되어 있습니다.
    






2. **패치 파일:** UPS 패치 파일은 특수 패치 소프트웨어를 사용하여 생성됩니다. 이 패치 파일에는 원본 데이터에 적용하려는 변경 사항이 포함되어 있습니다. 이러한 변경 사항에는 버그 수정, 번역 패치 또는 기타 수정 사항이 포함될 수 있습니다.
    






3. **패치 프로세스:** 변경 사항을 적용하려면 원본 ROM 및 UPS 패치 파일을 입력으로 사용하는 UPS 패치 도구를 사용합니다. 그런 다음 패치 도구는 UPS 패치 파일에 지정된 변경 사항을 원본 ROM에 적용하여 수정된 게임 또는 소프트웨어 버전을 만듭니다.
    






4. **결과:** 출력은 UPS 패치 파일의 변경 사항을 통합한 패치 또는 수정된 ROM입니다. 이 패치된 ROM은 에뮬레이터에서 재생되거나 수정 사항에 따라 다른 방식으로 사용될 수 있습니다.
    







UPS 패치 파일은 사용자가 저작권의 대상이 될 수 있는 전체 게임의 ROM을 배포하지 않고도 오래된 게임을 개선하거나 수정할 수 있도록 하기 때문에 에뮬레이션 커뮤니티에서 인기가 있습니다. 대신 사용자는 변경 사항이 포함된 UPS 패치 파일만 공유할 수 있으며 사용자는 이를 합법적으로 소유한 원본 ROM에 적용할 수 있습니다.

UPS 패치는 [IPS](/ko/game/ips/)에 비해 여러 가지 장점을 제공합니다.

1. **크기 제한 없음:** 16MB로 제한되는 IPS 패치와 달리 UPS 패치는 모든 크기의 파일에 사용할 수 있습니다. 이러한 유연성으로 인해 UPS는 대규모 게임 및 소프트웨어에 특히 유용합니다.
    






2. **양방향 패치:** UPS는 양방향 패치를 지원합니다. 즉, 단일 UPS 패치로 게임이나 소프트웨어에 대한 변경 사항을 적용하고 제거할 수 있습니다. 이 기능은 변경 사항을 수정하거나 되돌리는 프로세스를 단순화하여 사용자 경험을 향상시킵니다.
    






3. **CRC32 체크섬:** UPS는 올바른 게임이나 소프트웨어에 패치가 적용되도록 보장하기 위해 내장 메커니즘으로 CRC32 체크섬을 사용합니다. 이 체크섬 확인은 패치된 파일의 무결성을 유지하는 데 도움이 되며 실수로 또는 잘못된 패치 적용을 방지합니다.

## UPS 패치를 적용하는 방법은 무엇입니까?

UPS 패치를 적용하려면 Lunar IPS(Windows용), NUPS(Windows용) 또는 MultiPatch(다중 플랫폼용)와 같은 UPS 패치 도구와 패치하려는 게임 또는 소프트웨어의 원본 ROM이 필요합니다.

## UPS 파일 여는 방법?

UPS 파일을 여는 프로그램은 다음과 같습니다

- **Lunar IPS**(Windows용)
- **NUPS**(Windows용)
- **멀티패치**(여러 플랫폼용)

## 참고자료
* [루나 IPS](https://www.romhacking.net/utilities/240/)

