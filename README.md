国土地理院ベクトルタイル提供実験
======================
[Readme in English](README_en.md) also available.

## ベクトルタイルの仕様
本提供実験によるベクトルタイルは、[地理院タイル](http://maps.gsi.go.jp/development/siyou.html)と同じ方式で配信します。
`https://cyberjapandata.gsi.go.jp/xyz/{dataID}/{z}/{x}/{y}.{拡張子}`

- ベクトルタイルは、GeoJSONをタイル形式に分割したもの。
- GeoJSONは「The GeoJSON Format Specification」が定める形式で、拡張子は「geojson」。詳細は次のURLを参照のこと。 http://geojson.org/
- 文字コードはUTF-8。
- 1ファイルに1つのFeatureCollection型のオブジェクトがある。
- 個々のオブジェクトはそのFeatureCollection型のオブジェクトの中に配列で入っている。
- 個々のオブジェクトには、”geometry”（座標値（経緯度座標））と”property”（属性）が設定されている。
- スタイルの情報は含まない。（本提供実験では、[ベクトルタイルスタイル定義 style.js 規約](https://github.com/gsi-cyberjapan/style-dot-js-spec)に則って作成されたものを使用します。）

## 提供データ
- 道路中心線　https://github.com/gsi-cyberjapan/experimental_rdcl で説明
- 鉄道中心線　https://github.com/gsi-cyberjapan/experimental_railcl で説明
- 河川中心線　https://github.com/gsi-cyberjapan/experimental_rvrcl で説明
- 注記　https://github.com/gsi-cyberjapan/experimental_anno で説明
- 地名情報　https://github.com/gsi-cyberjapan/experimental_pni で説明
- 基盤地図情報（基本項目）　https://github.com/gsi-cyberjapan/experimental_fgd で説明
- 基盤地図情報（数値標高モデル）　https://github.com/gsi-cyberjapan/experimental_dem で説明
- 地形分類　https://github.com/gsi-cyberjapan/experimental_landformclassification で説明

## デモサイト
- 地理院地図  
https://maps.gsi.go.jp/#17/35.707179/139.959544/&base=ort&ls=ort%7Cexperimental_railcl%7Cexperimental_anno&disp=111&lcd=experimental_anno&vs=c1j0l0u0f0&d=l
- github  
https://gsi-cyberjapan.github.io/vector-tile-experiment/
- github(Canvas)  
https://gsi-cyberjapan.github.io/vector-tile-experiment/canvas.html

## 提供の位置づけ
国土地理院ベクトルタイル提供実験におけるデータの提供の位置づけは次のとおりです。
- 本提供実験は、ベクトルタイル提供における技術的・施策的課題を国土地理院が把握するとともに、外部からの技術的な提案を受け取り、外部との技術的な議論を通じてベクトルタイルの適切な提供方法を研究開発することを目的とするものです。
- 本提供実験の期間は、2014年8月1日から本提供実験終了までとなります。
- 本提供実験のデータは、国土地理院コンテンツ利用規約( http://www.gsi.go.jp/kikakuchousei/kikakuchousei40182.html )に従って利用できます。
- 本提供実験のベクトルタイルは基本測量成果と位置付けているものではありませんが、基本測量成果としての提供を検討するにあたって、提供を行うものです。
- 本提供実験の利用により生じた損失及び損害等について、国土地理院はいかなる責任も負わないものとします。

## 履歴
2017-08-04「地名情報（居住地名）」、「地名情報（自然地名）」、「地名情報（公共施設）」及び「地名情報（住居表示住所）」の提供実験を開始  
2017-03-29「地形分類（自然地形）」及び「地形分類（人工地形）」の提供実験を開始  
2016-03-09 地形分類の提供実験を開始  
2015-11-13 基盤地図情報（数値標高モデル）の5mメッシュ（航空レーザ測量）について、整備地域全体の提供実験を開始  
2015-10-29 基盤地図情報（数値標高モデル）の10mメッシュ（地形図の等高線）について、全国の提供実験を開始  
2015-10-29 基盤地図情報（基本項目）の点及び線について、全国の提供実験を開始  
2015-08-03 道路中心線、鉄道中心線、河川中心線ベクトルタイル提供実験を開始（日本全国）  
2015-06-04 地図情報（注記）の提供実験を開始  
2014-11-01 基盤地図情報（基本項目）の提供実験を開始（茨城県つくば市周辺、新潟県新潟市周辺）  
2014-10-31 基盤地図情報（数値標高モデル）の提供実験を開始（茨城県つくば市周辺、新潟県新潟市周辺）  
2014-08-01 道路中心線ベクトルタイル提供実験を開始（茨城県つくば市周辺、新潟県新潟市周辺）  
