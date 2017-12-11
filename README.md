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

## タイル一覧
<span style="color: #ff0000">提供実験中のデータであるため、事業化までにデータIDやデータ構成、データの内容（属性の有無等）が変わる可能性があります。</span>
これらを変更する場合、事前に<a href="https://twitter.com/gsi_cyberjapan/">Twitter（@gsi_cyberjapan）</a>にてアナウンスいたします。

### 地図情報（道路中心線）
<table>
	<tr><th>URL</th><td colspan="3">https://cyberjapandata.gsi.go.jp/xyz/experimental_rdcl/{z}/{x}/{y}.geojson</td></tr>
	<tr><th class="titletd">データソース</td><td>数値地図（国土基本情報）- 地図情報</td>
		<th>ズームレベル</td><td>16</td></tr>
	<tr><th class="titletd">提供範囲</td><td>日本全国</td>
		<th>提供開始</td><td>平成27年8月3日</td></tr>
	<tr><th colspan="2"><a href="https://maps.gsi.go.jp/#15/38.262749/140.873523/&ls=ort%7Cexperimental_anno%7Cexperimental_rdcl%7Cexperimental_railcl%7Cexperimental_rvrcl&disp=00100&lcd=experimental_rdcl&d=vl" class="blank">地理院地図で表示</a></td>
		<th colspan="2"><a href="https://github.com/gsi-cyberjapan/experimental_rdcl" class="blank">GitHubリポジトリ</a></td></tr>
</table>

### 地図情報（鉄道中心線）
<table>
	<tr><th>URL</th><td colspan="3">https://cyberjapandata.gsi.go.jp/xyz/experimental_railcl/{z}/{x}/{y}.geojson</td></tr>
	<tr><th class="titletd">データソース</td><td>数値地図（国土基本情報）- 地図情報</td>
		<th>ズームレベル</td><td>16</td></tr>
	<tr><th class="titletd">提供範囲</td><td>日本全国</td>
		<th>提供開始</td><td>平成27年8月3日</td></tr>
	<tr><th colspan="2"><a href="https://maps.gsi.go.jp/#15/38.262749/140.873523/&ls=ort%7Cexperimental_anno%7Cexperimental_rdcl%7Cexperimental_railcl%7Cexperimental_rvrcl&disp=10010&lcd=experimental_rdcl&d=vl" class="blank">地理院地図で表示</a></td>
		<th colspan="2"><a href="https://github.com/gsi-cyberjapan/experimental_railcl" class="blank">GitHubリポジトリ</a></td></tr>
</table>

### 地図情報（河川中心線）
<table>
	<tr><th>URL</th><td colspan="3">https://cyberjapandata.gsi.go.jp/xyz/experimental_rvrcl/{z}/{x}/{y}.geojson</td></tr>
	<tr><th class="titletd">データソース</td><td>数値地図（国土基本情報）- 地図情報</td>
		<th>ズームレベル</td><td>16</td></tr>
	<tr><th class="titletd">提供範囲</td><td>日本全国</td>
		<th>提供開始</td><td>平成27年8月3日</td></tr>
	<tr><th colspan="2"><a href="https://maps.gsi.go.jp/#15/38.262749/140.873523/&ls=ort%7Cexperimental_anno%7Cexperimental_rdcl%7Cexperimental_railcl%7Cexperimental_rvrcl&disp=10001&lcd=experimental_rdcl&d=vl" class="blank">地理院地図で表示</a></td>
		<th colspan="2"><a href="https://github.com/gsi-cyberjapan/experimental_rvrcl" class="blank">GitHubリポジトリ</a></td></tr>
</table>

### 地図情報（注記）
<table>
	<tr><th>URL</th><td colspan="3">https://cyberjapandata.gsi.go.jp/xyz/experimental_anno/{z}/{x}/{y}.geojson</td></tr>
	<tr><th class="titletd">データソース</td><td>数値地図（国土基本情報）- 地図情報</td>
		<th>ズームレベル</td><td>15</td></tr>
	<tr><th class="titletd">提供範囲</td><td>日本全国</td>
		<th>提供開始</td><td>平成27年6月4日</td></tr>
	<tr><th colspan="2"><a href="https://maps.gsi.go.jp/#15/38.262749/140.873523/&ls=ort%7Cexperimental_anno%7Cexperimental_rdcl%7Cexperimental_railcl%7Cexperimental_rvrcl&disp=11000&lcd=experimental_rdcl&d=vl" class="blank">地理院地図で表示</a></td>
		<th colspan="2"><a href="https://github.com/gsi-cyberjapan/experimental_anno" class="blank">GitHubリポジトリ</a></td></tr>
</table>

