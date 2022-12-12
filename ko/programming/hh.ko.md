{
  "date" : "2019-10-11",
  "keywords" :[ "h", ".hh",".hh 파일이란",".hh 파일을 여는 방법", "확장자", "파일", ".hh 파일",".hh 파일 형식", " .hh 파일 확장자",".HH 파일 예"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HH - C++ 헤더 파일 형식",
  "description":"HH 파일을 만들고 열 수 있는 HH 파일 형식과 API에 대해 알아보세요.",
  "linktitle" : "HH",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-20"
}

## .HH 파일이란?

확장자가 .hh인 파일은 변수, 상수 및 함수 선언을 포함하는 C++ 헤더 파일입니다. 이러한 선언은 해당 C++ 구현 파일에서 사용되며 일반적으로 사용자 논리의 실제 구현을 포함하는 [.cpp](/ko/programming/cpp/) 파일로 저장됩니다. .hh 헤더 파일은 `#include` 지시문을 사용하여 구현 CPP 파일에서 참조됩니다. C++ 프로젝트에 가능한 한 많은 헤더 파일을 추가하여 프로젝트 수준 선언을 포함할 수 있습니다.

## .HH 파일 형식

.hh 파일은 헤더 파일 정의 규칙을 유지하면서 생성되는 일반 텍스트 파일입니다. .hh 파일에 선언된 가장 일반적인 정보는 다음과 같습니다.

**`변수`** - 객체 지향 프로그래밍(OOP)의 경우 클래스 헤더 파일에는 구현 소스 코드 파일에서 액세스할 수 있는 모든 클래스 수준 변수의 정의가 포함됩니다.
**`메소드 선언`** - 모든 메서드 선언은 여러 구현 파일에서 액세스할 수 있도록 .h 헤더 파일에 포함됩니다.
**`비인라인 함수 정의`** - 헤더 파일에는 인라인이 아닌 메서드의 정의도 포함될 수 있습니다.
**`Message Maps`** - 헤더 파일에는 MFC 소스 코드 구현의 경우 메시지 맵도 포함될 수 있습니다. 이러한 경우 메시지 맵은 버튼, 체크박스, 라디오 버튼 등과 같은 UI 요소에 연결된 기능 구현에 연결됩니다.

## .H와 .HH 파일의 차이점

분명히, [C](/ko/programming/c/) 또는 C++와 같은 각 언어에 대해 권장되는 사용 방법 외에는 .h 및 .hh 헤더 파일 사이에 그러한 차이가 없습니다. 이러한 언어에 따라 헤더 파일의 이름을 지정하면 C 및 C++ 구현이 혼합될 수 있는 대규모 프로젝트에서 이들을 구별하는 데 도움이 됩니다.

또한 헤더가 확장자로 구분된 경우 편집기는 각각에 대해 적절한 형식을 자동으로 적용할 수 있습니다.

전반적으로 이 두 파일 형식을 구분하는 것은 아무런 해를 끼치지 않지만 유리하며 C 및 C++ 구분을 위해 따르는 것이 좋습니다.

### 헤더 가드

헤더 파일은 다른 헤더 파일을 추가한 결과로 동일한 파일에 여러 선언이 포함되는 복잡한 오류를 일으킬 수 있습니다. 이 중복 정의는 컴파일러 오류를 발생시킵니다. 이 문제가 있는 상황은 아래와 같이 조건부 컴파일 지시문인 헤더 가드라는 메커니즘을 통해 피할 수 있습니다.

```
#ifndef ANY_UNIQUE_NAME_HERE_HPP
#define ANY_UNIQUE_NAME_HERE_HPP

// your declarations (and certain types of definitions) here

#endif
```
이 헤더를 사용하여 전처리기는 `ANY_UNIQUE_NAME_HERE_HPP`가 이미 정의되었는지 여부를 확인합니다. 헤더가 동일한 파일에 반복적으로 포함되는 경우 헤더의 내용은 무시됩니다.

## 참고문헌

* [헤더 파일러 - Microsoft](https://docs.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)
* [.h 및 .hh 파일 형식의 차이점](https://stackoverflow.com/questions/10354321/c-reason-why-using-hh-as-extension-for-c-header-files)
