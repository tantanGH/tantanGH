# tantan's room

自作ソフトウェア・覚書など

## 目次

X680x0/Human68k ソフトウェア (サウンド関連)
- [S44BGP.X](https://github.com/tantanGH/s44bgp) ... ハイメモリ常駐型バックグラウンドPCMプレーヤー for Mercury-UNIT
- [MP3EXP.X](https://github.com/tantanGH/mp3exp) ... ADPCM/PCM/WAV/MP3 プレーヤー
- [MP3CONV.X](https://github.com/tantanGH/mp3conv) ... MP3 to ADPCM/PCM コンバータ
- [KMDED.X](https://github.com/tantanGH/kmded) ... ステップ入力式KMD歌詞データエディタ
- [MDXVV.X](https://github.com/tantanGH/mdxvv) ... MDXセレクタ＆プレーヤ＆音色データビュワー
- [MDXVCAT.X](https://github.com/tantanGH/mdxvcat) ... MDX音色データ抽出ツール (MDX/ZMS/XC/BAS形式出力対応)
- [BPMCHK.X](https://github.com/tantanGH/bpmchk) ... S44/WAVデータBPM推定ツール

X680x0/Human68k ソフトウェア (グラフィックス関連)
- [PNGSCALE.X](#pngscalex) ... 拡大縮小回転デモ兼ベンチ (68030以上専用)
- [JPEGEX.X](https://github.com/tantanGH/jpegex) ... JPEG画像ローダ (XEiJ拡張グラフィックス対応)
- [PNGEX.X](#pngexx) ... PNG画像ローダ (XEiJ拡張グラフィックス対応)
- [GIFEX.X](#gifexx) ... GIF画像ローダ (XEiJ拡張グラフィックス対応, ハイメモリ対応, アニメーション対応)
- [BMPEX.X](#bmpexx) ... BMP画像ローダ (XEiJ拡張グラフィックス対応)
- [JPEGTRAN.X](https://github.com/tantanGH/jpegtran) ... JPEG最適化ツールの移植版
- [GJ0.X](#gj0x) ... XEiJ拡張グラフィックス簡易操作ツール

X680x0/Human68k ソフトウェア (ゲーム関連)
- [PPTBREAK.X](https://github.com/tantanGH/pptbreak) ... ブロック崩しもどきゲーム

X680x0/Human68k ソフトウェア (ツール関連)
- [RSRX.X](https://github.com/tantanGH/rsrx) ... RS232Cクロス接続用ファイル受信ツール
- [RSTX.X](https://github.com/tantanGH/rstx) ... RS232Cクロス接続用ファイル送信ツール
- [FUNCOFF.R](#funcoffr) ... ファンクションキー表示強制抑制常駐プログラム
- [MPUTYPE.X](#mputypex) ... MPUタイプを判別して終了コードとして返すツール
- [FONTSAVE.X](https://github.com/tantanGH/fontsave) ... 現在のフォントをフォントファイルに書き出すツール
- [XDFWRITE.X](https://github.com/tantanGH/xdfwrite) ... XDFファイルをFDに書き込むツール
- [KEEPCHK.X](https://github.com/tantanGH/keepchk) ... 常駐プログラムが常駐しているかをチェックするツール
- [ONTIME.X](https://github.com/tantanGH/ontime) ... アプリケーションの実行時間を計測するツール

MicroPython for X680x0 ソフトウェア
- [sprite.py](#spritepy) ... 擬似3D宇宙空間移動デモ
- [sprite2.py](#sprite2py) ... オブジェクト指向ボール移動デモ
- [maze.py](#mazepy) ... 巨大迷路作成デモ
- [opmtest.py](#opmtestpy) ... MML記述＆FM音源再生デモ
- [opmtest2.py](#opmtestpy) ... MML記述＆FM音源再生デモその2
- [snake.py](#snakepy) ... へびさん危機一髪ゲーム
- [ujongpy.py](#ujongpypy) ... Micro麻雀デモ

Python ソフトウェア (サウンド関連)
- [wav2adpcm](https://github.com/tantanGH/wav2adpcm/) ... ローパスフィルタ付 WAV to X68k ADPCM コンバータ in Python

Python ソフトウェア (グラフィックス・ムービー関連)
- [pymag](https://github.com/tantanGH/pymag/) ... PNG/JPG/BMP to MAG コンバータ in Python
- [mov2gif](https://github.com/tantanGH/mov2gif/) ... MP4/AVI to アニメーションGIF コンバータ in Python
- [png2sp](https://github.com/tantanGH/png2sp) ... 透過PNG to X68k スプライトデータ コンバータ in Python
- [pngdeband](https://github.com/tantanGH/pngdeband) ... バンド除去フィルタ付 24/32bit PNG to 15bit PNG コンバータ in Python

Python ソフトウェア (ツール関連)
- [rstx](https://github.com/tantanGH/rstx) ... RS232Cクロス接続用ファイル送信ツール in Python
- [rsrx](https://github.com/tantanGH/rsrx) ... RS232Cクロス接続用ファイル受信ツール in Python
- [dim2xdf](https://github.com/tantanGH/dim2xdf/) ... X68k FDファイルイメージコンバータ in Python

各種覚書
- [macOSユーザのためのX680x0エミュレータXEiJ活用ガイド(導入編)](https://zenn.dev/tantangh/articles/1b86b788812028)
- [macOSユーザのためのX680x0クロス開発環境xdev68k導入ガイド](https://github.com/tantanGH/distribution/blob/main/INSTALL_xdev68k_M1Mac.md)
- [X680x0実機とMacとの間でファイル転送する(MO編)](https://github.com/tantanGH/distribution/blob/main/x68k_Mac_data_exchange_MO.md)
- [X680x0の1.2MBフォーマット3.5インチFDをMacでイメージ化する](https://github.com/tantanGH/xdfwrite/)
- [X680x0/WindowsユーザのためのPython導入ガイド](https://github.com/tantanGH/distribution/blob/main/windows_python_for_x68k.md)
- [X68030+060turboとのつきあい始め(導入編)](https://github.com/tantanGH/distribution/blob/main/X68030_with_060turbo.md)
- [X68030+060turboとのつきあい始め(周辺機器編)](https://github.com/tantanGH/distribution/blob/main/X68030_with_060turbo_peripherals.md)

---

## X680x0 / Human68k ソフトウェア

---

### PNGSCALE.X 

複数のPNG画像を拡大縮小回転させるデモアプリです。

注意: 68030/68040/68060+ハイメモリ専用ソフトウェアです。060turbo.sys/HIMEM.SYS/TS16DRVp.Xなどのハイメモリドライバが必須です。

![](https://github.com/tantanGH/distribution/raw/main/images/pngscale2a.gif)

* [PNGSC020.ZIP](https://github.com/tantanGH/distribution/raw/main/PNGSC020.ZIP) PNGSCALE.X 0.2.0 実行ファイルおよびデータファイル

- バージョン 0.2.0 ... X68030 + TS6BE16ハイメモリ + TS16DRVp.X 環境でも動くようにした
- バージョン 0.1.0 ... 初版 (060turbo専用)

アーカイブに含まれるファイルをすべて一つのディレクトリにコピーし、カレントディレクトリをそのディレクトリにした上で `PNGSCALE.X` を実行します。

    usage: pngscale [-f] <画像数(1-8)> [クロップレベル(0-5,デフォルト2)]
   
画像数の指定は必須です。PNGファイルはランダムに選択されます。画像を差し替える場合は 320x320px の RGB/RGBA のPNGファイルと入れ替えてください。

クロップレベルは 384x256 モードの周囲どれくらいを描画対象から外すかの指定です。デフォルトは2です。0だとクロップしません。

`-f` オプションをつけると fps の表示を行います。

ESC/CR/SPACEキーを押すと終了します。

拡大縮小回転の計算そのものよりもVRAMへの書き込みの方がネックになるようで、クロップレベルを上げた方がfpsに効くようです。

---

### PPT Breaker

X680x0用のブロック崩しもどきゲームです。

![](https://github.com/tantanGH/pptbreak/raw/main/images/17a.gif)

詳細は[PPT Breaker for X680x0](https://github.com/tantanGH/pptbreak/)へ。

---

### PNGEX.X

X680x0用のPNG画像ローダです。[XEiJ](https://stdkmd.net/xeij/)の[拡張グラフィック画面](https://stdkmd.net/xeij/feature.htm#extendedgraphic)に対応しており、最大1024x1024x32768色の表示が可能です。ハイメモリをバッファとして利用可能です。

![](https://github.com/tantanGH/distribution/raw/main/images/png_demo1.png)

詳細は[pngex](https://github.com/tantanGH/pngex)へ。

---

### GIFEX.X

X680x0用のGIF画像ローダです。[XEiJ](https://stdkmd.net/xeij/)の[拡張グラフィック画面](https://stdkmd.net/xeij/feature.htm#extendedgraphic)に対応しており、最大1024x1024x32768色の表示が可能です。ハイメモリをバッファとして利用可能です。

アニメーションにも対応していますが、表示タイミングは厳密ではありません。

![](https://github.com/tantanGH/distribution/raw/main/images/gif_demo1a.gif)

アニメーションGIFは拙作 [mov2gif](https://github.com/tantanGH/mov2gif/) などで動画ファイルを変換して作ることができます。
    
詳細は [gifex](https://github.com/tantanGH/gifex) へ。    
    
---

### BMPLEX.X

Arimac氏作の BMPL.X 0.33 を [XEiJ](https://stdkmd.net/xeij/) の[拡張グラフィック画面](https://stdkmd.net/xeij/feature.htm#extendedgraphic)に対応させ、
最大1024x1024x65536色(32768色)表示可能とする機能追加を行なったものです。
XEiJ上で拡張グラフィックを有効にした場合にのみ効果がありますので、実機([X68000 Z](https://www.zuiki.co.jp/products/x68000z/)含む)や他のX68エミュレータでは正常動作しません。
また、ツクモ電機製のグラフィックアクセラレータボードTS-6BGAにも対応していません。

![](https://github.com/tantanGH/distribution/raw/main/images/bmp_demo1.png)

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

### MPUTYPE.X

X68030 に装着されているMPUの種別を `IOCS __SYS_STAT` で判別し、終了コードとして返します。
これによって、バッチファイルの処理を分岐させることができます。
ROM IOCS v1.3 以上が前提のため、事実上X68030シリーズ専用です。かつ68060の場合は`060turbo.sys`の導入が必須です。
なお、68040については`040SYSpatch.x`の導入で対応できるのかは確認しておらず不明です。

* [MPUTYPE.ZIP](https://github.com/tantanGH/distribution/raw/main/MPUTYPE.ZIP) MPUTYPE.X 実行ファイル

MPUの種類と終了コードの対応
MPU|終了コード
-|-
68060|6
68040|4
68030|3
68000|0

以下のようにバッチファイル内で使うことを想定しています。

    ECHO OFF
    
    MPUTYPE.X >NUL
    IF ERRORLEVEL 6 GOTO X68060
    IF ERRORLEVEL 4 GOTO X68040
    IF ERRORLEVEL 3 GOTO X68030
    IF ERRORLEVEL 0 GOTO X68000
    GOTO END
    
    :X68060
    ECHO Hello, X68060.
    GOTO END
    
    :X68040
    ECHO Hello, X68040.
    GOTO END
    
    :X68030
    ECHO Hello, X68030.
    GOTO END
    
    :X68000
    ECHO Hello, X68000.
    
    :END

---

### GJ0.X

PNGEX.X や BMPLEX.X で最大1024x1024x65536色の画像表示を行なった後、`screen` コマンドなどを実行し、一時的にグラフィック画面が非表示になると、`screen ,1` として再表示しようとしても画面が乱れます。GVRAMにデータが残っている状態であれば、この GJ0.X を実行することで XEiJ 拡張グラフィック画面を再表示させることができます。なお、GJ0という名前はXEiJが内部的に使っている画面モードの定義からきています。

* [GJ0_003.ZIP](https://github.com/tantanGH/distribution/raw/main/GJ0_003.ZIP) GJ0.X ver0.03 実行ファイル

以下のように何も引数をつけずに実行するか、1をつけて実行すると、1024x1024x65536モードのグラフィック画面を再表示できます。

    GJ0.X
    GJ0.X 1

以下のように0をつけて実行すると、1024x1024x65536モードのグラフィック画面のVRAMをクリアします。

    GJ0.X 0

拡張グラフィックを有効にしたXEiJ上以外では意味がなく、正常動作しませんのでご注意ください。

---

## MicroPython for X680x0 ソフトウェア

---

### sprite.py

HAS.X / HIOCS.X で超高名なX68kレジェンドの一人、yunk氏が令和に送り出す [MicroPython for X680x0](https://github.com/yunkya2/micropython-x68k/tree/port-x68k/ports/x68k) 
を使う練習です。

<img width='600' src='https://github.com/tantanGH/distribution/raw/main/images/star2a.gif'/>

[sprite.py ソース](https://github.com/tantanGH/distribution/blob/main/sprite.py)

ジョイスティックの上下左右で移動、Bボタンで加速です。シフトキーで終了します。

---

### sprite2.py

<img width='600' src='https://github.com/tantanGH/distribution/raw/main/images/ball2.gif'/>

[sprite2.py ソース](https://github.com/tantanGH/distribution/blob/main/sprite2.py)

なるべくオブジェクト指向風に書いたスプライトサンプル。シフトキーで終了します。

---

### maze.py

<img width='600' src='https://github.com/tantanGH/distribution/raw/main/images/maze1a.gif'/>

<img width='600' src='https://github.com/tantanGH/distribution/raw/main/images/maze2a.gif'/>

[maze.py ソース](https://github.com/tantanGH/distribution/blob/main/maze.py)

巨大迷路作成の様子を眺める環境ソフト(スクリーンセイバー？)です。シフトキーで終了します。

---

### opmtest.py

MicroPython for X680x0 で MMLを記述しFM音源の曲を演奏します。OPMDRV3.X もしくは ZMUSIC v2 の組み込みが必要です。

https://user-images.githubusercontent.com/121137457/218295954-08157ce0-957b-43a0-be36-15bb10993f4d.mp4

[opmtest.py ソース](https://github.com/tantanGH/distribution/blob/main/opmtest.py)

---

### opmtest2.py

OPMDRV Pythonクラスを定義して扱いやすくした。コンストラクタでデバイスドライバ登録確認も実装。

https://user-images.githubusercontent.com/121137457/218763491-fd5e4ff9-56fa-4186-8c6b-fe5ba3f312e4.mp4

[opmtest2.py ソース](https://github.com/tantanGH/distribution/blob/main/opmtest2.py)


---

### snake.py

へび脱出ゲーム。エスケープシーケンスとDOSコールの利用サンプル。エスケープシーケンスの詳細は Human68k のマニュアルの巻末に載っています。

<img width='600' src='https://github.com/tantanGH/distribution/raw/main/images/snake.gif'/>

[snake.py ソース](https://github.com/tantanGH/distribution/blob/main/snake.py)

---

### ujongpy.py

Micro麻雀 for MicroPython X680x0。配牌と山からツモって捨て牌だけできますw

<img width='600' src='https://github.com/tantanGH/distribution/raw/main/images/mahjong.gif'/>

[ujongpy](https://github.com/tantanGH/ujongpy)

---

## Python ソフトウェア

---

### pymag

これはX680x0用ソフトウェアではなく Python で書かれたアプリケーションです。X680x0上で表示できる16色または256色のMAG形式画像ファイルを生成できるコンバータです。
pip導入可。
詳細は[pymag](https://github.com/tantanGH/pymag/)へ。

---

### dim2xdf

これはX680x0用ソフトウェアではなく Python で書かれたアプリケーションです。X680x0用DIM形式FDイメージフォーマットファイルをXDF形式に変換できるコンバータです。
pip導入可。
詳細は[dim2xdf](https://github.com/tantanGH/dim2xdf/)へ。

---

### wav2adpcm

これはX680x0用ソフトウェアではなく Python で書かれたアプリケーションです。WAVE形式のPCMデータをX680x0用ADPCMデータに変換できるコンバータです。
ローパスフィルターとレベル調整にも対応しています。pip導入可。
詳細は[wav2adpcm](https://github.com/tantanGH/wav2adpcm/)へ。

---

### mov2gif

これはX680x0用ソフトウェアではなく Python で書かれたアプリケーションです。MP4/AVI形式の動画データをアニメーションGIFデータに変換できるコンバータです。
リサイズ、クロップ、カット、トリムにも対応しています。pip導入可。
詳細は[mov2gif](https://github.com/tantanGH/mov2gif/)へ。

---

### png2sp

これはX680x0用ソフトウェアではなく Python で書かれたアプリケーションです。PNG形式の画像データを X68k スプライトパターンおよびパレットデータに変換できるコンバータです。
透過PNGに対応しています。16x16を超えるサイズの場合は、複数のスプライトパターンに自動分割します。パレットは共通です。出力形式はCコンパイラで即利用可能なテキスト形式です。pip導入可。
詳細は[png2sp](https://github.com/tantanGH/png2sp/)へ。

---

### pngdeband

これはX680x0用ソフトウェアではなく Python で書かれたアプリケーションです。24/32bit PNG形式の画像データを X68k で表示するのに適した 15bit PNGに変換します。 
その際に band (マッハバンド) 除去を行うことで X680x0 に適した形式となります。リサイズも可能。pip導入可。
詳細は[pngdeband](https://github.com/tantanGH/pngdeband/)へ。

---

## TERMS OF USE / 免責

ここで配布されているソフトウェアを使用したことにより何らかの不具合(システムクラッシュその他)が生じても、一切の責任は負えません。自己責任にてご利用ください。
アーカイブの再配布は不具合が見つかった時に収拾がつかなくなるのでなるべくご遠慮ください。ただしこの github のリンクの紹介は自由です。

---

## CONTACT / 連絡先

tantan (https://github.com/tantanGH/ twitter:@snakGH)

<!---
tantanGH/tantanGH is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
