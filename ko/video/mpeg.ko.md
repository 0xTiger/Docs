{
"날짜": "2023-07-12",
  "keywords": [
"mpeg",
"mpeg 파일",
"MPEG 파일이 무엇인가요?",
"MPEG 파일을 여는 방법",
"파일",
"mpeg 파일 확장자",
"확대"
],
  "author": {
"display_name": "샤킬 파이즈"
},
"draft": "false",
"toc": true,
"title": "MPEG 파일 형식 - MPEG 비디오",
  "description":"MPEG 파일을 만들고 열 수 있는 MPEG 형식과 API에 대해 알아보세요.",
"linktitle": "MPEG",
  "menu": {
    "docs": {
      "identifier": "video-mpeg",
"parent" : "video"
}
},
"lastmod": "2023-07-12"
}

## MPEG 파일이란 무엇입니까?

MPEG 비디오 파일로도 알려진 MPEG 파일은 비디오 압축을 위해 MPEG(Moving Picture Experts Group) 표준을 사용하는 디지털 비디오 파일 형식입니다. MPEG은 비디오 데이터를 저장하고 전송하는 데 널리 사용되는 형식입니다.

MPEG 형식은 손실 압축을 사용합니다. 즉, 파일 크기를 줄이기 위해 일부 정보가 삭제됩니다. 이 압축 기술을 사용하면 합리적인 비디오 품질을 유지하면서 비디오 콘텐츠를 효율적으로 저장하고 스트리밍할 수 있습니다. MPEG 표준에는 MPEG-1, MPEG-2, MPEG-4, MPEG-7 등 여러 버전이 있으며 각각 압축 수준과 품질이 다릅니다.

MPEG 파일은 일반적으로 파일 확장자가 ".mpeg" 또는 ".mpg"입니다. 여기에는 비디오 및 오디오 데이터가 모두 포함될 수 있으며 종종 단일 파일로 결합됩니다. MPEG 파일은 다양한 미디어 플레이어 및 비디오 편집 소프트웨어와 호환되므로 비디오 콘텐츠 공유 및 배포에 널리 사용됩니다.

## MPEG 파일을 여는 방법?

MPEG 파일을 열고 재생할 수 있는 다양한 소프트웨어 응용 프로그램이 있습니다. 다음은 몇 가지 인기 있는 옵션입니다.

- VLC 미디어 플레이어
- 윈도우 미디어 플레이어
- 퀵타임 플레이어
- MPC-HC
- 곰플레이어
- MPlayer
- 팟플레이어
- 코디

## MPEG 파일을 변환하는 방법은 무엇입니까?

VideoLAN VLC 미디어 플레이어, HandBrake 및 Apple QuickTime Player를 포함하여 MPEG 파일을 다른 형식으로 변환할 수 있는 다양한 비디오 응용 프로그램이 있습니다. 예를 들어 VLC는 MPEG 파일을 다음 형식으로 변환할 수 있습니다.

- MP4
-AVI
- MKV
- MOV
- WMV
- FLV

## MPEG 파일의 내부 구조 개요

MPEG 파일의 내부 구조는 비디오, 오디오 및 기타 관련 정보를 구성하고 저장하는 다양한 구성 요소와 데이터 구조로 구성됩니다. 다음은 MPEG 파일 내부 구조의 핵심 요소에 대한 개요입니다.

- **시스템 계층:**

시스템 계층은 MPEG 파일의 전체 구조를 정의합니다. 여기에는 디코딩 및 재생에 필요한 헤더, 프로그램 스트림 및 기타 시스템 관련 데이터가 포함됩니다. 시스템 계층은 기본 스트림의 동기화 및 다중화를 관리합니다.

- **초등학교 스트림:**

MPEG 파일에는 비디오, 오디오 및 기타 데이터 유형에 대한 별도의 기본 스트림이 포함되어 있습니다. 각 기본 스트림은 해당 유형에 특정한 압축 데이터를 전달합니다. 예를 들어 비디오 기본 스트림에는 압축된 비디오 프레임이 포함되고 오디오 기본 스트림에는 압축된 오디오 샘플이 포함됩니다.

- **동영상 압축:**

프레임 내 및 프레임 간 압축과 같은 MPEG 비디오 압축 기술은 비디오 품질을 유지하면서 파일 크기를 줄이는 데 사용됩니다. 압축된 비디오 프레임은 인트라 코딩(I), 예측(P) 및 양방향(B) 프레임으로 구성된 GOP(그림 그룹)로 구성됩니다.

- **오디오 압축:**

