国土地理院ベクトルタイル提供実験
======================
[Readme in English](README_en.md) also available.

# 提供データ
- 道路中心線　本レポジトリで説明
- 鉄道中心線　本レポジトリで説明
- 河川中心線　本レポジトリで説明
- 注記　https://github.com/gsi-cyberjapan/experimental_anno　で説明
- 基盤地図情報（基本項目）　https://github.com/gsi-cyberjapan/experimental_fgd　で説明
- 基盤地図情報（数値標高モデル）　https://github.com/gsi-cyberjapan/experimental_dem　で説明
- 基準点　https://github.com/gsi-cyberjapan/experimental_cp　で説明
- 単写真　https://github.com/gsi-cyberjapan/experimental_pp　で説明
- ２万５千分1地形図郭　https://github.com/gsi-cyberjapan/experimental_zk25000　で説明

# 道路中心線、鉄道中心線、河川中心線
ズームレベル 16の GeoJSON タイルに変換したものを提供実験いたします。
データの仕様は次のとおりです。

-道路中心線

テンプレート URL: http://cyberjapandata.gsi.go.jp/xyz/experimental_rdcl/{z}/{x}/{y}.geojson

サンプル：http://cyberjapandata.gsi.go.jp/xyz/experimental_rdcl/16/58242/25798.geojson

ベクトルタイルスタイル定義：http://cyberjapandata.gsi.go.jp/xyz/experimental_rdcl/style.js


-鉄道中心線

テンプレート URL: http://cyberjapandata.gsi.go.jp/xyz/experimental_railcl/{z}/{x}/{y}.geojson

サンプル：http://cyberjapandata.gsi.go.jp/xyz/experimental_railcl/16/58242/25798.geojson

ベクトルタイルスタイル定義：http://cyberjapandata.gsi.go.jp/xyz/experimental_railcl/style.js


-河川中心線

テンプレート URL: http://cyberjapandata.gsi.go.jp/xyz/experimental_rvrcl/{z}/{x}/{y}.geojson

サンプル：http://cyberjapandata.gsi.go.jp/xyz/experimental_rvrcl/16/58242/25798.geojson

ベクトルタイルスタイル定義：http://cyberjapandata.gsi.go.jp/xyz/experimental_rvrcl/style.js


## データについて
提供範囲は日本全国になります。

データの内容の詳細は、電子国土基本図 地図情報　ファイル仕様書(PDFファイル)（http://www.gsi.go.jp/common/000093949.pdf ）等をご覧ください。

## デモサイト
地理院地図
http://maps.gsi.go.jp/?ll=35.707179,139.959544&z=17&base=ort&ls=experimental_railcl%7Cexperimental_anno&cd=f4&vs=c1j0l0u0&d=l

github
http://gsi-cyberjapan.github.io/vector-tile-experiment

github(Canvas)
http://gsi-cyberjapan.github.io/vector-tile-experiment/canvas.html

# 提供の位置づけ
国土地理院ベクトルタイル提供実験におけるデータの提供の位置づけは次のとおりです。
- 本提供実験は、ベクトルタイル提供における技術的・施策的課題を国土地理院が把握するとともに、外部からの技術的な提案を受け取り、外部との技術的な議論を通じてベクトルタイルの適切な提供方法を研究開発することを目的とするものです。
- 本提供実験の期間は、2014年8月1日から本提供実験終了までとなります。
- 本提供実験は、予告なく内容変更したり提供停止したりする場合があります。
- 本提供実験のベクトルタイルは基本測量成果と位置付けているものではありませんが、基本測量成果としての提供を検討するにあたって、提供を行うものです。
- 本提供実験の利用により生じた損失及び損害等について、国土地理院はいかなる責任も負わないものとします。


# 履歴
2014-08-01 道路中心線ベクトルタイル提供実験を開始（茨城県つくば市周辺、新潟県新潟市周辺）

2015-08-03 道路中心線、鉄道中心線、河川中心線ベクトルタイル提供実験を開始（日本全国）