### 地名情報（居住地名）
<table>
	<tr><th>URL</th><td colspan="3">https://cyberjapandata.gsi.go.jp/xyz/experimental_nrpt/{z}/{x}/{y}.geojson</td></tr>
	<tr><th class="titletd">データソース</td><td>数値地図（国土基本情報）- 地名情報</td>
		<th>ズームレベル</td><td>15</td></tr>
	<tr><th class="titletd">提供範囲</td><td>日本全国</td>
		<th>提供開始</td><td>平成29年8月4日</td></tr>
	<tr><th colspan="2"><a href="https://maps.gsi.go.jp/#15/38.262749/140.873523/&ls=ort%7Cexperimental_nrpt%7Cexperimental_nnfpt%7Cexperimental_pfpt&disp=1100&lcd=experimental_nrpt&d=vl" class="blank">地理院地図で表示</a></td>
		<th colspan="2"><a href="https://github.com/gsi-cyberjapan/experimental_pni" class="blank">GitHubリポジトリ</a></td></tr>
</table>

### 地名情報（自然地名）
<table>
	<tr><th>URL</th><td colspan="3">https://cyberjapandata.gsi.go.jp/xyz/experimental_nnfpt/{z}/{x}/{y}.geojson</td></tr>
	<tr><th class="titletd">データソース</td><td>数値地図（国土基本情報）- 地名情報</td>
		<th>ズームレベル</td><td>15</td></tr>
	<tr><th class="titletd">提供範囲</td><td>日本全国</td>
		<th>提供開始</td><td>平成29年8月4日</td></tr>
	<tr><th colspan="2"><a href="https://maps.gsi.go.jp/#15/38.262749/140.873523/&ls=ort%7Cexperimental_nrpt%7Cexperimental_nnfpt%7Cexperimental_pfpt&disp=1010&lcd=experimental_nrpt&d=vl" class="blank">地理院地図で表示</a></td>
		<th colspan="2"><a href="https://github.com/gsi-cyberjapan/experimental_pni" class="blank">GitHubリポジトリ</a></td></tr>
</table>

### 地名情報（公共施設）
<table>
	<tr><th>URL</th><td colspan="3">https://cyberjapandata.gsi.go.jp/xyz/experimental_pfpt/{z}/{x}/{y}.geojson</td></tr>
	<tr><th class="titletd">データソース</td><td>数値地図（国土基本情報）- 地名情報</td>
		<th>ズームレベル</td><td>15</td></tr>
	<tr><th class="titletd">提供範囲</td><td>日本全国</td>
		<th>提供開始</td><td>平成29年8月4日</td></tr>
	<tr><th colspan="2"><a href="https://maps.gsi.go.jp/#15/38.262749/140.873523/&ls=ort%7Cexperimental_nrpt%7Cexperimental_nnfpt%7Cexperimental_pfpt&disp=1001&lcd=experimental_nrpt&d=vl" class="blank">地理院地図で表示</a></td>
		<th colspan="2"><a href="https://github.com/gsi-cyberjapan/experimental_pni" class="blank">GitHubリポジトリ</a></td></tr>
</table>

### 地名情報（住居表示住所）
<table>
	<tr><th>URL</th><td colspan="3">https://cyberjapandata.gsi.go.jp/xyz/experimental_jhj/{z}/{x}/{y}.geojson</td></tr>
	<tr><th class="titletd">データソース</td><td>数値地図（国土基本情報）- 地名情報</td>
		<th>ズームレベル</td><td>18</td></tr>
	<tr><th class="titletd">提供範囲</td><td><a href="https://maps.gsi.go.jp/#10/35.688533/139.695969/&base=pale&ls=pale%7Cexperimental_jhj%7Cexperimental_jhj_index&d=v">地理院地図で見る</a></td>
		<th>提供開始</td><td>平成29年8月4日</td></tr>
	<tr><th colspan="2"><a href="https://maps.gsi.go.jp/#18/38.262749/140.873523/&ls=std%7Cexperimental_jhj&disp=11&lcd=experimental_jhj&d=vl" class="blank">地理院地図で表示</a></td>
		<th colspan="2"><a href="https://github.com/gsi-cyberjapan/experimental_pni" class="blank">GitHubリポジトリ</a></td></tr>
</table>

### 基盤地図情報_基本項目
<table>
	<tr><th>URL</th><td colspan="3">https://cyberjapandata.gsi.go.jp/xyz/experimental_fgd/{z}/{x}/{y}.geojson</td></tr>
	<tr><th class="titletd">データソース</td><td>基盤地図情報 - 基本項目（点及び線）</td>
		<th>ズームレベル</td><td>18</td></tr>
	<tr><th class="titletd">提供範囲</td><td>日本全国</td>
		<th>提供開始</td><td>平成27年10月29日</td></tr>
	<tr><th colspan="2"><a href="https://maps.gsi.go.jp/#17/38.262749/140.873523/&ls=std%7Cexperimental_fgd&disp=01&lcd=experimental_fgd&d=vl" class="blank">地理院地図で表示</a></td>
		<th colspan="2"><a href="https://github.com/gsi-cyberjapan/experimental_fgd" class="blank">GitHubリポジトリ</a></td></tr>