MPEG 파일은 MP3, AAC 또는 MPEG-1 Audio Layer II와 같은 다양한 오디오 압축 코덱을 지원합니다. 오디오 샘플은 이러한 코덱을 사용하여 압축되므로 오디오 데이터를 효율적으로 저장하고 전송할 수 있습니다.

- **동기화 및 타이밍:**

MPEG 파일은 타임스탬프와 동기화 정보를 사용하여 재생 중에 비디오와 오디오 스트림 간의 적절한 정렬을 보장합니다. 이러한 타임스탬프는 동기화를 유지하고 오디오 및 비디오 프레임의 디코딩 및 렌더링을 위한 정확한 타이밍을 제공하는 데 도움이 됩니다.

- **메타데이터:**

MPEG 파일에는 비디오 및 오디오 콘텐츠에 대한 추가 정보를 제공하는 메타데이터가 포함될 수 있습니다. 이 메타데이터에는 제목, 작성자, 생성 날짜 및 기타 설명 정보와 같은 세부 정보가 포함될 수 있습니다.

- **패킷 및 팩 헤더:**

MPEG 파일은 데이터를 패킷으로 구성합니다. 각 패킷에는 스트림 유형, 패킷 크기, 타이밍 정보 등 패킷 내용에 대한 정보를 제공하는 팩 헤더가 포함되어 있습니다.

- **프로그램별 정보(PSI):**

PSI는 프로그램 및 스트림 식별자, 스트림 유형 및 설명자와 같은 프로그램 스트림에 대한 추가 정보를 전달하는 MPEG 파일의 섹션입니다. PSI는 파일 내의 기본 스트림을 디코딩하고 역다중화하는 데 도움이 됩니다.

- **전송 스트림:**

MPEG-2에는 비디오 콘텐츠를 방송하고 전송하는 데 사용되는 특정 전송 스트림 형식이 있습니다. 전송 스트림은 여러 프로그램을 단일 스트림으로 다중화하여 네트워크를 통해 오디오, 비디오 및 기타 데이터를 효율적으로 전송하고 동기화할 수 있도록 합니다.

## MPEG 파일 형식 - 추가 정보

다음은 MPEG 파일 형식에 대해 알아야 할 몇 가지 중요한 사항입니다.

- **압축:**

MPEG 파일은 합리적인 비디오 품질을 유지하면서 파일 크기를 줄이기 위해 손실 압축 기술을 사용합니다. 압축 정도는 사용된 MPEG 버전 및 설정에 따라 달라질 수 있습니다.

- **비디오 및 오디오:**

MPEG 파일에는 비디오 및 오디오 데이터가 모두 포함될 수 있습니다. 비디오 데이터는 MPEG 표준을 사용하여 압축되고, 오디오는 MP3 또는 AAC와 같은 다양한 오디오 코덱을 사용하여 압축할 수 있습니다.

- **MPEG 버전:**

MPEG 표준에는 MPEG-1, MPEG-2, MPEG-4, MPEG-7 등 다양한 버전이 있습니다. 각 버전에는 고유한 사양, 기능 및 압축 수준이 있습니다. MPEG-1은 일반적으로 VCD(비디오 CD)에 사용되는 반면 MPEG-2는 DVD 및 방송 TV에 사용됩니다. MPEG-4는 온라인 비디오 스트리밍에 널리 사용되며 MPEG-7은 멀티미디어 콘텐츠 설명 및 메타데이터에 중점을 둡니다.

- **파일 확장자:**

MPEG 파일은 일반적으로 ".mpeg" 또는 ".mpg" 파일 확장자를 갖습니다. 그러나 MPEG-4 파일의 경우 ".mp4", MPEG-1 Audio Layer 3 파일의 경우 ".mp3"와 같이 다양한 변형 및 확장자가 존재할 수 있습니다.

- **교차 플랫폼 호환성:**

MPEG 파일은 다양한 미디어 플레이어, 운영 체제 및 장치에서 널리 지원됩니다. Windows, Mac, Linux 시스템은 물론 스마트폰, 태블릿, 스마트 TV에서도 재생할 수 있습니다.

- **편집:**

MPEG 파일은 비디오 편집 소프트웨어를 사용하여 편집할 수 있습니다. 그러나 MPEG은 손실 압축을 사용하므로 파일을 반복적으로 편집하고 다시 인코딩하면 품질이 저하될 수 있습니다. 광범위한 편집을 하기 전에 무손실 형식으로 작업하거나 백업 복사본을 만드는 것이 권장되는 경우가 많습니다.

- **스트리밍:**

