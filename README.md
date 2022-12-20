# tantan's room

## X680x0 free softwares

### BMPLEX.X

Arimac氏作の BMPL.X 0.33 を [XEiJ](https://stdkmd.net/xeij/) の[拡張グラフィック画面](https://stdkmd.net/xeij/feature.htm#extendedgraphic)に対応させ、
最大1024x1024x65536色表示可能の機能追加を行なったものです。
XEiJ上で拡張グラフィックを有効にして動かす場合にのみ効果がありますので、実機([X68000 Z](https://www.zuiki.co.jp/products/x68000z/)含む)や他のX68エミュレータでは正常動作しません。

拡張グラフィック画面を使った表示を行うには、新規に追加された -e オプションをコマンドラインに追加してください。このオプションを付けない場合は従来通りの動作となります。
また、もう一つ新規に追加された -z オプションを使うと、与えたBMPファイルリスト(ワイルドカード含む)の中からランダムに一枚だけ表示します。

BMPL.X / BMPLEX.X ともに非圧縮のBMPファイルにのみ対応しています。任意の画像ファイルから非圧縮のBMPを作成するには Python上で [Pillow](https://pillow.readthedocs.io/en/stable/) ライブラリを使うのが手軽です。

    from PIL import Image
    Image.open('hoge.jpg').resize((768,432)).convert('RGB').save('hoge.bmp')


### funcoff.r

Human68kのコンソール画面の下に表示されるファンクションキー表示行を非表示にしても、アプリケーションによっては終了時に強制的に再表示されてしまう場合があります。
これを防ぐために、常駐してファンクションキー表示行を非表示にし続ける常駐プログラムです。昔自分が作ったものをリファインしました。

## CONTACT

tantan (github:tantanGH, twitter:snakGH)

<!---
tantanGH/tantanGH is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
