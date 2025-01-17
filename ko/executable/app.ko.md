{
"날짜": "2023-02-02",
  "keywords": [
"앱 파일",
"앱 파일이 무엇인가요?",
"파일",
"앱 파일을 여는 방법",
"앱 파일 확장자",
"확대"
],
  "author": {
"display_name": "샤킬 파이즈"
},
"draft": "false",
"toc": true,
  "description":"APP 파일 형식과 APP 파일을 생성하고 열 수 있는 API에 대해 알아보세요.",
"title": "APP 파일 형식 - macOS 애플리케이션 번들",
"linktitle": "APP",
  "menu": {
    "docs": {
      "identifier": "executable-app",
"parent" : "executable"
}
},
"lastmod": "2023-02-02"
}

## .APP 파일이란?

macOS의 .app 파일은 실행 코드, 리소스 및 메타데이터를 포함하여 특정 애플리케이션을 실행하는 데 필요한 모든 파일을 포함하는 특별한 유형의 디렉터리입니다. .app 확장자는 이 디렉토리가 별도의 파일 모음이 아닌 단일 단위로 처리되어야 하며 Finder 또는 Dock에서 직접 실행할 수 있음을 운영 체제에 알립니다.

Finder는 macOS의 기본 파일 관리자 응용 프로그램입니다. 이를 통해 컴퓨터의 파일과 디렉터리를 탐색하고 구성할 수 있습니다. Dock은 자주 사용하는 응용 프로그램과 문서에 빠르게 접근할 수 있는 macOS의 기능입니다. Finder와 Dock 모두 .app 파일을 클릭하여 애플리케이션을 시작할 수 있으며, 그러면 해당 애플리케이션 번들이 열립니다. 애플리케이션을 시작하면 .app 번들 내의 실행 코드가 실행되어 애플리케이션을 사용할 수 있게 됩니다. .app 파일은 파일 시스템의 애플리케이션을 나타내며 사용자가 애플리케이션에 액세스하고 실행할 수 있는 방법을 제공합니다.

macOS 시스템의 Finder에서 .app 파일을 마우스 오른쪽 버튼으로 클릭하고 "패키지 콘텐츠 표시"를 선택하면 애플리케이션 번들의 내부 구조를 볼 수 있습니다. 이는 응용 프로그램에서 사용하는 리소스나 파일에 액세스하려는 경우 또는 문제 해결을 위해 응용 프로그램의 내용을 검사하려는 경우에 유용합니다. .app 파일의 패키지 콘텐츠에는 일반적으로 이미지, 사운드 등의 리소스에 대한 디렉터리와 애플리케이션의 실행 코드가 포함됩니다. .app 파일의 콘텐츠를 탐색하면 애플리케이션이 어떻게 구성되고 무엇을 하는지에 대한 더 깊은 통찰력을 얻을 수 있습니다.

## APP 파일을 여는 방법은 무엇입니까?

macOS에서 .app 파일을 열려면 Finder에서 파일을 두 번 클릭하면 됩니다. 그러면 .app 번들에 포함된 애플리케이션이 시작됩니다. 응용 프로그램이 시스템에 설치되어 있고 .app 파일 형식과 연결된 경우 파일을 두 번 클릭하면 응용 프로그램이 자동으로 시작됩니다. 응용 프로그램이 .app 파일 형식과 연결되어 있지 않으면 파일을 마우스 오른쪽 버튼으로 클릭하고 "연결 프로그램"을 선택하여 파일을 여는 데 적합한 응용 프로그램을 선택해야 할 수도 있습니다.

"open" 명령을 사용하여 macOS의 터미널에서 .app 파일을 열 수 있습니다. 이렇게 하려면 "cd" 명령을 사용하여 .app 파일이 있는 디렉터리로 이동한 후 다음 명령을 실행합니다.

```
open <AppName>.app 
```

어디<AppName> 실행하려는 애플리케이션의 이름입니다. 그러면 Finder에서 두 번 클릭한 것처럼 응용 프로그램이 시작됩니다. "open" 명령은 응용 프로그램, 문서 및 디렉터리를 포함하여 다양한 유형의 파일을 여는 데 사용할 수 있는 범용 유틸리티입니다. .app 파일에서 "open" 명령을 사용하면 번들에 포함된 애플리케이션이 시작됩니다.

## 참고자료
* [Bundle (macOS)](https://en.wikipedia.org/wiki/Bundle_(macOS))
