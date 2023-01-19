# tantan's room

## 目次

X680x0/Human68k ソフトウェア
- [RSRX.X](https://github.com/tantanGH/rsrx) ... RS232C-USB クロス接続用ファイル受信ツール
- [PPT Breaker](https://github.com/tantanGH/pptbreak) ... ブロック崩しもどきゲーム (xdev68k対応ソースコード付)
- [MDXVCAT.X](https://github.com/tantanGH/mdxvcat) ... MDX音色データ抽出ツール (MDX/ZMS/XC/BAS形式出力対応)
- [PNGEX.X](#pngexx) ... PNG画像ローダ (XEiJ拡張グラフィックス対応, ハイメモリ対応)
- [GIFEX.X](#gifexx) ... GIF画像ローダ (XEiJ拡張グラフィックス対応, ハイメモリ対応, アニメーション対応)
- [BMPEX.X](#bmpexx) ... BMP画像ローダ (XEiJ拡張グラフィックス対応)
- [funcoff.r](#funcofr) ... ファンクションキー表示強制抑制常駐プログラム
- [MPUTYPE.X](#mputypex) ... MPUタイプを判別して終了コードとして返すツール
- [GJ0.X](#gj0x) ... XEiJ拡張グラフィックス簡易操作ツール

Python ソフトウェア
- [rstx](https://github.com/tantanGH/rstx) ... RS232C-USB クロス接続用ファイル送信ツール
- [pymag](https://github.com/tantanGH/pymag/) ... PNG/JPG/BMP to MAG コンバータ in Python
- [dim2xdf](https://github.com/tantanGH/dim2xdf/) ... X68k FDファイルイメージコンバータ in Python
- [wav2adpcm](https://github.com/tantanGH/wav2adpcm/) ... ローパスフィルタ付 WAV to X68k ADPCM コンバータ in Python
- [mov2gif](https://github.com/tantanGH/mov2gif/) ... MP4/AVI to アニメーションGIF コンバータ in Python
- [png2sp](https://github.com/tantanGH/png2sp) ... 透過PNG to X68k スプライトデータ コンバータ in Python
- [pngdeband](https://github.com/tantanGH/pngdeband) ... バンド除去フィルタ付 24/32bit PNG to 15bit PNG コンバータ in Python

各種覚書
- [X680x0実機とMacとの間でファイル転送する(MO編)](https://github.com/tantanGH/distribution/blob/main/x68k_Mac_data_exchange_MO.md)
- [X680x0 C言語でハイメモリを使う](https://github.com/tantanGH/distribution/blob/main/use_HIMEM_in_C.md)
- [X680x0で384x256の画面モードを使う](https://github.com/tantanGH/distribution/blob/main/x680x0_screen_384x256.md)
- [令和に再開するX680x0 C言語プログラミング](https://github.com/tantanGH/distribution/blob/main/x68k_c_programming_1.md)
- [X680x0/WindowsユーザのためのPython導入ガイド](https://github.com/tantanGH/distribution/blob/main/windows_python_for_x68k.md)
- [macOSユーザのためのX680x0エミュレータXEiJ活用ガイド(導入編)](https://zenn.dev/tantangh/articles/1b86b788812028)
- [macOSユーザのためのX680x0クロス開発環境xdev68k導入ガイド](https://github.com/tantanGH/distribution/blob/main/INSTALL_xdev68k_M1Mac.md)

---

## X680x0 / Human68k ソフトウェア

---

### PPT Breaker

X680x0用のブロック崩しもどきゲームです。

![](https://github.com/tantanGH/pptbreak/raw/main/images/17.gif)

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

![](https://github.com/tantanGH/distribution/raw/main/images/gif_demo1.gif)

* [GIFEX050.ZIP](https://github.com/tantanGH/distribution/raw/main/GIFEX050.ZIP) GIFEX.X 0.５.0 実行ファイル


      GIFEX - GIF image loader with XEiJ graphic extension support version 0.5.0 by tantan 2023
      usage: gifex.x [options] <image.gif>
      options:
       -b<n> ... バッファメモリの大きさを調整します[1-24] (デフォルト:4)
       -c ... 表示する前に画面クリアします
       -f<n> ... 最大表示フレーム数 (デフォルト:無制限)
       -h ... ヘルプメッセージの表示
       -i ... GIFファイル情報の表示
       -l ... 無限ループします(ESCキーで抜けます)
       -m ... すべてのデータを事前にメモリに展開してからアニメーションを再生します
       -n ... 画像を中央に表示します
       -o<x,y> ... 画像の表示位置を指定します -n は上書きされます
       -s<n> ... 画面モード 0:384x256, 1:512x512, 2:768x512, 3:768x512(拡張モード XEiJのみ)
       -u ... ハイメモリをバッファとして使用します
       -v<n> ... 明るさ調整 (0-100)
       -w<n> ... フレームレートを指定します (0:1/30fps, n:n fps, default:自動判定)

注意：大きく長いアニメーションGIFを再生するには大量のメモリとマシンパワーが必要です。ハイメモリの利用(`-u`)を強く推奨します。

アニメーションGIFは拙作 [mov2gif](https://github.com/tantanGH/mov2gif/) などで動画ファイルを変換して作ることができます。
    
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
IPL ROM v1.3 以上が前提のため、事実上X68030シリーズ専用です。
なお、実際に実機もしくはエミュレータでこちらが確認したのは68060/68030/68000だけです。

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
    
    MPUTYPE.X
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
