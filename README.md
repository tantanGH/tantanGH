# tantan's room

## X680x0 free software

### PNGEX.X

X680x0用のPNG画像ローダです。[XEiJ](https://stdkmd.net/xeij/)の[拡張グラフィック画面](https://stdkmd.net/xeij/feature.htm#extendedgraphic)に対応しており、最大1024x1024x32768色の表示が可能です。

詳細は[pngex](https://github.com/tantanGH/pngex)へ。

---

### BMPLEX.X

Arimac氏作の BMPL.X 0.33 を [XEiJ](https://stdkmd.net/xeij/) の[拡張グラフィック画面](https://stdkmd.net/xeij/feature.htm#extendedgraphic)に対応させ、
最大1024x1024x65536色(32768色)表示可能とする機能追加を行なったものです。
XEiJ上で拡張グラフィックを有効にした場合にのみ効果がありますので、実機([X68000 Z](https://www.zuiki.co.jp/products/x68000z/)含む)や他のX68エミュレータでは正常動作しません。
また、ツクモ電機製のグラフィックアクセラレータボードTS-6BGAにも対応していません。

* [BMPL032.LZH](https://github.com/tantanGH/distribution/raw/main/BMPL032.LZH) BMPL 0.32 オリジナルアーカイブ
* [BMPL033.LZH](https://github.com/tantanGH/distribution/raw/main/BMPL033.LZH) BMPL 0.33 オリジナルアーカイブ (0.32に対するアップデート差分)
* [BMEX0331.ZIP](https://github.com/tantanGH/distribution/raw/main/BMEX0331.ZIP) BMPLEX.X 0.33.1 実行ファイルおよびソース
* [BMP768SP.ZIP](https://github.com/tantanGH/distribution/raw/main/BMP768SP.ZIP) 動作確認用横幅768pxのBMPファイル集 ([NovelAI](https://novelai.net/)で生成)

拡張グラフィック画面を使った表示を行うには、新規に追加された `-e` オプションをコマンドラインに追加してください。このオプションを付けない場合は従来通りの動作となります。

    BMPLEX.X -e -c -n -v70 1220_23_nai.bmp

また、もう一つ新規に追加された `-z` オプションを使うと、与えたBMPファイルリスト(ワイルドカード含む)の中からランダムに一枚だけ表示します。

    BMPLEX.X -e -c -n -v70 -z D:\BMP\*.BMP

BMPL.X / BMPLEX.X ともに非圧縮のBMPファイルにのみ対応しています。任意の画像ファイルから非圧縮のBMPを作成するには
Python上で [Pillow](https://pillow.readthedocs.io/en/stable/) ライブラリを使うのが手軽です。

    from PIL import Image
    Image.open('hoge.jpg').resize((768,432)).convert('RGB').save('hoge.bmp')

おまけとして、ファイラーSTFでの拡張子設定サンプルです。単にリターンを押すと100%輝度全画面表示。SHIFT,CTRLを押しながらリターンを押すと背景差し替えのみ(それぞれ輝度85%,75%)。他のファイラでも似たような設定ができると思います。ご参考。

    .bmp    ---------sfp-   bmplex -e -n -k -r %p%
            -t--------fp-   bmplex -e -n -v85 %p%
            -c--------fp-   bmplex -e -n -v75 %p%

---

### GJ0.X

BMPLEX.X で最大1024x1024x65536色の画像表示を行なった後、`screen` コマンドなどを実行し、一時的にグラフィック画面が非表示になると、`screen ,1` として再表示しようとしても画面が乱れます。
GVRAMにデータが残っている状態であれば、この GJ0.X を実行することで XEiJ 拡張グラフィック画面を再表示させることができます。なお、GJ0という名前はXEiJが内部的に使っている画面モードの定義からきています。

* [GJ0_003.ZIP](https://github.com/tantanGH/distribution/raw/main/GJ0_003.ZIP) GJ0.X ver0.03 実行ファイル

以下のように何も引数をつけずに実行するか、1をつけて実行すると、1024x1024x65536モードのグラフィック画面を再表示できます。

    GJ0.X
    GJ0.X 1

以下のように0をつけて実行すると、1024x1024x65536モードのグラフィック画面のVRAMをクリアします。

    GJ0.X 0

拡張グラフィックを有効にしたXEiJ上以外では意味がなく、正常動作しませんのでご注意ください。

---

### funcoff.r

Human68kのコンソール画面の下部に表示されるファンクションキー表示行は、何らかの方法でこれを一度非表示にしても、アプリケーションによっては終了時に強制的に再表示されてしまう場合があります。
これを防ぐために、常駐してファンクションキー表示を強制的に抑制するプログラムです。
具体的には、`DOS __CONCTRL($ff23)` をフックし、ファンクションキーを表示するモードで呼ばれても表示しないようにします。

なお、常駐したままで機能を有効化したり無効化したり切り替えることもできます。どうしてもファンクションキー表示が欲しい場合で一時的に有効化する時などに使えます。

* [FNCOF200.ZIP](https://github.com/tantanGH/distribution/raw/main/FNCOF200.ZIP) funcoff.r 2.00 実行ファイル

ファンクションキー表示を抑制するには、パラメータ `on` をつけて実行します。常駐していない場合は常駐します。なにもパラメータを付けない場合は `on` と同じ動作となります。

    funcoff.r on

ファンクションキー表示を許可するには、パラメータ `off` をつけて実行します。

    funcoff.r off
    
常駐解除するには、`-r` オプションをつけて実行してください。

    funcoff.r -r

なお、これはXEiJ専用プログラムではありません。

---

### pymag

これはX680x0用ソフトウェアではなく Python で書かれたアプリケーションです。X680x0上で表示できる16色または256色のMAG形式画像ファイルを生成できるコンバータです。
詳細は[pymag](https://github.com/tantanGH/pymag/)へ。

---

### dim2xdf

これはX680x0用ソフトウェアではなく Python で書かれたアプリケーションです。X680x0用DIM形式FDイメージフォーマットファイルをXDF形式に変換できるコンバータです。
詳細は[dim2xdf](https://github.com/tantanGH/dim2xdf/)へ。

---

### xdev68k install guide for M1 Mac

X680x0対応クロス開発環境である [xdev68k](https://github.com/yosshin4004/xdev68k) をM1 Macに導入した際の覚書です。
詳細は[ここ](https://github.com/tantanGH/distribution/blob/main/INSTALL_xdev68k_M1Mac.md)。

---

## TERMS OF USE / 免責

ここで配布されているソフトウェアを使用したことにより何らかの不具合(システムクラッシュその他)が生じても、一切の責任は負えません。自己責任にてご利用ください。
アーカイブの再配布は不具合が見つかった時に収拾がつかなくなるのでなるべくご遠慮ください。ただしこの github のリンクの紹介は自由です。

## CONTACT / 連絡先

tantan (github:tantanGH, twitter:snakGH)

<!---
tantanGH/tantanGH is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
