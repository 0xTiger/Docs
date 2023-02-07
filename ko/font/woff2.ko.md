{
  "date" : "2023-01-10",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WOFF2 파일 - Web Open Font Format 2.0 파일",
  "description":"WOFF2 파일이 무엇인지, WOFF2 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "WOFF2",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2023-01-10"
}

## WOFF2 파일이란 무엇입니까?

WOFF2는 WOFF(Web Open Font Format)의 보다 압축된 버전인 글꼴 파일 형식입니다. 웹 글꼴의 파일 크기를 줄이는 방법으로 개발되어 더 빠르게 로드하고 더 적은 대역폭을 사용할 수 있습니다. WOFF2는 Brotli라는 압축 알고리즘을 사용하여 글꼴 데이터를 압축하므로 동등한 [WOFF](/ko/font/woff/) 글꼴보다 파일 크기가 훨씬 작을 수 있습니다. 이 형식은 Chrome, Firefox, Safari, Opera 및 Edge(버전 14 이후)를 포함한 대부분의 최신 웹 브라우저에서 지원됩니다.

## WOFF2 파일 형식 - 추가 정보

WOFF2 글꼴 파일의 내부 파일 구조는 헤더, 메타데이터, 테이블 디렉터리 및 글꼴 데이터 자체를 비롯한 여러 부분으로 구성됩니다.

1. 헤더에는 버전 번호와 파일에 있는 테이블 수를 포함하여 파일의 전체 형식에 대한 정보가 들어 있습니다.

1. 메타데이터 섹션에는 글꼴 이름, 저작권 및 기타 글꼴 관련 정보가 포함되어 있습니다.

1. 테이블 디렉토리에는 파일에서의 위치 및 길이를 포함하여 글꼴을 구성하는 다양한 테이블에 대한 정보가 들어 있습니다.

1. 글꼴 데이터 자체는 여러 개의 다른 테이블로 나뉘며 각 테이블에는 문자 및 해당 글리프와 같은 글꼴에 대한 특정 정보가 포함되어 있습니다. 이 테이블에는 다음이 포함될 수 있습니다.

* 'glyf' 테이블에는 각 문자의 모양과 크기를 포함한 실제 글꼴 윤곽선이 포함되어 있습니다.
* 'head' 테이블에는 버전 번호, 디자인 크기 등과 같은 글꼴에 대한 일반 정보가 들어 있습니다.
* 'hmtx' 테이블에는 문자의 너비와 위치를 포함하여 글꼴의 메트릭에 대한 정보가 포함되어 있습니다.
* 각 테이블은 인코딩이 완료된 후 압축되어 WOFF2 파일 형식으로 저장됩니다.

전반적인 구조는 웹 브라우저가 빠르고 효율적으로 글꼴을 로드하고 웹 사이트에 표시할 수 있도록 빠른 구문 분석 및 디코딩이 가능하도록 설계되었습니다.

### WOFF2 헤더
WOFF 헤더는 파일에 포함된 데이터의 종류를 나타내는 식별 서명으로 구성됩니다. 해당 필드와 함께 WOFF 헤더는 다음과 같습니다.

|유형|필드 이름|설명|
---|---|---|
|UInt32|서명 |0x774F4632 'wOF2' |
|UInt32| flavor |입력 글꼴의 "sfnt 버전"입니다.|
|UInt32| 길이 |WOFF 파일의 총 크기.|
|UInt16| numTables |폰트 테이블 디렉토리의 항목 수.|
|UInt16| 예약됨 |예약됨; 0으로 설정.|
|UInt32| totalSfntSize |sfnt 헤더, 디렉토리 및 글꼴 테이블(패딩 포함)을 포함하여 압축되지 않은 글꼴 데이터에 필요한 총 크기.|
|UInt32| totalCompressedSize 압축된 데이터 블록의 총 길이.|
|UInt16| majorVersion |WOFF 파일의 주 버전.|
|UInt16| minorVersion |WOFF 파일의 부 버전.|
|UInt32| metaOffset |WOFF 파일 시작부터 메타데이터 블록까지의 오프셋.|
|UInt32| metaLength |압축된 메타데이터 블록의 길이.|
|UInt32| metaOrigLength |메타데이터 블록의 압축되지 않은 크기.|
|UInt32| privOffset |WOFF 파일의 시작부터 개인 데이터 블록까지의 오프셋.|
|UInt32| privLength |비공개 데이터 블록의 길이.|


## 참조
* [w3 WOFF2 파일 형식](https://www.w3.org/TR/WOFF2/)
