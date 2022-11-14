{
  "date" : "2021-03-12",
  "keywords" :["VP9","ファイル","拡張子","ファイル形式","ビデオ形式","TrueMotion ビデオ","VPX","On2 テクノロジー"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VP9 - TrueMotion ビデオ ファイル",
  "description":"VP9 ファイル形式と,VP9 ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "VP9",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-03-27"
}

## VP9ファイルとは何ですか?

Google は、VP8 の後継として、ロイヤルティ フリーのオープンソース ビデオ コーディング標準として VP9 コーデックを開発しました。元々は、YouTube のウルトラ HD コンテンツを圧縮するために設計されました。これは、前身のコーディング効率を拡張および強化するためです。元の VPX コーデックについて言えば、それらは 2010 年に Google によって同化された On2 Technologies から来ました。Google は後にコーデックをオープンソース化しました。 VP8 と VP9 の両方のフォーマットは、フリーの BSD ライセンスの下で利用できます。これにより、オペレータは、ソース コードを明らかにすることなく、専用ソフトウェアとオープンソース ソフトウェアの両方でエンコードまたはデコードの能力を組織することができます。

## VP9 の技術的特徴

* VP9 は、最大 120 fps で 8192x4352 の最大解像度と、Rec 601、Rec 709、Rec 2020、SMPTE-170、SMPTE-240、および sRGB を使用した複数の色空間をプロビジョニングします。
* 10/12 ビット エンコーディングと HDR の追加サポートにより、低ビットレート圧縮から高品質のウルトラ HD まで、Web およびモバイルのあらゆるユース ケースがこのフォーマットで完全にサポートされます。
* ビデオのビットレートを他社と比較して 50% も削減できます
* アダプティブ ストリーミングに対応しており、YouTube やその他の有名な Web ビデオ プロバイダーで使用されています。
* Chrome、Opera、Edge、Firefox、Android デバイス、および数百万台のスマート TV が、このコーデックのデコードをサポートしています
* 1080p を超えるビデオ解像度は VP9 によって変更され、ロスレス圧縮が可能になります
* Recのような異なる色空間。 601、Rec。 709、Rec。 2020、SMPTE-170、SMPTE-240、および sRGB は VP9 でサポートされています
* Hybrid Log-Gamma と Perceptual Quantizer を使用した HDR ビデオも VP9 でサポートできます


## 簡単な歴史

* VP9 ビデオ コーデックの開発は 2011 年に開始され、そのデコーダーは 2012 年 12 月に Chromium Web ブラウザーに追加されました。
* 最初の Google Chrome Web ブラウザー バージョンは 2013 年 2 月にリリースされ、その時点でデコードをリリースしました
* Google は、2013 年 8 月に VP9 の最終サポートを含む Chrome 29.0.1547 をリリースしました
* 2013 年 10 月、直感的な VP9 デコーダーが FFmpeg に追加されました
* Mozilla は、2013 年 12 月に Firefox に VP9 のサポートを追加し、バージョン 2 を 2014 年 3 月 18 日にリリースしました。
 

## VP9の働き

通常、4K ビデオは特定のピクセルを小さくすることで画質を向上させますが、VP9 コーデックと HEVC はピクセルを大きくしてビットレートとファイル サイズを縮小します。これは矛盾しているように思えるかもしれませんが、エンコーディング エンジンはより大きなピクセルを取得し、より高い解像度の生産性に変換します。ビデオ フレームを伴うソース ビデオは、圧縮ビデオ ビットストリームを作成するためにエンコードまたは圧縮されます。個々のフレームは、最初にピクセルのブロックに分割されます。次に、ブロックは 3 次元の却下について精査され、変更できない領域を利用するためにフレーム間の順次接続が評価されます。これらは、次のフレームで特定のブロックの品質を保証するモーション ベクトルを介してエンコードされます。残差情報は、効果的なバイナリ圧縮を使用してエンコードされます。

## 参考文献

* [VP9 Wikipedia](https://en.wikipedia.org/wiki/VP9#:~:text=VP9%20is%20an%20open%20and,on%20Google's%20video%20platform%20YouTube)
* [MDN ウェブ ドキュメント](https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Video_codecs#vp9)
※【ココナッツ】(https://www.coconut.co/)
