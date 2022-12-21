# tantan's room

## X680x0 free softwares

### BMPLEX.X

Arimac氏作の BMPL.X 0.33 を [XEiJ](https://stdkmd.net/xeij/) の[拡張グラフィック画面](https://stdkmd.net/xeij/feature.htm#extendedgraphic)に対応させ、
最大1024x1024x65536色表示可能とする機能追加を行なったものです。
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


### GJ0.X

BMPLEX.X で最大1024x1024x65536色の画像表示を行なった後、`screen` コマンドなどを実行し、一時的にグラフィック画面が非表示になると、`screen ,1` として再表示しようとしても画面が乱れます。
GVRAMにデータが残っている状態であれば、この GJ0.X を実行することで XEiJ 拡張グラフィック画面を再表示させることができます。なお、GJ0という名前はXEiJが内部的に使っている画面モードの定義からきています。

* [GJ0_001.ZIP](https://github.com/tantanGH/distribution/raw/main/GJ0_001.ZIP) GJ0.X 0.01 実行ファイル

実行は以下だけです。特にオプションなどもありません。

    GJ0.X

### funcoff.r

Human68kのコンソール画面の下部に表示されるファンクションキー表示行は、これを一度非表示にしても、アプリケーションによっては終了時に強制的に再表示されてしまう場合があります。
これを防ぐために、常駐してファンクションキー表示行を強制的に非表示にするプログラムです。
具体的には、`DOS __CONCTRL($ff23)`をフックし、ファンクションキーを表示するモードで呼ばれても表示しないようにします。
昔自分が作ったものをリファインしたものになります。

なお、常駐したままで機能を有効化したり無効化したり切り替えることもできます。どうしてもファンクションキー表示が欲しい場合に一時的に有効化したい場合などに使えます。

* [FNCOF200.ZIP](https://github.com/tantanGH/distribution/raw/main/FNCOF200.ZIP) funcoff.r 2.00 実行ファイル

ファンクションキー表示を抑制するには、パラメータ `on` をつけて実行します。常駐していない場合は常駐します。なにもパラメータを付けない場合は `on` と同じ動作となります。

    funcoff.r on

ファンクションキー表示を許可するには、パラメータ `off` をつけて実行します。

    funcoff.r off
    
常駐解除するには、`-r` オプションをつけて実行してください。

    funcoff.r -r


## CONTACT

tantan (github:tantanGH, twitter:snakGH)

<!---
tantanGH/tantanGH is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
