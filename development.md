---
layout: page
title: 開発
permalink: /development/
---

### 深層学習によるブラインド信号源分離の実装
ブラインド信号源分離とは、音源の数より少ない数の録音チャネルで録音された音を、音源ごとに分離する問題です。
例えば、モノラル音源をボーカルと楽器の音に分離することが挙げられます。
そのような分離を実現するモデルであり、DeepClusteringの派生モデルであるChimeraNetを実装しました。

{% include image.html src="/assets/images/blind-source-separation.png" caption="音声を楽器の音と人の声に分離する概念図" height="400px" %}

#### 主なプログラミング言語・ライブラリ
* Python
  - Keras
  - LibROSA

#### 参考文献・関連リンク
* [GitHub](https://github.com/arity-r/ChimeraNet)
* [Luoらの論文](https://arxiv.org/abs/1611.06265)
* [Hersheyらの論文](https://arxiv.org/abs/1508.04306)
* [LuoらのChimeraNetのサイト](http://danetapi.com/chimera)


### 非負値行列因子分解による自動採譜の実装 (開発中)
非負値行列因子分解とは、与えられた行列を行列積や行列積の和に近似する操作です。
これをスペクトログラムに適用すると、どの楽器(周波数に対する音の強さ)が、いつどの程度の強さで鳴っているのか分かります。
この操作を派生させた、複数種類の楽器の演奏音から特定の楽器の音を取り出す方法を実装しています。

{% include image.html src="/assets/images/musical-notation-by-nmf.png" caption="北村らの方法による自動採譜" width="800px" %}

#### 主なプログラミング言語・ライブラリ
* Python
  - NumPy
  - LibROSA

#### 参考文献
* [北村らのポスター](http://d-kitamura.net/pdf/poster/DSP2013_poster_kitamura.pdf)


### OpenFaceを用いた髪型カタログシステムの提案
顔画像処理ライブラリの[OpenFace](http://cmusatyalab.github.io/openface/)を用いて、自分の顔と似た顔のモデルを髪型カタログから検索するシステムを提案・実装しています。

#### 主なプログラミング言語・技術要素
* Python
  - OpenFace
  - Requests (カタログ画像を取得するため)
* Docker (とはいえ、イメージを引っ張ってきただけですが)


### BlenderとInkscapeによる型紙生成
BlenderとInkscapeを使ってぬいぐるみの型紙を作る方法を考案しています。
以前からBlender単体で作る方法は知られていましたが、その方法にひと手間加えることでより滑らかな型紙を作ります。

{% include image.html src="/assets/images/softtoy-pattern-procedure.png" caption="3Dモデルから型紙を生成する手順" width="400px" %}
