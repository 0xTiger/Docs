{
  "date" : "2021-03-12",
  "keywords" :[ "VP9", "파일", "확장자", "파일 형식", "비디오 형식", "TrueMotion 비디오", "VPX", "On2 기술"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VP9 - TrueMotion 비디오 파일",
  "description":"VP9 파일 형식과 VP9 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "VP9",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-03-27"
}

## .VP9 파일이란?

Google은 VP8의 후속 제품으로 VP9 코덱을 로열티 프리, 오픈 소스 비디오 코딩 표준으로 개발했습니다. 원래 유투브의 울트라 HD 콘텐츠를 압축하기 위해 고안된 것은 전작의 코딩 효율성을 확장하고 향상시키기 때문입니다. 원래 VPX 코덱에 대해 이야기하면 2010년 Google에 동화된 On2 Technologies에서 가져왔습니다. Google은 나중에 코덱을 오픈 소스로 제공했습니다. VP8 및 VP9 두 형식 모두 무료 BSD 라이선스에 따라 제공되며, 이를 통해 운영자는 소스 코드를 공개하지 않고 독점 소프트웨어와 오픈 소스 소프트웨어 모두에서 인코딩 또는 디코딩 능력을 구성할 수 있습니다.

## VP9의 기술적 특징

* VP9는 Rec 601, Rec 709, Rec 2020, SMPTE-170, SMPTE-240 및 sRGB를 사용하여 최대 120fps 및 다중 색상 공간에서 8192x4352의 최대 해상도를 제공합니다.
* 이 형식은 10/12비트 인코딩 및 HDR에 대한 추가 지원과 함께 낮은 비트 전송률 압축에서 고품질 울트라 HD에 이르기까지 웹 및 모바일 사용 사례의 전체 범위를 완벽하게 지원합니다.
* 타사 대비 최대 50%까지 비디오 비트율을 낮출 수 있습니다.
* 적응형 스트리밍을 지원하며 YouTube 및 기타 유명 웹 비디오 제공업체에서 사용합니다.
* Chrome, Opera, Edge, Firefox 및 Android 장치와 수백만 대의 스마트 TV가 이 코덱의 디코딩을 지원합니다.
* 1080p 이상의 비디오 해상도는 VP9를 통해 수정되며 무손실 압축이 가능합니다.
* Rec.와 같은 다른 색 공간. 601, Rec. 709, Rec. 2020, SMPTE-170, SMPTE-240 및 sRGB는 VP9에서 지원됩니다.
* Hybrid Log-Gamma 및 Perceptual Quantizer를 사용하는 HDR 비디오는 VP9에서도 지원될 수 있습니다.


## 약력

* 2011년 VP9 비디오 코덱 개발 시작, 2012년 12월 Chromium 웹 브라우저에 디코더 추가
* 2013년 2월 최초의 구글 크롬 웹 브라우저 버전이 출시되었으며 당시 디코딩이 출시되었습니다.
* Google은 2013년 8월에 VP9를 최종 지원하는 Chrome 29.0.1547을 출시했습니다.
* 2013년 10월, 본능적인 VP9 디코더가 FFmpeg에 추가되었습니다.
* Mozilla는 2014년 3월 18일에 출시된 버전 2에서 2013년 12월 Firefox에 VP9 유지를 추가했습니다.
 

## VP9의 작업

일반적으로 4K 비디오는 특정 픽셀을 작게 만들어 화질을 높이고 VP9 코덱과 HEVC는 비트 전송률과 파일 크기를 축소하기 위해 픽셀을 크게 만듭니다. 이것이 모순적으로 보일 수 있지만 인코딩 엔진은 더 큰 픽셀을 가져와 더 나은 해상도 생산성으로 변경합니다. 비디오 프레임을 수반하는 소스 비디오는 압축된 비디오 비트스트림을 만들기 위해 인코딩되거나 압축됩니다. 각 개별 프레임은 먼저 픽셀 블록으로 나뉩니다. 그런 다음 블록을 3차원 해제에 대해 면밀히 조사하고 프레임 간의 순차적 연결을 평가하여 변경할 수 없는 영역을 활용합니다. 이들은 다음 프레임에서 주어진 블록의 품질을 보장하는 모션 벡터를 통해 인코딩됩니다. 잔여 정보는 효과적인 이진 압축을 사용하여 인코딩됩니다.

## 참고문헌

* [VP9 위키백과](https://en.wikipedia.org/wiki/VP9#:~:text=VP9%20is%20an%20open%20and,on%20Google's%20video%20platform%20YouTube)
* [MDN 웹 문서](https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Video_codecs#vp9)
* [코코넛](https://www.coconut.co/)
