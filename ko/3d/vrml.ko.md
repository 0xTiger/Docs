{
  "date" : "2019-10-11",
  "keywords" :[ "vrml 파일", "vrml 파일 형식", "vrml 파일이란", "파일", "vrml 예제", "vrml 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VRML 파일 형식",
  "description":"VRML 파일 형식과 VRML 파일을 열고 생성할 수 있는 API에 대해 알아보세요.",
  "linktitle" : "VRML",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## .VRML 파일이란?
VRML(가상 현실 모델링 언어)은 월드 와이드 웹(www)을 통해 대화형 [3D](/ko/3d/) 세계 개체를 표현하기 위한 파일 형식입니다. 일러스트레이션, 정의 및 가상 현실 프레젠테이션과 같은 복잡한 장면의 3차원 표현을 만드는 데 사용됩니다. 형식은 [X3D](/ko/3d/x3d/)로 대체되었습니다. 많은 3D 모델링 응용 프로그램은 객체와 장면을 VRML 형식으로 저장할 수 있습니다.

## VRML 파일 형식

VRML은 표면 색상, UV 매핑된 텍스처, 광택, 투명도 등과 같은 정보와 함께 3D 다각형의 꼭짓점 및 가장자리와 같은 정보를 지정하는 텍스트 파일 형식입니다. 사운드, 영화 및 이미지와 같은 다른 미디어에 대한 하이퍼링크를 갖는 것 외에도 정적 및 애니메이션 개체를 나타내는 기능이 있습니다. 이렇게 하면 사용자가 이러한 개체를 클릭할 때 하이퍼링크된 요소를 열 수 있습니다.

일반적인 용어로 TVRML 파일은 "세계"라고 하며 확장자가 .wrl입니다. 이러한 파일의 텍스트 특성으로 인해 gzip과 같은 압축 형식을 사용하여 파일 크기를 줄일 수 있으므로 인터넷을 통해 빠르게 전송할 수 있습니다. [VRML v 2.0](http://gun.teipir.gr/VRML-amgem/spec/index.html)의 파일 형식 사양은 이러한 파일을 읽고 쓸 수 있는 응용 프로그램을 만들기 위한 개발자 참조 역할을 합니다.

## 디자인 기준 ##

VRML의 목표와 설계는 다음 요구 사항을 중심으로 이루어집니다.

* **권한성** - 애플리케이션 생성기 및 편집기를 개발하고 다른 산업 형식에서 데이터를 가져올 수 있습니다.
* **완벽성** - 구현에 필요한 모든 정보를 제공하고 광범위한 업계 수용을 위한 완전한 기능 세트를 해결합니다.
* **구성 가능성** - VRML의 요소를 조합하여 사용하여 재사용이 가능하도록 하는 기능.
* **확장성** - 새로운 요소를 추가하는 기능.
* **구현 가능성** - 광범위한 시스템에서 구현 가능.
* **다중 사용자 가능성** - 다중 사용자 환경의 구현을 배제해서는 안 됩니다.
* **직교성** - VRML의 요소는 서로 독립적이거나 모든 종속성이 구조화되고 잘 정의되어야 합니다.
* **성능** - 요소는 다양한 컴퓨팅 플랫폼에서 대화형 성능에 중점을 두고 설계되어야 합니다.
* **확장성** - VRML의 요소는 무한히 큰 구성을 위해 설계되어야 합니다.
* **표준 관행** - 기존 관행을 반영하거나 기존 관행을 지원하는 데 필요하거나 제안된 표준을 지원하는 데 필요한 요소만 표준화해야 합니다.
* **잘 구조화됨** - 요소는 잘 정의된 인터페이스와 단순하게 명시된 무조건적인 목적을 가져야 합니다. 다목적 요소와 부작용은 피해야 합니다.

## 참조 ##

* [VRML - 위키피디아 작성](https://en.wikipedia.org/wiki/VRML)
* [VRML v 2.0 파일 형식 사양](http://gun.teipir.gr/VRML-amgem/spec/index.html)
