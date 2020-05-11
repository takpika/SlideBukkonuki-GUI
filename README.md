# SlideBukkonuki+（仮名称）
![](https://raw.githubusercontent.com/takpika/SlideBukkonuki-Plus/master/SlideBukkonuki-GUI/img/スライドぶっこぬきマン.pn-2.png)

授業動画からスライド画面を切り取ることができます。

ダウンロードは[こちら](https://github.com/takpika/SlideBukkonuki-Plus/releases)
※ベータ版です。動作を保証していません。

# インストール方法
同梱のinstall.commandを実行すると、自動で必要なドライバのインストールが始まります。

画面の指示に従って操作してください。（英語です。ターミナル画面です。マウスは使えません。）

install.commandが実行できない人はターミナルで以下のコマンドを実行してください。（Homebrewがインストールされていない人向けのコマンドです。）
```
xcode-select --install
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
brew install opencv
```
※OpenCVが既にインストールされている場合はこの作業は必要ありません。
[参考URL](https://qiita.com/pypypyo14/items/4bf3b8bd511b6e93c9f9)

# なぜベータ版？
ソフトに使われているOpenCVをインストールするのに現状ターミナルを開く必要があり、上級者向けだからです。現状回避策を考えています。

# 対応OS
macOS Catalina 10.15以上

# 動作確認環境
Mac mini Late 2014: macOS Catalina 10.15.4

# FAQ
## Q. 「ぶっこ抜く！」を押してフォルダを選択したあとフリーズする。

A. 仕様です。修正予定ではあります。

## Q. オープンソースにしないのか？

A. どうするか考えてます。内部のソフトウェアのコンパイル版のみ一応公開します。

### オプション一覧
|  オプション  |  デフォルト  |  説明  |
| ---- | ---- | ---- |
|  -i  |  ./movie.mp4  |  入力動画のパスを指定してください。  |
|  -o  |  ./  |  出力先のフォルダーのパスを指定してください。  |
|  -t  |  10  |  閾値  |
|  -l  |  0  |  トリミング開始位置<br>動画にスライドの他先生が写ってる場合にスライドのみをトリミングできます。<br>左から何ピクセルかを指定してください。  |
|  -r  |  0  |  トリミング終了位置<br>右から何ピクセルかを指定してください。  |
|  -a  |  0  |  スライドのアスペクト比<br>0を指定すると4:3<br>0以外の整数を指定すると16:9になります。  |
|  -f  |  5  |  フレーム取得間隔（秒）<br>スライドが切り替わり判定を何秒ごとにするか整数で指定します。<br>先生のスライド切り替えがあまりにも早い場合は小さくするといいです。<br>小さすぎると計算量が多くなり時間がかかる場合があります。  |
|  -c  |  0  |  上寄り(0)・中間(1)・下寄り(2)のいずれかを選択できます。  |

# クレジット
開発者: [takpika](https://twitter.com/takpika0308)

デザイン: [SGO](https://twitter.com/SGO_ITF)

# その他
アプリ開発はほぼ初心者なので、色々とバグがあります。今後修正はしていく予定なので少々お待ちを…。何かあれば[こちら](https://github.com/takpika/SlideBukkonuki-GUI/issues)にご連絡ください。

バグ修正が終わり次第、リリース版にしようと考えています。
