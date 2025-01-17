{
  "date" : "2021-09-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"OSR 파일을 만들고 열 수 있는 API와 OSR 파일 형식에 대해 알아보세요.",
  "title" :"OSR 파일 - osu! 재생 파일 형식",
  "linktitle" : "OSR",
  "menu" : {
    "docs" : {
      "identifier":"game-osr",
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## .OSR 파일이란?

OSR 파일은 [osu! 게임](https://osu.ppy.sh/home). 오스! 는 사용자가 마우스 클릭과 음악을 맞추는 리듬 게임입니다. OSR 파일에는 사용자가 연주한 곡, 안타, 안타, 연주한 시간과 날짜, 전체 순위가 기록됩니다. 이 OSR 파일은 재생 목적으로 다른 사람과 공유할 수 있습니다. OSR 파일은 "Songs" 폴더에 비트맵 파일이 있어야 합니다.

**OSR 파일 형식의 MIME 유형:** x-osu-replay

## OSR 파일 형식

OSR 파일은 고정 및 가변 길이 데이터 필드가 있는 이진 파일로 저장됩니다.

|데이터 유형| 형식|
---|---|
|바이트 |리플레이 게임 모드(0 = osu! Standard, 1 = Taiko, 2 = Catch the Beat, 3 = osu!mania)|
|정수 |리플레이가 생성되었을 때의 게임 버전(예: 20131216)|
|문자열 |osu! 비트맵 MD5 해시|
|문자열| 선수 이름|
|문자열| 오스! replay MD5 해시(replay의 특정 속성 포함)|
|짧게| 300대 수|
|짧게| 표준 100대, Taiko 150대, CTB 100대, 매니아 100대 수|
|짧게| 표준의 50대, CTB의 작은 과일, 매니아의 50대 수|
|짧게| 표준의 Gekis 수, 매니아의 최대 300s|
|짧게| 카투스는 기본, 매니아는 200대 |
|짧게| 놓친 횟수|
|정수| 점수 보고서에 표시되는 총 점수|
|짧게| 점수 보고서에 표시되는 최고의 콤보|
|바이트| 완벽/완벽한 콤보(1 = 미스 없음, 슬라이더 브레이크 없음, 조기 완료 슬라이더 없음)|
|정수| 사용된 모드. mod 값 목록은 아래를 참조하십시오.|
|문자열| 수명 막대 그래프: 쉼표로 구분된 u/v 쌍, 여기서 u는 노래에 들어간 시간(밀리초)이고 v는 주어진 시간에 보유한 생명의 양을 나타내는 0 - 1의 부동 소수점 값입니다(0 = 생명 막대는 비어 있음, 1= 라이프 바가 가득 찼음)|
|롱| 타임스탬프(Windows 틱)|
|정수| 압축된 재생 데이터의 길이(바이트) |
|바이트 |배열 압축 재생 데이터|
|롱| 온라인 점수 ID|
|더블| 추가 모드 정보. Target Practice가 활성화된 경우에만 존재합니다.|

## 참조

* [오쓰! 리듬게임](https://osu.ppy.sh/home)
* [OSR 파일 형식](https://osu.ppy.sh/wiki/en/Client/File_formats/Osr_%28file_format%29#data-types)

