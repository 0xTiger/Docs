{
  "date" : "2020-11-11",
  "keywords" :[ "ACCDT", "확장자", "파일", "파일 형식", "데이터베이스 파일 형식", "데이터베이스 파일 형식", "데이터베이스 파일" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"ACCDT 파일 형식과 ACCDT 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "title" :"ACCDT - Microsoft Access 2007 템플릿 데이터베이스 파일 형식",
  "linktitle" : "ACCDT",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-12"
}

## .ACCDT 파일이란?

확장자가 .accdt인 파일은 미리 정의된 데이터베이스 요소가 포함된 Microsoft Access 데이터베이스 템플릿 파일입니다. 이러한 요소는 데이터 저장을 위한 데이터베이스 스키마, 데이터 보기에 대한 레이아웃 설명, 데이터베이스를 설명하는 메타데이터와 같은 데이터베이스 응용 프로그램을 정의하는 구조 모음입니다. 템플릿 파일이기 때문에 ACCDT 파일은 사용 가능한 템플릿 설정을 기반으로 데이터베이스를 만드는 데 사용할 수 있습니다. 결과 데이터베이스 파일은 [ACCDB](/ko/database/accdb/) 파일로 저장되고 테이블의 데이터로 채워집니다. Microsoft Access 2007 이상에서는 ACCDT 파일을 열 수 있습니다.

## ACCDT 파일 형식

ACCDT 템플릿 파일은 Office Open XML 사양을 기반으로 하며 모든 데이터는 ZIP 패키지에 포함되어 있습니다. 데이터베이스의 구조 및 내용 정보는 [XML](/ko/web/xml/) 파일 및 텍스트 파일에 포함되어 있으며 관계를 통해 서로 연결됩니다. ACCDT 파일의 이름을 [.zip](/ko/compression/zip/) 확장자로 바꾸고 압축 소프트웨어를 사용하여 ZIP 아카이브의 내용을 추출할 수 있습니다.

### 파일 구조

ACCDT 파일은 관련 부품 모음을 포함하는 패키지입니다. 각 **부분**은 다음을 포함하는 XML, 텍스트 및 이진 형식을 사용하여 데이터베이스 응용 프로그램의 내용에 대한 정보를 저장합니다.

* 데이터베이스 객체
* 관련 메타데이터
* 패키지 구조

#### 패키지

패키지는 여러 부분을 포함하고 [ISO/IEC-29500-2](https://go.microsoft.com/fwlink/)에 지정된 개방형 패키징 규칙을 준수하는 [ZIP](/ko/compression/zip/) 아카이브입니다. ?링크 ID=150883). ACCDT 파일에는 관계의 대상이 되어야 하는 템플릿 메타데이터 부분이 하나 이상 포함되어야 합니다. 이 템플릿 메타데이터는 ACCDT 파일의 시작 부분입니다.

#### 부분

부분은 그 안에 저장된 콘텐츠의 성격과 유형을 지정하기 위한 관련 유형이 있는 바이트 스트림입니다. 부품 열거는 유효한 부품, 유효한 콘텐츠 유형 및 패키지의 모든 부품 간의 필수 관계를 지정합니다.

#### 관계

'패키지 관계' - 여기서 대상은 일부이고 소스는 전체 패키지입니다.

'부품 대 부품 관계' - 여기서 대상은 부품이고 소스는 패키지의 부품입니다.

'명시적 관계' - ID 속성 값으로 관계 요소를 참조하여 소스 부분의 내용에서 리소스를 참조하는 경우.

'암시적 관계' - 명시적이지 않은 관계입니다.

'내부 관계' - 대상이 패키지의 일부인 경우.

'외부 관계' - 대상이 패키지에 없는 외부 리소스인 경우.

## 참조 ##

* [액세스 템플릿 파일 형식](https://docs.microsoft.com/en-us/openspecs/sharepoint_protocols/ms-accdt/0a4a68d7-7a85-4a27-ad74-730db57862d7)