MPEG 파일은 일반적으로 인터넷을 통해 비디오 콘텐츠를 스트리밍하는 데 사용됩니다. 특히 MPEG-4는 효율적인 압축과 우수한 크기 대비 품질 비율로 인해 온라인 비디오 플랫폼 및 비디오 공유 웹사이트에서 인기가 높습니다.

- **진화하는 표준:**

MPEG 표준은 기술 발전을 따라잡기 위해 계속 발전하고 있습니다. MPEG-4 Part 10(H.264 또는 AVC라고도 함) 및 MPEG-4 Part 14(MP4)와 같은 최신 버전 및 변형은 향상된 압축 효율성을 제공하고 고화질 비디오 및 3D 콘텐츠와 같은 고급 기능을 지원합니다.

- **멀티미디어 애플리케이션:**

MPEG 파일은 디지털 TV, 스트리밍 서비스, 화상 회의, 비디오 감시, 멀티미디어 프레젠테이션 등 다양한 영역에서 응용 프로그램을 찾습니다.

## MPEG 대 다른 형식

MPEG 파일 형식을 다른 비디오 형식과 비교할 때 압축 효율성, 호환성, 기능 및 지원을 포함한 여러 요소가 작용합니다. 다음은 MPEG와 일부 인기 있는 비디오 형식을 비교한 것입니다.

### MPEG 대 AVI(오디오 비디오 인터리브)

- **압축:**
   

MPEG 파일은 일반적으로 AVI에 비해 압축 효율성이 높기 때문에 파일 크기가 더 작아집니다.

- **호환성:**

AVI 파일은 다양한 미디어 플레이어에서 널리 지원되지만 MPEG 파일은 장치와 플랫폼 전반에 걸쳐 더 폭넓은 호환성을 제공합니다.

- **특징:**

MPEG 파일은 다중 오디오 트랙, 자막, 챕터와 같은 고급 기능을 지원하는 경우가 많지만 AVI는 이러한 기능을 제한적으로 지원합니다.

- **비디오 품질:**

압축 설정에 따라 MPEG와 AVI는 유사한 비디오 품질을 얻을 수 있지만 MPEG은 고급 압축 기술로 인해 낮은 비트 전송률에서 더 나은 품질을 제공하는 경우가 많습니다.

### MPEG 대 WMV(Windows Media 비디오):

- **압축:**

WMV 파일은 일반적으로 MPEG에 비해 더 나은 압축 효율성을 제공하므로 우수한 비디오 품질을 유지하면서 파일 크기가 더 작아집니다.

- **호환성:**

MPEG 파일은 다양한 장치 및 플랫폼에서 더 폭넓은 호환성을 갖고 있는 반면, WMV 파일은 주로 Windows 기반 시스템과 연결되어 있습니다.

- **특징:**

두 형식 모두 다중 오디오 트랙 및 자막을 포함한 다양한 기능을 지원하지만 MPEG는 고급 기능에 대해 더 다양한 기능과 광범위한 지원을 제공하는 경우가 많습니다.

- **비디오 품질:**

유사한 압축 설정을 사용하면 MPEG와 WMV가 비슷한 비디오 품질을 얻을 수 있지만 WMV는 고급 압축 기술로 인해 특정 시나리오에서 더 나은 성능을 발휘할 수 있습니다.

### MPEG 대 MP4(MPEG-4 파트 14):

- **압축:**

MPEG과 MP4는 모두 유사한 압축 기술을 사용하며 압축 효율성은 비슷할 수 있습니다. 그러나 MP4 내의 MPEG-4 Part 10(H.264/AVC)은 이전 MPEG 형식보다 더 나은 압축 기능을 제공하는 경우가 많습니다.

- **호환성:**

MPEG와 MP4는 모두 장치와 플랫폼 전반에 걸쳐 광범위한 호환성을 가지고 있습니다. MP4는 광범위한 지원과 채택으로 인해 최근 몇 년간 큰 인기를 얻었습니다.

- **특징:**

MP4는 자막, 챕터, 대화형 메뉴, H.264 및 HEVC(H.265)와 같은 고급 비디오 코덱 지원을 포함하여 더욱 고급 기능을 제공합니다. MP4 내의 MPEG-4 Part 2(DivX, Xvid)도 고급 기능을 지원합니다.

- **비디오 품질:**

MPEG 및 MP4는 비슷한 압축 설정을 사용하면 비슷한 비디오 품질을 얻을 수 있습니다. 그러나 MP4는 고급 비디오 코덱을 지원하므로 낮은 비트 전송률에서도 더 나은 품질을 얻을 수 있습니다.

## 참고자료
* [MPEG-1](https://en.wikipedia.org/wiki/MPEG-1)

