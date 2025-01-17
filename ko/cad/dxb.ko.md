{
"날짜": "2023-05-10",
  "keywords": [
"dxb 파일",
"dxb 파일이 무엇인가요?",
"dxb 파일의 형식은 무엇입니까",
"dxb 파일에는 무엇이 포함되어 있나요?",
"파일",
"dxb 파일 확장자",
"확대"
],
  "author": {
"display_name": "샤킬 파이즈"
},
"draft": "false",
"toc": true,
"title": "DXB 파일 형식 - 도면 교환 바이너리",
  "description":"DXB 파일을 생성하고 열 수 있는 DXB 형식과 API에 대해 알아보세요.",
"linktitle": "DXB",
  "menu": {
    "docs": {
      "identifier": "cad-dxb",
"parent" : "cad"
}
},
"lastmod": "2023-05-10"
}

## .DXB 파일이란?

DXB는 Drawing Exchange Binary의 약자로 CAD(컴퓨터 지원 설계) 소프트웨어에 사용되는 파일 형식입니다. DXB 파일에는 2D 벡터 그래픽을 나타내는 이진 데이터가 포함되어 있으며 서로 다른 CAD 프로그램 간에 도면을 교환하는 데 사용됩니다. 일반적으로 CAD 프로그램에서 도면을 DXB 형식으로 내보낸 다음 다른 CAD 프로그램으로 가져와서 생성됩니다.

DXB 형식은 오늘날 DXF 또는 DWG와 같은 다른 CAD 파일 형식보다 덜 일반적으로 사용됩니다. 그러나 일부 이전 CAD 프로그램에서는 도면을 내보내거나 가져오기 위한 파일 형식으로 여전히 DXB를 사용할 수 있습니다.

DXB 파일이 있고 이를 보거나 편집해야 하는 경우 DXB 형식을 지원하는 CAD 프로그램이 필요합니다. DXB를 지원하는 CAD 프로그램의 예로는 AutoCAD, DraftSight 및 LibreCAD가 있습니다.

## DXB 파일 형식 - 추가 정보

DXB(드로잉 교환 바이너리)는 서로 다른 소프트웨어 응용 프로그램 간에 CAD 도면을 교환하기 위한 표준 형식인 DXF(드로잉 교환 형식) 파일 형식의 바이너리 버전입니다.

DXB 파일에는 DXF 파일과 마찬가지로 2D 벡터 그래픽을 나타내는 바이너리 데이터가 포함되어 있습니다. 그러나 DXB 파일은 일반 텍스트 대신 바이너리 형식으로 저장되므로 DXF 파일보다 더 작고 로드 속도가 빠릅니다.

DXB 파일을 생성하기 위해 CAD 프로그램은 도면을 DXB 형식으로 내보낼 수 있으며, 이는 DXB를 지원하는 다른 CAD 프로그램에서 읽을 수 있는 바이너리 파일을 생성합니다. 마찬가지로 DXB 파일을 가져오기 위해 CAD 프로그램은 바이너리 데이터를 읽고 편집을 위해 자체 내부 형식으로 변환할 수 있습니다.

## DXB 파일의 형식은 무엇입니까?

DXB(드로잉 교환 바이너리) 파일 형식은 바이너리 파일 형식으로 컴퓨터에서 직접 해석할 수 있는 바이너리 데이터로 구성됩니다.

DXB에서 사용하는 바이너리 형식은 다양한 소프트웨어 응용 프로그램 간에 CAD 도면을 교환하는 데에도 사용되는 텍스트 기반 DXF(도면 교환 형식) 파일 형식보다 더 컴팩트하고 로드 속도가 빠릅니다.

DXB 파일의 구조는 도면의 단일 개체 또는 엔터티를 나타내는 헤더와 데이터를 포함하는 일련의 이진 레코드로 구성됩니다. 헤더에는 데이터가 나타내는 개체 또는 엔터티의 유형과 크기 및 기타 속성에 대한 정보가 포함됩니다.

DXB 파일의 데이터는 도면의 하위 개체나 구성 요소를 나타내는 하위 수준 레코드에 대한 참조가 포함된 상위 수준 레코드를 사용하여 계층적으로 구성됩니다. 예를 들어, 폴리라인을 나타내는 레코드에는 폴리라인을 구성하는 개별 선 세그먼트를 나타내는 레코드에 대한 참조가 포함될 수 있습니다.

## DXB 파일에는 무엇이 포함되어 있습니까?

DXB(드로잉 교환 바이너리) 파일에는 CAD 도면을 구성하는 선, 호, 원, 텍스트 및 기타 기하학적 모양과 같은 2D 벡터 그래픽을 나타내는 바이너리 데이터가 포함되어 있습니다.

CAD 프로그램이 도면을 DXB 형식으로 내보낼 때 DXB를 지원하는 다른 CAD 프로그램에서 도면을 재생성하는 데 필요한 모든 정보가 포함된 이진 파일을 생성합니다. 여기에는 도면에 있는 각 객체의 위치, 크기, 색상 및 스타일에 대한 정보뿐만 아니라 포함될 수 있는 텍스트나 주석도 포함됩니다.

DXB 파일은 바이너리 형식으로 저장되므로 일반 텍스트로 저장되는 DXF(도면 교환 형식) 파일보다 일반적으로 크기가 더 작고 로드 속도가 더 빠릅니다. 그러나 DXB 파일은 DXB 형식을 지원하는 CAD 프로그램에서만 읽을 수 있는 반면, DXF 파일은 더 넓은 범위의 프로그램에서 읽을 수 있습니다.

## 참고자료
* [DXB 파일 형식](http://web.archive.org/web/20060824054154/https://www.autodesk.com/techpubs/autocad/acadr14/dxf/the_dxb_file_format_al_u05_b.htm)

