{
  "date" : "2019-10-11",
  "keywords" :[ "jp2 파일", "jp2 파일 형식", "jp2 파일이란", "파일", "jp2 예", "jp2 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JP2 - 이미지 파일 형식",
  "description":"JP2 파일 형식과 JP2 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "JP2",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-08-10"
}

## .JP2 파일이란? ##

JPEG 2000(**JP2**)은 이미지 코딩 시스템이자 최첨단 이미지 압축 표준입니다. 웨이블릿 기술을 사용하여 한 번에 모든 품질의 무손실 콘텐츠를 코딩합니다. 게다가, JPEG 2000은 코딩 효율성에 있어 실질적인 불이익 없이 동일한 콘텐츠에 액세스하고 다양한 다른 해상도 및 품질로 효과적으로 디코딩할 수 있는 기능을 가지고 있습니다. JPEG 2000의 코드 스트림은 공간 랜덤 액세스를 위한 기능을 제공하는 관심 영역을 포함하여 상당히 확장 가능합니다.

JPEG 2000은 가장 확장 가능한 표준 중 하나입니다. 다양한 품질을 사용하여 이미지의 다른 부분을 저장할 수 있습니다. 다양한 방법으로 코드 스트림을 주문함으로써 주목할만한 성능 향상을 달성할 수 있습니다. 그럼에도 불구하고 JP2는 이러한 유연성의 결과로 복잡하고 계산이 까다로운 인코더/디코더가 필요합니다. JPEG와 비교할 때 JPEG 2000은 이미지 가장자리 근처에서 링을 만들고 흐릿해질 수 있는 링잉 아티팩트만 생성하는 반면 JPEG는 링잉 및 차단 아티팩트가 될 수 있는 8×8 시각적 아티팩트 블록을 사용합니다. 최대 16384개의 다양한 구성 요소를 테라픽셀 단위의 치수와 38비트/샘플의 정밀도까지 보유합니다.

## 역사 ##

2000년 Joint Photography Experts Group 위원회는 이 새로운 웨이블릿 기반 방법으로 이산 코사인 변환 기반 JPEG 표준을 개선할 목적으로 JP2를 설계했습니다. JPEG 위원회는 라이선스 비용이 없는 기본 방법을 제공하는 것을 목표로 했습니다. JP2 라이선스가 20개 회사 사이에서 경쟁을 벌이는 과정에서 수염으로 이겼습니다. JPEG 2000은 ISO 표준으로 선언되었지만 대부분의 웹 브라우저는 2017년 이후로 JPEG 2000에 손을 댈 준비가 되어 있지 않습니다.

## JPEG 2000 이미지 코딩 시스템의 일부 ##

다음은 JPEG 2000에 대한 전체 표준 제품군을 구성하는 주요 부분입니다.


|부품|제목|설명|번호
---|---|---|---|
|파트 1|코어 코딩 시스템| 코드 스트림의 구문을 정의합니다. JPEG 2000 이미지 디코딩과 관련된 다양한 단계. 기본 파일 형식 JP2, 메타데이터 및 제공할 IP 권한을 설명합니다.|ISO/IEC 15444-1
|파트 2|확장자|파일 형식 코드 스트림에 대한 확장자를 정의하고 HDR 샘플 데모, 색상 공간 사양, 자르기, 기하학적 변환을 허용합니다. 다양한 애니메이션, 메타데이터 및 다중 코드 스트림.|ISO/IEC 15444-2
|3부|모션 JPEG 2000(MJ2 또는 MJP2)|독립적인 코드 스트림으로 이미지를 인코딩하는 모션 시퀀스용 파일 형식을 소개합니다.|ISO/IEC 15444-3
|4부|적합성|인코딩 및 디코딩을 위한 테스트 기술을 설명하고 베어 코드 스트림과 JP2 파일 모두에 대한 파일을 확인합니다.|ISO/IEC 15444-4
|파트 5|참조 소프트웨어|Core 코딩 시스템을 구현하고 오픈 소스 라이선스에 따라 사용 가능한 두 개의 소스 코드 패키지(Java, C)로 구성됩니다.|ISO/IEC 15444-5
|6부|복합 이미지 파일 형식|JPM 파일 형식을 정의하고 팩스와 같은 응용 프로그램에 대한 다중 페이지 문서 이미징을 허용합니다. JBIG2 및 JPEG 사용을 지원합니다.|ISO/IEC 15444-6
|8부|JPSEC(JPEG 2000 Secured)|트랜잭션, 콘텐츠 및 기술의 보안을 보장하고 보안 JPEG 2000 비트 스트림을 허용합니다.|ISO/IEC 15444-8
|9부|JPIP|메타데이터 및 이미지에 액세스하기 위해 네트워크 환경에서 도구를 정의하고 대화형 및 효율적인 프로토콜|ISO/IEC 15444-9
|파트 10|JP3D|파트 1의 체적 확장 및 Z 치수를 소개합니다. 타일, 코드 블록, 구역 및 3D 관심 영역 접근성 기능의 개념을 확장합니다.|ISO/IEC 15444-10
|11부|JPWL|오류가 발생하기 쉬운 무선 네트워크를 통한 잘 구성된 전송을 다룹니다. 이 확장은 디코더|ISO/IEC 15444-11과 호환됩니다.
|파트 13|엔트리 레벨 인코더|코어 코딩 시스템의 엔트리 레벨 인코더 구현을 정의합니다.|ISO/IEC 15444-13
|파트 14|JPXML|XML로 표현하고 이미지의 내부 데이터에 액세스하기 위한 마커 세그먼트 및 방법을 설명합니다.|ISO/IEC 15444-14
|15부|HTJ2K(개발 중)|대체 블록 코딩 알고리즘을 지정합니다. 알고리즘은 10배 증가한 처리량과 무손실 코딩/디코딩을 제공합니다.|

## JP2 파일 형식 ##

JPEG 2000은 JPEG-1과 같은 방식으로 파일 형식과 코드 스트림을 정의합니다. 이미지 샘플은 JPEG 2000에서만 설명되지만 JPEG-1에는 이미지를 인코딩하는 데 필수적인 색상 공간 및 해상도에 대한 기타 추가 정보가 포함되어 있습니다. 이미지가 JPEG 2000 파일로 저장된 경우 **.jp2**가 확장자로 사용됩니다. 이 파일 형식은 애니메이션 메커니즘과 수많은 코드 스트림의 구성을 하나의 단일 이미지로 정의하는 JPEG 2000 part-2 확장으로 더욱 향상되었습니다. **.jpx** 확장자는 이 확장 파일 형식을 사용하여 이미지를 저장할 때 사용됩니다. 코드 스트림 데이터는 주로 파일에 저장되는 것으로 간주되지 않으므로 이 목적을 위해 정의된 표준 확장자가 없습니다. 테스트 목적을 위해 자주 **.jpc** 또는 **.j2k** 확장자를 얻습니다. JPEG-1과 달리 JPEG 2000은 메타데이터를 XML 형식으로 인코딩하는 다른 방법을 선택합니다. 표준 12234-1.4(ISO TC42 위원회)는 Exif 태그와 XML 구성 요소 간의 참조로 사용됩니다. JPEG 2000에는 ISO 표준, XMP가 포함될 수 있습니다.

### 청크 ###
JPEG 2000 파일은 연속적인 청크로 구성됩니다. 각 청크에는 8바이트 헤더가 있습니다. 4바이트 청크 크기(빅 엔디안, 상위 바이트 우선) 및 4바이트 청크 유형 - 사전 정의된 서명 중 하나: "jP" 또는 "jP2".

두 번째 청크는 "ftyp" 유형이어야 하고 오프셋 8에 하위 유형이 있어야 합니다. "jp2"(파일 유형 \*.JP2), "jp20"(파일 유형 \*.JPA), "jpm "(파일 유형 \*.JPM), "jpx"(파일 유형 \*.JPX).

알 수 없는 유형이 감지될 때까지 청크를 반복하여 JPEG 2000 이미지/비디오 파일을 구성합니다.

### 색상 변환 ###

처음에는 RGB 색 공간에서 다른 색 공간으로 이미지를 변환해야 합니다. 이를 위해 ICT(Irreversible Color Transform)와 RCT(Reversible Color Transform)의 두 가지 방법이 있습니다. 전자는 YC,,B,,C,,R,, 색 공간을 사용하고 고정/부동 소수점으로 구현해야 하지만 나중에 수정된 YUV 색 공간과 가역성은 본질적으로 가역적입니다.// //RGB 모델에 국한되지 않음, JPEG 2000 언어는 다중 구성 요소 변환을 사용합니다.

### 타일링 ###

색상 변환이 완료되면 이미지는 개별적으로 변환 및 인코딩할 수 있는 타일이라는 직사각형 영역으로 변환됩니다. 모든 타일의 크기는 동일하거나 전체 이미지를 하나의 단일 타일로 간주할 수 있습니다. 디코더는 타일링을 활용하고 메모리를 덜 사용하거나 일부 타일을 부분적으로 인코딩할 수 있습니다. 그러나 이 기술은 화질이 저하되는 단점이 있다.

### 웨이블릿 변환 ###

타일링 후 이미지는 되돌릴 수 없거나 되돌릴 수 있고 컨볼루션 또는 리프팅 방식을 사용하여 구현될 수 있는 웨이블릿 변환됩니다.

### 압축률 ###

이미지의 물리적 특성에 따라 20%의 압축 이득을 얻습니다. JPEG 2000의 공간 중복 예측은 압축 과정에서 중요한 역할을 하며 고해상도 이미지가 가장 이점을 얻는 경향이 있습니다.

## 표준 ##에서 제공하는 애플리케이션

* 프레임 기반 HD 비디오의 녹화, 편집 및 저장
* 의료 이미지 및 생체 인식
* 위성 이미지, 원격 감지 및 모션 감지
* 클라이언트/서버 통신, 네트워크 배포 및 저장.
* 디지털 시네마, 라이브 HDTV 피드 기고, 디지털화된 시청각 자료

## 참조 ##

* [JPEG 2000 개요](https://jpeg.org/jpeg2000)
* [JPEG 2000 이미지 코딩 시스템](https://en.wikipedia.org/wiki/JPEG_2000#JPEG_2000_image_coding_system_-_Parts)