</table>

### 基盤地図情報_数値標高モデル（DEM10B）
<table>
	<tr><th>URL</th><td colspan="3">https://cyberjapandata.gsi.go.jp/xyz/experimental_dem10b/{z}/{x}/{y}.geojson</td></tr>
	<tr><th class="titletd">データソース</td><td>基盤地図情報 - 数値標高モデル DEM10B</td>
		<th>ズームレベル</td><td>18</td></tr>
	<tr><th class="titletd">提供範囲</td><td>日本全国</td>
		<th>提供開始</td><td>平成27年10月29日</td></tr>
	<tr><th colspan="2"><a href="https://maps.gsi.go.jp/#18/38.262749/140.873523/&ls=std%7Cexperimental_dem10b&disp=11&lcd=experimental_dem10b&d=vl" class="blank">地理院地図で表示</a></td>
		<th colspan="2"><a href="https://github.com/gsi-cyberjapan/experimental_dem" class="blank">GitHubリポジトリ</a></td></tr>
</table>

### 基盤地図情報_数値標高モデル（DEM5A）
<table>
	<tr><th>URL</th><td colspan="3">https://cyberjapandata.gsi.go.jp/xyz/experimental_dem5a/{z}/{x}/{y}.geojson</td></tr>
	<tr><th class="titletd">データソース</td><td>基盤地図情報 - 数値標高モデル DEM5A</td>
		<th>ズームレベル</td><td>18</td></tr>
	<tr><th class="titletd">提供範囲</td><td><a href="https://maps.gsi.go.jp/#12/35.688533/139.695969/&base=pale&ls=pale%7Cfgd_dem5a_area_dtil&d=v">地理院地図で見る</a></td>
		<th>提供開始</td><td>平成27年10月29日</td></tr>
	<tr><th colspan="2"><a href="https://gsi-cyberjapan.github.io/experimental_dem/#20/38.262749/140.873523" class="blank">デモサイトを表示（GitHub）</a></td>
		<th colspan="2"><a href="https://github.com/gsi-cyberjapan/experimental_dem" class="blank">GitHubリポジトリ</a></td></tr>
</table>

### 地形分類（自然地形）
<table>
	<tr><th>URL</th><td colspan="3">https://cyberjapandata.gsi.go.jp/xyz/experimental_landformclassification1/{z}/{x}/{y}.geojson</td></tr>
	<tr><th class="titletd">データソース</td><td>数値地図25000（土地条件）、脆弱地形調査、治水地形分類図</td>
		<th>ズームレベル</td><td>14～16（2～13：おおよその範囲図）</td></tr>
	<tr><th class="titletd">提供範囲</td><td><a href="https://maps.gsi.go.jp/#5/35.688533/139.695969/&base=pale&ls=pale%7Cexperimental_landformclassification1&d=vl">地理院地図で見る</a></td>
		<th>提供開始</td><td>平成27年3月29日</td></tr>
	<tr><th colspan="2"><a href="https://maps.gsi.go.jp/#14/38.304082/141.059046/&base=std&ls=std%7Cexperimental_landformclassification1%7Cexperimental_landformclassification2&disp=110&d=v" class="blank">地理院地図で表示</a></td>
		<th colspan="2"><a href="https://github.com/gsi-cyberjapan/experimental_landformclassification" class="blank">GitHubリポジトリ</a></td></tr>
</table>

### 地形分類（人工地形）
<table>
	<tr><th>URL</th><td colspan="3">https://cyberjapandata.gsi.go.jp/xyz/experimental_landformclassification2/{z}/{x}/{y}.geojson</td></tr>
	<tr><th class="titletd">データソース</td><td>数値地図25000（土地条件）、脆弱地形調査、治水地形分類図</td>
		<th>ズームレベル</td><td>14～16（2～13：おおよその範囲図）</td></tr>
	<tr><th class="titletd">提供範囲</td><td><a href="https://maps.gsi.go.jp/#5/35.688533/139.695969/&base=pale&ls=pale%7Cexperimental_landformclassification2&d=vl">地理院地図で見る</a></td>
		<th>提供開始</td><td>平成27年3月29日</td></tr>
	<tr><th colspan="2"><a href="https://maps.gsi.go.jp/#14/38.304082/141.059046/&base=std&ls=std%7Cexperimental_landformclassification1%7Cexperimental_landformclassification2&disp=101&d=v" class="blank">地理院地図で表示</a></td>
		<th colspan="2"><a href="https://github.com/gsi-cyberjapan/experimental_landformclassification" class="blank">GitHubリポジトリ</a></td></tr>
</table>

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
