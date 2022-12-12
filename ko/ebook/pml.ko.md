{
  "date" : "2021-03-08",
  "keywords" :[ "PML", "eReader", "확장", "형식", "eBook", "팜 마크업 언어" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"PML 파일 형식, Palm Markup Language 및 PML 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "title" :"PML - Palm 마크업 언어 파일",
  "linktitle" : "PML",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-08"
}

## .PML 파일이란?

Palm Inc는 Palm Markup Language File의 약자인 PML 파일 형식을 도입했습니다. 그 목적은 태블릿 컴퓨터와 유사한 eBook 읽기 장치인 eReader용 문서를 만드는 것입니다. PML 파일은 [PDB](/ko/ebook/pdb/) 파일(다양한 데이터 파일 포함)에 레이아웃을 제공하여 Palm 장치에 표시합니다.

## PML 파일의 기술적 세부 사항

PML 파일의 구조는 단락, 제목, 들여쓰기 및 참조를 포함하여 eBook 설정을 생성하기 위한 태그로 구성됩니다. 또한 굵게, 작은 대문자 및 위 첨자와 같은 서식 지정 태그를 허용합니다. 개발자는 eBook에 이미지를 추가할 수도 있습니다.

### 팜 마크업 언어
다음 표는 PML 명령을 지정합니다.

|명령|설명|
---|---|
| \p | 새 페이지 |
| \x | 새로운 장; 또한 새 페이지 나누기가 발생합니다. 장 제목(및 모든 스타일 코드)을 \x 및 \x |
| \Xn | 챕터 대화 상자에서 새 챕터, 들여쓰기 n 레벨(n은 0에서 4까지 포함); 페이지 나누기가 발생하지 않습니다. 장 제목(및 모든 스타일 코드)을 \Xn 및 \Xn으로 묶습니다. |
| \Cn="챕터 제목" | \Xn과 같이 레벨 n으로 "챕터 제목"을 챕터 목록에 삽입합니다. 텍스트는 페이지에 표시되지 않으며 강제로 페이지를 나누지 않습니다. 이것은 예를 들어 장의 소개 시작 부분에 챕터 표시를 삽입하는 데 유용할 수 있습니다. |
| \c | 이 텍스트 블록을 가운데에 맞춥니다. 줄의 시작 부분에 \c로 닫기 |
| \r | 텍스트 블록을 오른쪽으로 정렬합니다. 줄의 시작 부분에 \r로 닫기 |
| \i | 블록을 기울임꼴로 표시합니다. 닫기 \i |
| \u | 밑줄 블록; 닫기 \u |
| \o | 오버스트라이크 블록; 닫기 \o |
| \v | 보이지 않는 텍스트; \v로 닫습니다(주석에 사용할 수 있음) |
| \t | 들여쓰기 블록. 줄 시작 부분에서 시작하고 줄 끝에서 \t로 닫음 |
| \T="50%" | 화면 너비의 지정된 백분율(이 경우 50%)을 들여씁니다. 현재 그리기 위치가 이미 지정된 화면 위치를 지난 경우 이 태그는 무시됩니다. |
| \w="50%" | 화면의 주어진 백분율 너비(이 경우 50%)의 수평선을 포함합니다. 이 태그는 앞뒤에 줄 바꿈을 발생시킵니다. 규칙은 중앙에 있습니다. 백분율 기호는 필수입니다. |
| \n | 사용자가 지정한 "일반" 글꼴로 전환 |
| \s | stdFont로 전환하십시오. 일반 글꼴로 되돌리려면 \s로 닫습니다. |
| \b | 굵은 글꼴로 전환하십시오. 일반 글꼴로 되돌리려면 \b로 닫으십시오(더 이상 사용되지 않음, 대신 \B 사용) |
| \l | LargeFont로 전환하십시오. 일반 글꼴로 되돌리려면 \l로 닫습니다. |
| \B | 텍스트를 굵게 표시합니다. \b 태그와 달리 \B는 글꼴을 변경하지 않으므로 큰 굵은 텍스트를 사용할 수 있습니다. 동일한 PML 파일에서 \b와 \B를 혼합할 수 없습니다. |
| \Sp | 텍스트를 위 첨자로 표시합니다. 굵게, 기울임꼴 등과 같은 다른 스타일과 혼합해서는 안 됩니다. \Sp로 위첨자 텍스트를 묶습니다. |
| \Sb | 텍스트를 아래 첨자로 표시합니다. 굵게, 기울임꼴 등과 같은 다른 스타일과 혼합해서는 안 됩니다. 아래 첨자 텍스트를 \Sb로 묶습니다. |
| \k | 동봉된 텍스트를 작은 대문자로 만듭니다. \k로 닫습니다. \k 태그로 묶인 모든 문자(액센트가 있는 문자 포함)는 대문자로 만들어지고 일반 대문자보다 작은 포인트 크기로 렌더링됩니다. |
| \\ | 단일 백슬래시를 나타냅니다 |
| \aXXX | Windows-1252 코드가 10진수 XXX인 비 ASCII 문자를 삽입하십시오. 자세한 내용은 PML 문자표를 참조하십시오. |
| \UXXXX | 유니코드 코드가 16진수 XXXX인 비 ASCII 문자를 삽입하십시오. 자세한 내용은 확장 PML 문자 테이블을 참조하십시오. |
| \m="이미지 이름.png" | 명명된 이미지를 삽입합니다. 아래 이미지 섹션을 참조하십시오. |
| \q="#linkanchor"텍스트\q | 문서의 다른 지점에 있는 링크 앵커를 참조하십시오. 앵커 사양 뒤와 후행 \q 앞의 문자열은 밑줄이 그어져 있거나 문서를 볼 때 링크로 표시됩니다. |
| \Q="링크 앵커" | 문서에 링크 앵커를 지정합니다. |
| \- | 부드러운 하이픈을 삽입합니다. 부드러운 하이픈은 줄을 가로질러 단어를 분리해야 하는 경우에만 나타납니다. |
| \Fn="각주1"1\Fn | 이름이 footnote1이고 PML 문서 끝에 태그가 지정된 각주에 "1"을 연결합니다. 아래의 각주 및 사이드바 섹션을 참조하십시오. |
| \Sd="sidebar1"사이드바\Sd | "사이드바" 텍스트를 PML 문서 끝에 태그가 지정된 sidebar1이라는 이름의 사이드바에 연결합니다. 아래의 각주 및 사이드바 섹션을 참조하십시오. |
| \나 | 참조 색인 항목으로 표시합니다. 색인 항목(및 모든 스타일 코드)을 \I 및 \I로 묶습니다.|
 


## 참고문헌

* [Palm Markup Language - By MobileRead](https://wiki.mobileread.com/wiki/EReader)
* [E-Reader - By MobileRead](https://en.wikipedia.org/wiki/E-reader)
