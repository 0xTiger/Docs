{
"날짜": "2023-06-08",
  "keywords": [
"crx 파일",
"crx 파일이 무엇인가요?",
"Google 크롬에 crx 파일을 설치하는 방법",
"crx 파일을 여는 방법",
"crx 파일에는 무엇이 포함되어 있나요?",
"crx 파일의 형식은 무엇입니까",
"파일",
"crx 파일 확장자",
"확대"
],
  "author": {
"display_name": "샤킬 파이즈"
},
"draft": "false",
"toc": true,
"title": "CRX 파일 형식 - Google Chrome 확장 프로그램",
  "description":"CRX 파일을 생성하고 열 수 있는 CRX 형식과 API에 대해 알아보세요.",
"linktitle": "CRX",
  "menu": {
    "docs": {
      "identifier": "misc-crx",
"parent" : "misc"
}
},
"lastmod": "2023-06-08"
}

## .CRX 파일이란?

CRX 파일 형식은 Google Chrome 브라우저 확장 프로그램과 연결되어 있습니다. CRX 파일은 기본적으로 Google Chrome에서 확장 프로그램을 설치하고 실행하는 데 필요한 파일과 메타데이터가 포함된 압축 패키지입니다. 추가 기능이나 테마를 제공하여 웹 브라우저의 기능이나 모양을 향상시킵니다.

CRX 파일이 Google Chrome에 다운로드되어 설치되면 브라우저는 공개 키와 서명을 사용하여 확장 프로그램의 무결성을 확인합니다. 확인에 성공하면 Chrome은 CRX 파일의 콘텐츠를 추출하고 확장 프로그램을 설치하여 사용할 수 있도록 합니다. 사용자는 설치된 확장 프로그램을 활성화, 비활성화 또는 제거할 수 있는 Chrome 확장 프로그램 페이지를 통해 확장 프로그램을 관리할 수 있습니다.

## Google Chrome에 CRX 파일을 설치하는 방법은 무엇입니까?

Google Chrome에 CRX 파일을 설치하려면 다음 단계를 따르세요.

1. 크롬 브라우저를 엽니다.
2. 주소 표시줄에 `chrome://extensions`를 입력하고 Enter를 누르세요.
3. 확장 프로그램 페이지 오른쪽 상단에 있는 "개발자 모드" 토글 스위치를 활성화합니다.
4. "압축해제된 항목 로드" 버튼을 클릭합니다.
5. CRX 파일의 추출된 내용이 포함된 폴더를 찾아서 선택합니다(또는 간단히 CRX 파일 자체를 선택합니다).
6. 확장 프로그램을 설치하려면 "열기"를 클릭하세요.

## CRX 파일에는 무엇이 포함되어 있나요?

CRX 파일에는 Google Chrome 확장 프로그램에 필요한 파일과 메타데이터가 포함되어 있습니다. 다음은 CRX 파일 내에서 발견되는 일반적인 내용에 대한 분석입니다.

- **매니페스트 파일(manifest.json):** JSON 형식의 파일로 이름, 버전, 설명, 권한, 백그라운드 스크립트 등 확장자에 대한 정보가 포함되어 있습니다. 확장의 구조와 동작을 정의합니다.
- **JavaScript 파일:** 이 파일에는 확장 기능을 정의하는 코드가 포함되어 있습니다. 여기에는 이벤트 처리, 웹페이지 수정, Chrome API와의 상호작용을 위한 스크립트가 포함될 수 있습니다.
- **HTML, CSS 및 이미지 파일:** 확장 프로그램에는 팝업 창이나 옵션 페이지와 같은 사용자 인터페이스 요소가 포함되는 경우가 많습니다. HTML 파일은 이러한 인터페이스의 구조를 정의하고 CSS 파일은 인터페이스의 모양을 제어합니다. 이미지 파일은 아이콘이나 기타 그래픽 자산에 사용됩니다.
- **선택적 리소스 파일:** 확장 프로그램에는 여러 언어를 지원하기 위한 현지화 파일과 같은 추가 리소스가 포함될 수 있습니다. 이 파일에는 확장 프로그램의 사용자 인터페이스에 사용되는 텍스트 번역이 포함되어 있습니다.
- **백그라운드 스크립트:** 확장 프로그램에 활성 웹 페이지와 독립적으로 실행되는 백그라운드 프로세스나 스크립트가 있는 경우 이러한 스크립트는 CRX 파일에 포함됩니다.
- **콘텐츠 스크립트:** 콘텐츠 스크립트는 웹페이지의 동작을 수정하거나 콘텐츠와 상호 작용하기 위해 웹페이지에 삽입할 수 있는 스크립트입니다. 확장 프로그램이 콘텐츠 스크립트를 사용하는 경우 해당 스크립트에 필요한 파일이 CRX 파일에 있습니다.
- **기타 자산:** 확장의 특정 요구 사항에 따라 오디오 또는 비디오 파일, 글꼴, 데이터 파일과 같은 추가 파일이 포함될 수 있습니다.

CRX 파일 형식은 본질적으로 이러한 모든 파일과 폴더를 구조화된 방식으로 포함하는 압축 패키지입니다. CRX 파일이 Google Chrome에 설치되면 브라우저는 콘텐츠를 추출하여 적절한 위치에 배치하여 브라우저 내에서 확장 프로그램을 로드하고 실행할 수 있도록 합니다.

## CRX 파일의 형식은 무엇입니까?

CRX 파일 형식은 Google Chrome 확장 프로그램을 패키징하고 배포하기 위한 특정 형식입니다. 본질적으로 파일 확장자가 다른 압축된 ZIP 아카이브입니다. CRX 파일의 기본 구조는 다음과 같습니다.

- **파일 서명:** 파일의 처음 4바이트에는 해당 파일을 CRX 파일로 식별하는 서명 역할을 하는 매직 넘버 "Cr24"(16진수: 43 72 32 34)가 포함되어 있습니다.
- **버전 번호:** 다음 4바이트는 CRX 형식의 버전 번호를 나타냅니다.
- **공개 키 길이:** 다음 4바이트는 확장 서명 확인에 사용되는 인코딩된 공개 키의 길이를 나타냅니다.
- **서명 길이:** 후속 4바이트는 확장의 서명 길이를 지정합니다.
- **공개 키:** 이 섹션에는 확장 프로그램의 무결성을 확인하는 데 사용되는 인코딩된 공개 키가 포함되어 있습니다.
- **서명:** 이 섹션에는 위에서 언급한 공개 키에 해당하는 개인 키를 사용하여 확장 프로그램의 내용에 서명하여 생성된 확장 프로그램의 서명이 포함되어 있습니다.
- **ZIP 아카이브:** CRX 파일의 나머지 바이트는 압축된 ZIP 아카이브로 구성됩니다. 이 아카이브에는 매니페스트 파일, JavaScript 파일, HTML 파일, CSS 파일, 이미지 및 기타 리소스를 포함하여 필요한 모든 파일과 확장 폴더가 포함되어 있습니다.

## 참고자료
* [CRX 형식 사양](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/K3YIsNL_Et4)

