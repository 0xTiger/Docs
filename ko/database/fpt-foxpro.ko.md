{
"날짜": "2023-06-12",
  "keywords": [
"fpt",
"FPT 파일",
"폭스프로 FPT 파일",
"FoxPro 테이블 메모",
"FPT 파일이 무엇인가요?",
"FPT 파일 여는 방법",
"파일",
"FPT 파일 확장자",
"확대"
],
  "author": {
"display_name": "샤킬 파이즈"
},
"draft": "false",
"toc": true,
"title": "FPT 파일 형식 - FoxPro 테이블 메모",
  "description":"FPT 파일을 생성하고 열 수 있는 FPT FoxPro 형식과 API에 대해 알아보세요.",
"linktitle": "FPT FoxPro",
  "menu": {
    "docs": {
      "identifier": "database-fpt-foxpro",
"parent" : "database"
}
},
"lastmod": "2023-06-12"
}

## .FPT 파일이란?

"FPT" 파일은 FoxPro 데이터베이스 관리 시스템과 관련된 파일 확장자입니다. FoxPro의 FPT 파일에는 테이블과 연결된 메모 필드가 포함되어 있습니다. 메모 필드는 일반 데이터베이스 필드에 맞지 않을 수 있는 긴 설명, 문서 또는 이미지와 같은 대량의 텍스트 또는 이진 데이터를 저장하는 데 사용됩니다.

FoxPro 파일 구조의 작동 방식은 다음과 같습니다.

- **DBF(데이터베이스 파일):** 일반 필드를 포함하여 테이블 형식의 구조화된 데이터가 포함된 기본 파일입니다. 각 레코드는 테이블의 행에 해당하고, 레코드 내의 각 필드는 열에 해당합니다.

- **FPT(메모 파일):** FPT 파일은 DBF 파일의 기록과 관련된 메모 필드를 저장하는 데 사용됩니다. 각 메모 필드는 DBF 파일의 기록에 해당하며 FPT 파일은 실제 메모 내용을 저장합니다.

- **CDX(인덱스 파일):** DBF 파일에서 데이터 검색 및 정렬 성능을 향상시키는 인덱스가 저장되는 파일입니다.

메모 필드가 있는 FoxPro 데이터베이스가 있는 경우 각 테이블에 해당하는 DBF, FPT 및 CDX 파일이 있어야 합니다. FPT 파일에는 이진 데이터가 포함되어 있으며 텍스트 편집기로 직접 열 수 없습니다. 대신 FoxPro 응용 프로그램이나 기타 호환 가능한 데이터베이스 도구를 통해 액세스하고 관리합니다.

## FoxPro와의 관계

FPT 파일은 원래 Fox Software에서 개발하고 나중에 Microsoft에서 인수한 관계형 데이터베이스 관리 시스템(DBMS)인 FoxPro와 연결되어 있습니다. 다양한 버전으로 제공되며 가장 잘 알려진 버전 중 하나는 Visual FoxPro(VFP)입니다. Visual FoxPro는 데스크톱 및 클라이언트-서버 응용 프로그램 개발에 사용되는 강력하고 인기 있는 데이터베이스 관리 시스템이었습니다.

Visual FoxPro의 주요 기능은 다음과 같습니다.

- **테이블 형식 데이터 저장소:** 사용자는 다른 데이터베이스 시스템과 유사한 필드와 레코드를 사용하여 테이블 형식의 구조화된 데이터를 생성하고 관리할 수 있습니다.
- **메모 필드 지원:** Visual FoxPro는 대량의 텍스트 또는 이진 데이터를 저장할 수 있는 메모 필드를 지원했습니다.
- **대화형 개발 환경:** 그래픽 인터페이스를 사용하여 양식, 보고서, 애플리케이션을 디자인할 수 있는 시각적 개발 환경을 갖추고 있었습니다.
- **SQL 지원:** Visual FoxPro는 표준 SQL 구문을 사용하여 데이터를 쿼리하고 조작할 수 있는 SQL(구조적 쿼리 언어)을 지원합니다.
- **객체 지향 프로그래밍:** Visual FoxPro는 객체 지향 프로그래밍을 지원하므로 보다 모듈화되고 유지 관리가 쉬운 응용 프로그램을 만들 수 있습니다.
- **인덱싱 및 검색:** 데이터를 더 빠르게 검색하고 정렬할 수 있도록 인덱싱 기능을 제공했습니다.
- **보고 도구:** Visual FoxPro에는 데이터베이스에 저장된 데이터를 기반으로 보고서를 생성하고 생성하기 위한 도구가 포함되어 있습니다.
- **호환성:** 다른 Microsoft 제품 및 기술과의 통합이 가능했습니다.

Microsoft는 2007년에 Visual FoxPro에 대한 주류 지원을 종료하고 2015년에 확장 지원을 종료했습니다. 즉, FoxPro를 사용하여 개발된 기존 응용 프로그램은 계속 작동할 수 있지만 Microsoft에서 제공하는 공식 업데이트나 보안 패치는 없습니다. 더욱이 현대 개발 추세는 웹 기반 및 클라우드 기반 애플리케이션으로 전환되었으며 새로운 데이터베이스 관리 시스템이 등장했습니다.

## FPT 파일을 여는 방법?

FPT 파일을 여는 프로그램은 다음과 같습니다

- 마이크로소프트 비주얼 폭스프로(유료)

## 기타 FPT 파일

- [FPT - Alpha Five 테이블 메모 파일](/ko/database/fpt-alphafive/)
- [FPT - FileMaker Pro 데이터베이스 메모 파일](/ko/database/fpt/)

## 참고자료
* [비주얼 폭스프로](https://en.wikipedia.org/wiki/Visual_FoxPro)

