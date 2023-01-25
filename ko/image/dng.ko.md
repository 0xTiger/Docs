{
  "date" : "2019-10-11",
  "keywords" :[ "dng 파일", "dng 파일 형식", "dng 파일이란", "파일", "dng 예제", "dng 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DNG - 디지털 카메라 이미지 파일 형식",
  "description":"DNG 파일을 만들고 열 수 있는 DNG 파일 형식과 API에 대해 알아보세요.",
  "linktitle" : "DNG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## .DNG 파일이란?

DNG는 원시 파일의 저장에 사용되는 디지털 카메라 이미지 형식입니다. 2004년 9월 Adobe에서 개발했습니다. 기본적으로 디지털 사진용으로 개발되었습니다. DNG는 [TIFF](/ko/image/tiff/)/EP 표준 형식의 확장이며 메타데이터를 많이 사용합니다. 유연성과 예술적 제어가 용이하도록 디지털 카메라의 원시 데이터를 조작하기 위해 사진 작가는 Camera Raw 파일을 선택합니다. JPEG 및 TIFF 형식은 카메라에서 처리되는 이미지를 저장하므로 이러한 형식으로 변경할 수 있는 여지가 많지 않습니다.

## DNG 파일 형식의 역사 및 버전

지금까지 DNG 사양에는 5가지 버전이 있습니다. 버전 1.0.0.0은 "2.3"(ACR 및 DNG 변환기) 릴리스와 함께 2004년 9월에 출시되었습니다. 2005년 2월 버전 1.1.0.0이 게시되었습니다. 2008년 5월 버전 1.2.0.0이 출시되어 "4.4"에서 사용되었습니다. 버전 1.3.0.0은 2009년 6월에 게시되었습니다. 버전 1.4.0.0은 2012년에 나타났습니다.

## DNG 파일 형식

Camera Raw 파일은 센서에서 직접 처리되지 않거나 처리량이 적은 데이터를 캡처합니다. 필름 네거티브와 유사하므로 Camera Raw 형식은 "디지털 네거티브"라고도 합니다. 원시 형식의 이점은 최종 사용자의 예술적 제어가 향상된다는 것입니다. 사용자는 화이트 밸런스, 톤 매핑, 노이즈 감소, 샤프닝 등과 같은 요구 사항에 따라 다양한 매개변수 범위를 조정할 수 있습니다. 반면에 Camera Raw 파일은 모든 소프트웨어나 변환기를 통해 사용하기 위해 처리되어야 합니다.

따라서 Camera Raw 파일에 사용할 수 있는 표준 형식이 없었기 때문에 최종 사용자에게 여러 문제가 발생했습니다. 이러한 문제는 Adobe에서 해결했으며 Camera Raw 파일에 대해 비독점 형식을 정의했습니다. 형식은 디지털 네거티브 또는 DNG로 알려져 있습니다. DNG는 원시 파일 처리를 위해 다양한 하드웨어 및 소프트웨어에서 사용할 수 있습니다. 또한 DNG는 고유한 원시 형식이 있는 카메라로 원래 캡처한 이미지를 저장하기 위한 중간 형식으로도 사용할 수 있습니다.

### DNG 파일 형식 사양

이 섹션에서는 DNG 형식을 TIFF 6.0의 확장으로 설명합니다.

* **파일 확장자**: DNG는 ".DNG" 또는 ".TIF" 확장자를 사용합니다.
* **SubIFD 트리**: DNG는 SubIFD 체인을 지원하지 않습니다. 대신 DNG는 TIFF-EP 사양에 언급된 SubIFD 트리 사용을 권장합니다. 최고 품질 및 해상도는 0의 NewSubFileType을 사용할 수 있지만 감소된 품질의 썸네일은 1과 동일한 NewSubFileType을 사용해야 합니다. 또한 첫 번째 IFD가 낮은 품질 또는 해상도 썸네일을 가져야 하는 것은 아니지만 권장됩니다.
* **바이트 순서**: 특정 카메라 모델의 파일에 대해서도 DNG 리더에서 바이트 순서를 지원해야 합니다.
* **마스킹된 픽셀**: 대부분의 카메라 센서는 블랙 인코딩을 통해 센서 가장자리에서 완전히 마스킹된 픽셀을 계산합니다. 이러한 픽셀은 이미지를 DNG 형식으로 저장하기 전에 포함하거나 트리밍할 수 있습니다. 마스킹된 픽셀이 잘리지 않으면 이러한 픽셀의 영역이 ActiveArea 태그에 언급되어야 합니다. 블랙 인코딩 레벨에 대해 이러한 픽셀에서 수집된 정보는 원시 데이터가 저장되기 전에 사용되거나 블랙 레벨을 지정하는 DNG 파일에 포함될 수 있습니다.
* **불량 픽셀**: 원시 데이터를 DNG로 저장하기 전에 불량 픽셀을 제외해야 합니다.
* **메타데이터**: 메타데이터는 다음 방법 중 하나로 DNG에 포함될 수 있습니다.
** TIFF-EP 또는 EXIF 메타데이터 태그 사용
** IPTC 메타데이터 태그(33723)를 통해
** XMP 메타데이터 태그 사용(700)
* **독점 데이터**: 일반적으로 공급업체는 자체 변환기에서 사용할 독점 데이터를 원시 파일에 포함합니다. DNG는 개인 태그, 개인 IFD 및 개인 MakerNote에 독점 데이터를 저장합니다. 공급업체는 DNG 파일을 편집하는 애플리케이션이 이 독점 데이터를 보존하도록 하기 위해 DNGPrivateData 및 MakerNoteSafety 태그를 사용해야 합니다.

다음은 몇 가지 중요한 제한 및 확장 TIFF 태그입니다.

**BitsPerSample**

8 ~ 32비트/샘플이 지원됩니다. SamplesPerPixel이 1과 같지 않은 경우 각 샘플에 대해 동일한 깊이가 있어야 합니다. 그러나 BitsPerSample이 8, 16 또는 32와 같지 않은 경우 비트는 TIFF 기본 FillOrder 1(빅 엔디안)을 사용하여 바이트로 압축되어야 합니다.

**압축**

두 가지 압축 태그 값이 지원됩니다.

* 값 # 1: 압축되지 않은 데이터.
* 값 # 7: 기본 DCT JPEG 또는 무손실 JPEG 압축인 JPEG 압축 데이터.

**측광 해석**

다음 값은 축소판 및 미리 보기 IFD에만 지원됩니다.

* 1 = BlackIsZero. 감마 2.2 색 공간에 있다고 가정합니다.
* 2 = RGB. sRGB 색 공간에 있다고 가정합니다.
* 6 = YCbCr. JPEG로 인코딩된 미리보기 이미지에 사용됩니다.

원시 IFD에 대해 다음 값이 지원되며 카메라의 기본 색상 공간으로 간주됩니다.

* 32803 # CFA(컬러 필터 어레이).
* 34892 # LinearRaw.

**정위**

Orientation 태그는 DNG 파일의 무손실 회전을 수행할 수 있도록 파일 브라우저에 사용됩니다. DNG 판독기는 미러링된 방향을 포함하여 가능한 모든 방향을 지원해야 합니다.

## 최신 버전의 DNG 기능

DNG 버전 1.4 2012년 10월에는 다음과 같은 고급 기능이 있습니다.

* 기본 사용자 자르기
* 투명도
* 부동 소수점(HDR)
* 손실 압축
* 프록시

## 참조 ##

* [DNG 사양 - Adobe 제공](https://www.kronometric.org/phot/processing/DNG/dng_spec_1.4.0.0.pdf)
* [디지털 네거티브 - 위키피디아](https://en.wikipedia.org/wiki/Digital_Negative)
* [DNG - 디지털 카메라 원시 데이터의 공개 보관 형식](https://helpx.adobe.com/photoshop/digital-negative.html)
