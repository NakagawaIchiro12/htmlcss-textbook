## CSSを使ってWebサイトをデザインしよう！
### cssとは「HTMLをさらに見やすくデザインする方法」
CSSとは何か、CSSの文法はどうなっているのかを解説していきます。

**目次**
<!-- TOC depthFrom:1 depthTo:6 withLinks:1 updateOnSave:1 orderedList:0 -->

	- [CSSを使ってWebサイトをデザインしよう！](#css使web)
		- [cssとは「HTMLをさらに見やすくデザインする方法」](#csshtml見方法)
		- [CSSとは](#css)
	- [CSSの文法の書き方。](#css文法書方)
		- [CSSのセレクタ,プロパティとは](#css)
		- [HTMLとCSSをリンクする](#htmlcss)
		- [では、CSSとリンクをしていきましょう。](#css)
		- [CSSを使うための準備をします。](#css使準備)
	- [できたHTMLファイルを実際のWebブラウザで確認してみよう！](#html実際web確認)
	- [セレクタについて（デザインをもっと細部に）](#細部)
		- [ユニバーサルセレクタでまとめて基本を指定](#基本指定)
- [best{](#best)
		- [classの使い方](#class使方)
		- [divタグを使ってみましょう。](#div使)
		- [マウスを乗せると変わる(擬似クラス)](#乗変擬似)
		- [cssセレクタのまとめ](#css)
		- [CSSのプロパティ（どんなパラメータをどうするか？）](#css)
		- [まず最初に、colorプロパティをおさらいしてみましょう。](#最初color)
- [red{](#red)
		- [background-colorプロパティを使います。](#background-color使)
		- [フォントのサイズを指定して、フォントの大きさを整えます。](#指定大整)
		- [text alignでテキストの位置を指定します。](#text-align位置指定)
		- [font weightを使い、文字を太くします。](#font-weight使文字太)
- [bold{](#bold)
		- [ここまでプロパティについて沖縄メニュー表を作りながら学習しました。](#沖縄表作学習)
		- [画像を入れて、より美味しそうなメニューにしていきましょう。](#画像入美味)
		- [新しいimgフォルダを作って画像を入れましょう。](#新img作画像入)
	- [ここからは下記の画像に使うプロパティを学んでいきます。](#下記画像使学)
		- [widthのサイズを指定して、画像サイズを決める](#width指定画像決)
		- [heightのサイズを指定して、画像サイズを決める](#height指定画像決)
	- [background-imgeプロパティで、背景を変えることもできます。](#background-imge背景変)
		- [background-sizeプロパティを使って背景画像を整えます。](#background-size使背景画像整)
		- [サイズは小さくしたいけど、リピートしなくていいときに使うbackground-repeatプロパティ](#小使background-repeat)
	- [よく使う横並びのやり方をdisplayプロパティでやってみましょう。](#使横並方display)
		- [CSSのエラー解決](#css解決)
	- [サイトデザインを整える余白の作り方を学びます。](#整余白作方学)
		- [borderプロパティを使って、線を引き、目立たせたり仕切りをつけることができます。](#border使線引目立仕切)
			- [色を変えることもできます。](#色変)
			- [さらに、線を細くして、スタイリッシュにします。](#線細)
		- [margin （外側の余白)とpadding (内側の余白)を使って、バランスをよくする](#margin-外側余白padding-内側余白使)
		- [marginとpaddingの細かい指定方法を学んでみましょう。](#marginpadding細指定方法学)
		- [margin(マージン)を設定してみましょう](#margin設定)

<!-- /TOC -->


### CSSとは
![img-tagc01](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc01.png)
CSSとは
Cascading  カスケーディング
 Style　　　スタイル
 Sheets　　シート
 を略したもので、頭文字をとってCSS（シーエスエス）と呼びます。

・ウェブページのスタイルを指定するための言語です。

## CSSの文法の書き方。
まずは、文字に色をつけていくことができます。
下記の図のような感じです。
![img-tagc27](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc27.png)

```
p{
color:red;
}
```

CSSは上記のように書きます。
**意外と簡単そうですね。**
意味は「pタグの、色を、赤にする」という意味です。
![img-tagc02](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc02.png)
図解すると、こんな感じですね。

- どこの　　＝　p
- 何を　　　＝　color
- どうする　＝　赤

という構成です。

あとは、
![img-tagc03](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc03.png)
- どんなプロパティがあるか
- どんな指定方法があるか

ということを、調べながらやっていくのが、実際のプログラマーの現場になります。

### CSSのセレクタ,プロパティとは
![img-tagc04](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc04.png)
専門的には、
- pタグの部分をセレクタ
- colorの部分をプロパティ
- redの部分を値

と呼びます。

なので、

**pタグの色を赤にしておいて**
という指示は

**セレクタはpに、プロパティは赤色で**
という指定方法になります。

ただ、「pタグは赤で。」でも伝わりますので、用語よりも、

- どこの　　＝　p
- 何を　　　＝　color
- どうする　＝　赤

という順番でCSSが構成されているという基本を覚えておいていただければ、大丈夫です。

### HTMLとCSSをリンクする
![img-tagc05](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc05.png)
**pタグに指定されている「オススメはゴーヤチャンプルです」が赤くなっていますね。

HTMLにCSSのデザインを適用するためにはHTMLファイルとCSSファイルをリンクする作業をすれば、できるようになります。

早速やっていきましょう。
![img-tagc06](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc06.png)
Atomエディタのファイル＞新規ウインドウの順にクリックして、新規ウインドウを開きます。

![img-tagc07](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc07.png)
ファイル＞プロジェクトフォルダを追加をクリックします。

![img-tagc08](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc08.png)
保存先をデスクトップに指定して、
新規フォルダをクリックし、新規フォルダのな名前を「css-test」と入力して、「作成」をクリックします。

![img-tagc09](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc09.png)
そうすると、デスクトップに
css-testのフォルダができました。

![img-tag10](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc10.png)
次にAtomエディタを準備していきます。

Open a Projectをクリックします。

![img-tagc11](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc11.png)
先ほど作ったcss-testのフォルダを開きます。

![img-tagc12](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc12.png)
プロジェクトタブのCSS-TESTを右クリックし、新規ファイルをクリックします。

![img-tag13](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc13.png)
すると、Enter the path for the new file　と出てきますので、「css-test.html」と入力します。

入力したら、エンターキーを押します。

![img-tagc14](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc14.png)
これで、css-test.htmlというhtmlファイルができました。

新しくファイルを作る場合はこの手順になりますので、わからなくなったら、この作り方を見て作ってみてください。

---
では作っていきましょう。
まず、　半角で　「!」　を入力します。
![img-tag13](https://job555.info/wp-content/uploads/2020/05/img-tag13.png)
tabキーを入力することで、下記の内容が自動で入力されます。
![img-tag14](https://job555.info/wp-content/uploads/2020/05/img-tag14.png)

```html:mysite.html
    <!DOCTYPE html>
    <html lang="en">
    <head>
      <meta charset="UTF-8">
      <meta name="viewport" content="width=device-width, initial-scale=1.0">
      <meta http-equiv="X-UA-Compatible" content="ie=edge">
      <title>Document</title>
    </head>
    <body>

    </body>
    </html>
```

このページでは、全てmysite.htmlにコードを書いていきます。

次に、メタタグを２行削除します。
削除するのは下記の２行です。
headタグの下にmetaタグが３行あります。そのうちの下２行です。

```html:mysite.html
削除するmetaタグ

    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
```

そして、２行目のhtml lang="en"　をhtml lang="ja"に変更し、ホームページの言語の属性を英語→日本語に変更します。

そして、５行目のtitleタグを　Document→オススメメニュー　に変更します。

bodyタグの中に下記のように記入してみましょう

```
<p>ゴーヤチャンプル700円</p>
<p>フーチャンプル700円</p>

```

previewタブの画面には　<p>ゴーヤチャンプル700円</p>
<p>フーチャンプル700円</p>と表示だけされたはずです。

ここまでのコードは以下の通りになりました。

```html:mysite.html
    <!DOCTYPE html>
    <html lang="ja">
    <head>
      <meta charset="UTF-8">
      <title>オススメメニュー</title>
    </head>
    <body>
    <p>ゴーヤチャンプル700円</p>
    <p>フーチャンプル700円</p>
    </body>
    </html>
```

**ここまで行なった作業は以下の通り**
- メタタグを２行削除
- html langを　en から　ja　に変更
- titleタグを　Document　から　オススメメニュー　に変更
- bodyタグ内に <p>ゴーヤチャンプル700円</p>
<p>フーチャンプル700円</p>　と入力し、Previewタブで　hello world　と表示


**ここまでで、オススメメニューのCSSデザインの下準備ができました。**
***

### では、CSSとリンクをしていきましょう。
**cssファイルを作ります。**
ここからCSSを使ってデザインを当ててみましょう。
### CSSを使うための準備をします。

- css-testフォルダを右クリックし、
![img-tagc15](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc15.png)

- 新規ファイルを作成をクリックし、
![img-tagc16](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc16.png)
- mysite.cssと入力し、エンターキーでCSSファイルを作ります。
![img-tagc17](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc17.png)
そうしたら、mysite.htmlとmysite.cssを
リンクするために、headタグの中にlinkタグを記入します。

入力前はこんな感じ。
![img-tagc18](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc18.png)

```html:css-test.html
    <link rel="stylesheet" href="css-test.css" type="text/css" />
```

入力すると、下記のようになります。

![img-tagc19](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc19.png)


---
## できたHTMLファイルを実際のWebブラウザで確認してみよう！
Atomエディタタブの一番左側、projectタブから、作成したHTMLファイル
今回は「css-test.html」を右クリックし、Finderから開くを選択します。
![img-tagc20](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc20.png)

すると、下記画面が開きます
![img-tagc21](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc21.png)

Finderのウインドウから、「css-test.html」を右クリックし、
このアプリケーションで開く＞Google Chrome　をクリックします。

＊Google Chromeブラウザをインストールしていない方は、この際にインストールしておきましょう。

![img-tagc22](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc22.png)

すると、Webブラウザでcss-test.htmlが表示されました。
![img-tagc23](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc23.png)

これで、見たいHTMLファイルをブラウザで見ることができるようになりました！
AtomエディタのPreview表示も超ベンリですが、
実際のWebブラウザで確認することも大切になってきます。

ここで、上の画像の通り、Webブラウザには

「ゴーヤチャンプル

フーチャンプル」

とだけ表示されています。

css-test.cssファイルはリンクしましたが、
まだファイルの中は空なので、何も反映されていませんね。


ここで、先ほどのpタグに赤色をつけるcssを反映させてみましょう。

pタグを赤くするcssは以下の通りでした。

```
p{
  color:red;
}
```
これを、css-test.cssに書いていきましょう。

projectタブ＞css-test.cssをクリックして、
cssのページを表示させます。

![img-tagc24](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc24.png)

表示させたら、pタグについて上のように書いていきましょう。

意味は、

- どこの　　＝　p
- 何を　　　＝　color
- どうする　＝　赤

「pの色を赤にする」でしたね。

![img-tagc25](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc25.png)
入力したら、上記のようになりました。
これでは、保存されていません。保存しないと反映しないので、⌘＋Sで保存します。

青丸が消えました。保存完了です。
![img-tagc26](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc26.png)

**それでは、CSSで赤色になっているか、確認します**

先ほど開いたgoogle chromeの画面を見て、⌘＋Rで更新します。

更新前
![img-tagc23](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc23.png)


コマンド＋RでWebブラウザを更新後
![img-tagc27](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc28.png)

赤くなっています！これで、**pタグで指定した部分は赤くなるというCSSが反映**できました。

このようにCSSを書いていけば、サイトをどんどんデザインしていけます。


***

## セレクタについて（デザインをもっと細部に）
「どこにデザインを当てるのか」を指定するCSSセレクタの入力方法をみていきます。
ここからの内容をみると、特定のclassやidがついたhtmlタグにのみデザインを当てることができるようになります。
下記のようなデザインができるようになります。
![img-tagc97](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc97.png)

目次にするとこんな感じです。
- CSSセレクタ
- .クラス名
- #id名
- ユニバーサルセレクタ



**ここでは、CSSセレクタを組み合わせてより細かい場所の指定をする方法をみていきます。**

![img-tagc28](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc28.png)
言葉で言うと難しく聞こえますが、単純にここのことです。（上の画像）

セレクタ、つまり、選ぶ場所を指定して、細かくデザイン設定をできます。と言うことです。

セレクタを.class #id  *(ユニバーサルセレクタ)に指定して、デザインを当てる範囲を選ぶ事ができるんです。

順番に手を動かしながらやってみましょう。

ではまず、オススメのメニュー表を作っていきながら、デザインもしていきます。

下記の内容を入力していきます。

bodyタグのすぐ下に入れていきましょう。

```
<h1>沖縄の定番メニュー</h1>
<h2>沖縄にきたらこれ！オススメメニュー</h2>
```
入力するとこんな感じになります。
![img-tagc29](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc29.png)
⌘＋Sで保存も忘れずにしてくださいね。

そして、Webブラウザの方も⌘＋Rで更新してみましょう。
![img-tagc30](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc30.png)
このような感じになっていると思います。

シンプルなメニューですね。

それぞれ色を変えてみましょう。
- では、h1タグはgreen
- h2タグはblue

にします。
css-test.cssファイルに、下記のを入力していきましょう。

```
h1{
  color:green;
}

h2{
  color:blue;
}

```

わかりやすいように、それぞれ１行ずつ開けるのがポイントですね。

css-test.cssファイルに入力したらこんな感じになります。
![img-tagc31](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc31.png)

**セーブも忘れずにしましょう。セーブのショートカットは⌘＋Sです。**
セーブしないと、CSSが反映されません。初めのうちはよくあるミスです。＾＾；

Webブラウザも、更新してみましょう。
⌘＋Rです。

![img-tagc32](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc32.png)
色がついてみやすくなりました。
h1には緑、h2には青が適用されたのがわかります。


これで、**セレクタにタグを指定する事で、デザインを変えられる事がわかる**と思います。

では、まとめて色を赤にしてしまいたい。と言う場合、どのようにやるか解説します。

### ユニバーサルセレクタでまとめて基本を指定

ユニバーサルセレクタを使う事で、全てに基本デザインを指定できます。

わかりやすくするために、一度CSSをコメントアウトしましょう。

**コメントアウトとは**
コメントアウト【comment out】とは、プログラムのソースコードなどを編集する際に、特定の箇所をコメント化して一時的に除外すること。あとで復活させるかもしれない内容を消さずにその場で取っておくために行われる。

と言う感じです。
ユニバーサルセレクタを使うために、全てコメントアウトします。

コメントアウトには下記のようにします。

```
/* コメントアウトしたいものを入れる */
```
ではやってみましょう。

css-test.cssファイルに入力します。

**入力する部分は一番最初と最後です**
コメントアウトする前
![img-tagc31](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc31.png)

コメントアウトした後
![img-tagc33](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc33.png)

コメントアウトしたコードが薄くなって見えます。
見た目も分かりやすいですし、すぐあとで使うとなれば、コメントアウトを消すだけなので、楽ですね
。


Webブラウザの方を確認してみると、
CSSで色づけされたものが全て解除されています。

コメントアウトは・・・
- **CSSを適用する前と後の比較**
- **後で実装予定のコードを先に書いておく**
このように使います。

![img-tagc34](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc34.png)

では、準備が整ったので、ユニバーサルセレクタを使いましょう。

下記のコードを入力します。

```
*{
  color:red;
}

```

![img-tagc35](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc35.png)
入力するとこんな感じです。

Webブラウザの方は全ての文字が赤くなりましたね。

![img-tagc36](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc36.png)

このようにユニバーサルセレクタを使う事で、色やフォントなどを指定しておく事ができ、Webサイトのデザインの基盤にする事ができます。

この上から、順番にCSSを指定していってみましょう。

では、pタグを緑に指定します。
コメントアウトをpタグだけ外しましょう。

![img-tagc37](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc37.png)
css-test.cssファイルは今このような状態になっていて、ユニバーサルセレクタの部分のみ、適用されている状態になっています。

ここからpタグだけコメントアウトを探すと、次のようになります。
![img-tagc38](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc38.png)

そして、pタグの指定色が赤になっていて、そのままでは何も変わらないので、緑に変更します。

```
p{
  color:green;
}
```
このように指定します。

Webブラウザの方でも確認してみましょう。

![img-tagc39](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc39.png)

あとは、オススメメニューに、
- ソーキそば
- タコライス

をcss-test.htmlに追加します。

追加するときにはpタグで囲みましょう。

```
<p>ソーキそば</p>
<p>タコライス</p>
```
![img-tagc40](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc40.png)
追加するとこんな感じになりました。


![img-tagc41](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc41.png)
Webブラウザで確認すると、こんな感じですね。


ここでわかるのは、cssの優先順位です。

- 最初に*(ユニバーサルセレクタ)で赤色を指定して、
- 次にpタグに緑色を指定します。

**全てのユニバーサルセレクタより、タグを指定した方が、優先度が高いので、pタグは緑色になった。と言う事です。**


次に、ソーキそばは沖縄にきたら是非食べてもらいたい！と思うので、より目立たせたいと思います。

そう言う時はどうするかと言うと
pタグにidを割り振ります。

```
<p id="best">ソーキそば</p>

```
と言うふうにidをつけます。
**pとidの間には半角スペースを忘れないようにしましょう**
![img-tagc42](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc42.png)
これだけではまだ変わりません。
次に、id="best"にCSSを適用していきます。
入力する場所はcss-test.cssファイルです。

```
#best{
  color:blue;
}
```
とします。

入力するとこんな感じになります。
![img-tagc43](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc43.png)


Webブラウザで確認するとソーキそばが青色になっていますね。
![img-tagc44](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc44.png)



pタグは、緑が指定されていますが、その中でもidで指定されているソーキそばは青になっています。

pタグよりも、その中のidの方が、優先度が高いと言う事です。

このように、細かくCSSを指定していく事ができます。

### classの使い方
ゴーヤチャンプルと、フーチャンプルの2つが目立ちすぎなので、**２個以上同時に変えたい**

となったときに使うのが、classです。

では、ゴーヤチャンプルとフーチャンプルを黒色に変えます。

```
<p class="normal">ゴーヤチャンプル</p>
<p class="normal">フーチャンプル</p>

```

上記をcss-test.htmlに入力します。
![img-tagc45](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc45.png)
次に、

```
.normal{
  color:black;
}
```
**normalの前についている 「.(ドット)」がclassと言う意味になっています**

上記をcss-test.cssファイルに入力します。
![img-tagc46](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc46.png)

Webブラウザで確認すると、ゴーヤチャンプルとフーチャンプルが黒く表示されています。


![img-tagc47](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc47.png)

このように、2つ以上指定する場合は、classを使う事でできるようになります。

h2タグも黒でいいなと思うので、先ほどの.normalをつけて、黒くしましょう。

css-test.htmlの
h2タグに.normalを指定します。
![img-tagc48](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc48.png)

こんな感じです。

セーブして、Webブラウザを更新します。

![img-tagc49](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc49.png)
このように、h2の部分の「沖縄にきたらこれ！オススメメニュー」が黒くなりました。


**CSSは変えていませんが、classにnormalが指定されているタグは、全て文字が黒くなると言うCSSが適用される**と言う事です。


結構便利ですよね。


**では、逆にpタグのclassにだけ、黒を適用したいと指定したい場合はどうするかです。**

- class="normal"が複数のタグに指定してある
- pタグのみ、normalのCSSを適用させたい


そんな時は下記のようにします。
css-test.cssのファイルに書き込みます。
```
.normal{
  color:black;
}


```
となっていますが、

```
p.normal{
  color:black;
}


```

に変えます。
**.normalの前にpをつけるだけですね。**
![img-tagc50](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc50.png)

セーブして、Webブラウザを更新してみます。

![img-tagc51](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc51.png)
h2の「沖縄にきたらこれ！オススメメニュー」が赤色に戻りました。


ここまでのCSSのおさらいをしてみると

- 1番目に*(ユニバーサルセレクタ)で色を赤に指定して、文字を全部赤色にする
![img-tagc52](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc52.png)

- ２番目に、idで指定したpタグを青色に指定している
![img-tagc53](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc53.png)

- ３番目に、classで指定したpタグとh2タグの文字の色を黒に指定している。
![img-tagc54](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc54.png)

- ４番目に、classで指定するものを、pタグ限定にした。

![img-tagc55](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc55.png)
-
まとめるとこんな感じです

同じ「赤にする」でも、5つの指定方法があります。
これらを使う事で、思った通りのデザインにしていく事が可能です。
![img-tagc56](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc56.png)



***
### divタグを使ってみましょう。

**CSSが複雑になってきましたので、いったんこの練習では消してしまいましょう。**
css-test.cssを開き、
- 全てを選択
- デリートキーで削除
- ⌘＋Sで保存
- Webブラウザで更新

の順に消します。

![img-tagc57](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc57.png)
全てを選択します。⌘＋Aでも選択できます。

![img-tagc58](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc58.png)
デリートキーで全部消します。
⌘＋Sで保存も忘れずにしましょう。Webブラウザに反映されます。
![img-tagc59](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc59.png)
Webブラウザで⌘＋Rで更新します。
文字が全部黒くなり、CSSが全て消えた事がわかります。


**では、divタグを使って階層を指定してみましょう。**(階層関係を指定するセレクタについて)



タコライスの下に、下記を入力します。

```
<div>
<p>沖縄にきたら、やっぱりソーキそばと、タコライスが一番です。</p>
</div>

```
![img-tagc60](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc60.png)
css-test.htmlを開きます。
タコライスの下にスペースを作り、上記を入力していきましょう。

![img-tagc61](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc61.png)
入力したら、保存してWebブラウザを更新します。

![img-tagc62](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc62.png)
更新されて、「沖縄にきたら、やっぱりソーキそばと、タコライスが一番です。」が追加されています。


**divタグにcssを適用させていきます。**

css-test.cssに下記を入力していきます。

```
div p{
  color:red;
}

```
![img-tagc63](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc63.png)
入力したら、セーブしてWebブラウザを更新します。

![img-tagc64](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc64.png)
更新すると、divに囲まれたpタグのみが赤くなりました。

**これが、divタグの中のpタグを指定したcssになります。**

divタグの中のpタグと言う書き方が「階層を指定して書いています。」
![img-tagc65](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc65.png)


**h1タグとpタグを指定してみましょう。(複数要素を指定するセレクタ)**

h1タグとpタグを沖縄の海をイメージした青色にしてみましょう。


css-test.cssに
下記のように入力します。
```
h1,p{
  color:blue;
}

```

![img-tagc66](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc66.png)

入力したら、保存して、Webブラウザを更新してみましょう。

![img-tagc67](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc67.png)

沖縄の綺麗な青い感じが出たと思います。

今回は階層は関係なく、**h1とpタグを青にすると言う複数の要素を指定**しています。

これが複数要素を指定するセレクタです。


### マウスを乗せると変わる(擬似クラス)

css-test.cssに下記を入力していきます。

```
p:hover{
  color:red;
}

```
![img-tagc68](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc68.png)
入力して、保存します。Webブラウザを更新してみると、何も変わっていません。


![img-tagc69](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc69.png)
では、先ほど入力したCSSはpに指定しましたので、pタグであるゴーヤチャンプルとフーチャンプルと、ソーキそばとタコライスのどれかにマウスカーソルを載せてみてください。

![img-tagc70](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc70.png)
ソーキソバに載せてみました。
そうしたらソーキそばが赤くなりました。

hoverはマウスが乗ったら指定したCSSの通りに変化すると言うルールです。

今回は**color:red;とpタグを指定したので**マウスを乗せたら赤く変化しました。

### cssセレクタのまとめ

たくさんのcssセレクタが出てきました。
![img-tagc71](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc71.png)
![img-tagc72](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc72.png)
![img-tagc73](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc73.png)
覚えなくても大丈夫ですが、このようなセレクタを使う事で、細かく指定していく事ができます。

### CSSのプロパティ（どんなパラメータをどうするか？）
![img-tagc74](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc74.png)

ではいったん、body内のh2〜pタグまでのidやclassを消してシンプルにしましょう。

もとのコード
```
<h1>沖縄の定番メニュー</h1>
  <h2 class="normal">沖縄にきたらこれ！オススメメニュー</h2>
  <p class="normal">ゴーヤチャンプル</p>
  <p class="normal">フーチャンプル</p>
  <p id="best">ソーキそば</p>
  <p>タコライス</p>

```

idやclassを消してシンプルにします

```
<h1>沖縄の定番メニュー</h1>
<h2>沖縄にきたらこれ！オススメメニュー</h2>
<p>ゴーヤチャンプル</p>
<p>フーチャンプル</p>
<p>ソーキそば</p>
<p>タコライス</p>

```

![img-tagc75](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc75.png)
これでシンプルになりました。
![img-tagc76](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc76.png)
css-test.cssの中のcssも消してしまいます。

![img-tagc77](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc77.png)
Webブラウザを更新すると、CSSが綺麗になくなっています。

***

では、**ここから実際に変化を見ながら、手を動かしてCSSプロパティーを使って、**沖縄のオススメメニューをデザインしてみましょう。



### まず最初に、colorプロパティをおさらいしてみましょう。
css-test.htmlに

```
<p id="red">沖縄にきたら、やっぱりソーキそばと、タコライスが一番です。</p>

```
と入力します。

![img-tagc78](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc78.png)
次に、
css-test.cssに
```
#red{
  color:red;
}

```
![img-tagc79](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc79.png)
Webブラウザを更新すると、CSSが適用されていて、赤くなっています。

![img-tagc80](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc80.png)




### background-colorプロパティを使います。

css-test.htmlに

```
<h1 class="title">沖縄の定番メニュー</h1>

```
と入力します。

![img-tagc81](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc81.png)
次に、
css-test.cssに
```
.title{
  background-color:blue;
}

```

と入力して、背景色を沖縄の海の雰囲気のブルーにします。


![img-tagc82](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc82.png)
Webブラウザを更新すると、CSSが適用されていて、h1のタイトルの背景が青くなっています。


![img-tagc83](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc83.png)

ただ青が強すぎて黒い文字がみにくいので、
文字を白くしてみましょう。

css-test.cssに書き込みます。

```
.title{
  background-color:blue;
  color:white;
}


```
![img-tagc84](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc84.png)
このようになりました。

保存を忘れないようにしてくださいね。

webブラウザを更新します。
![img-tagc85](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc85.png)
h1のタイトルがはっきり見えるようになり、よく見えるようになりましたね。

これだけでもずいぶん印象が違います。

### フォントのサイズを指定して、フォントの大きさを整えます。

今までフォントのサイズを指定していませんでしたが、ここでフォントのサイズを指定して、デザインを整えましょう。


**今からやることは、文章の主体であるpタグのフォントサイズを決めることです**


css-test.htmlに下記を入力します。


```
p{
  font-size:18px;
}

```
入力すると、下記のようになります。
![img-tagc86](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc86.png)
セーブしてWebブラウザを更新してみると、
今までフォントサイズが指定してなかったものに比べると、若干大きくなり、みやすくなっています。
![img-tagc87](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc87.png)

このようにフォントのサイズを指定してあげることで、文字の大きさがしっかり指定され、どのWebブラウザで見たときもばらつきが少なくなります。
![img-tagc88](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc88.png)
font-sizeのパラメータの数字を変えることで、好きなサイズに変える事ができます。

今回は**セレクタをpタグ**に指定しています。
**セレクタをh2タグやそのほかに指定する事で、サイズを自由に指定する事ができます**





### text alignでテキストの位置を指定します。

今回は全体的に文字をセンター表示します。
ですので、ユニバーサルセレクタを指定して、パラメータをセンターにします。

css-test.cssに下記を入力します。
```
*{
  text-align:center;
}
```

ユニバーサルセレクタは全体に適用されるので、入力の位置は一番上にしましょう。**後でCSSをチェックするときにみやすくなります。**

入力したら下記のようになります。
![img-tagc89](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc89.png)
Webブラウザを更新すると、センター表示されました。

![img-tagc90](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc90.png)


### font weightを使い、文字を太くします。

これはブログでもよく使うものですね。
太くしたりする事で**目立たせて印象付ける方法です。**

では早速やってみましょう。

pタグにcssを適用させたいので、

css-test.cssに下記を入力します。


```
p{
  font-size:18px;
  font-weight:bold;
}


```


お店で**人気商品はタコライスなので、タコライスをさりげなく太文字にして、注文してもらいやすくしよう**と思います。

pタグにcssを適用させればいいと思うのですが、pタグはたくさんありますので、**タコライスのpタグのみ適用できるようにidを割り振り**ましょう。


css-test.htmlに入力していきます。
```
<p id="bold">タコライス</p>

```

![img-tagc93](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc93.png)
続いて、css-test.cssに
タコライスのみ太文字で文字サイズを18pxに揃えたcssを書いていきます。

```
#bold{
  font-size:18px;
  font-weight:bold;
}

```

![img-tagc94](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc94.png)

Webブラウザを更新してみます。
何も変わっていません。

![img-tagc95](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc95.png)

**pタグも同じcssがついているからです。**

pタグの太文字はいらないので、削除しましょう。

css-test.cssに入力します。
```
p{
  font-size:18px;
}

```

font-weight:bold;を削除しました。
![img-tagc96](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc96.png)

Webブラウザを更新してみます。

![img-tagc97](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc97.png)
こうする事で、さりげなく目線をタコライスの太文字にする事ができます。

これもデザインで大切な要素なので是非使ってくださいね。

### ここまでプロパティについて沖縄メニュー表を作りながら学習しました。

**文字だけでもかなりデザインできますよね**

実際ワードプレスなどでも文字表現ですので、これだけ知っておくだけでも読みやすく、目線を操作できるデザインが作れます


- colorプロパティ
- background-colorプロパティ
- コメントアウト
- font-sizeプロパティ
- text-alignプロパティ
- font-weightプロパティ

について学びました。

***

### 画像を入れて、より美味しそうなメニューにしていきましょう。

画像はダウンロードして使います。
ダウンロードリンクは下記です。
https://blog.job555.info/html-css/

**パスワードは htmlcss です。**
![img-tagc98](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc98.png)
**パスワードを入力して画面を開いてから右クリックで保存してください。**

では早速、画像を入れていきましょう！

css-test.htmlに画像を入れるために、画像を保存します。
![img-tagc99](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc99.png)

![img-tagc100](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc100.png)
名前をsokisoba-2にして保存をクリックします。

![img-tagc101](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc101.png)
ダウンロードされると、Webブラウザの下に表示されます。　
Finderで表示をクリックします。

![img-tagc102](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc102.png)
ダウンロードフォルダに入っているのが確認できました。

![img-tagc103](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc103.png)
ダウンロードフォルダからデスクトップに移動します。

もう1つの画像を同様の手順でデスクトップまで移動していきます。
![img-tagc104](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc104.png)

2つの画像がデスクトップにダウンロードできました。

![img-tagc105](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc105.png)

### 新しいimgフォルダを作って画像を入れましょう。

![img-tagc106](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc106.png)
css-test.htmlで新しいフォルダを作ります。

css-testフォルダの上で右クリック＞新規フォルダ＞imgと入力してエンターキーの順で作ります。


![img-tagc107](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc107.png)
imgフォルダができたら、デスクトップから先ほどの画像２枚をドラッグアンドドロップでimgフォルダに入れます。![img-tagc108](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc108.png)

![img-tagc109](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc109.png)

これで準備が整いました。

**画像を入れていきます**

## ここからは下記の画像に使うプロパティを学んでいきます。
このプロパティを使って下記のようなデザインができます。
![img-tagc144](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc144.png)
- widthプロパティ
- heightプロパティ
- background-colorプロパティ
- background-sizeプロパティ
- background-repeatプロパティ
- displayプロパティ


css-test.htmlに下記を入力していきます。
```
<img src="img/sokisoba-2.jpg">

```
![img-tagc110](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc110.png)
けっこう簡単で、img src="画像のURL" を指定してあげるだけで、画像を入れる事ができます。

![img-tagc111](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc111.png)
これで画像の挿入位置を書き込みました。

![img-tagc112](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc112.png)
画像が挿入できました。
しかし、画像が大きすぎて、Webブラウザから見えなくなってしまっています。

これをcssでデザインしていきましょう。
### widthのサイズを指定して、画像サイズを決める

css-test.cssに入力していきます。
```
img{
width:800px;
}

```

![img-tagc113](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc113.png)
cssに入力したら、セーブしてWebブラウザで更新してみましょう。


![img-tagc114](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc114.png)

かなり美味しそうになりました

サイズを800pxで指定しているのは、pcでWebページを見るときにWordPressで指定するのによく使うサイズだからです。

**幅を指定しましたが、縦横比はそのまま、Width(幅)のサイズに合わせてサイズ変更されています。**

### heightのサイズを指定して、画像サイズを決める

次はタコライスの画像を使います。
css-test.htmlに入力していきます。

```
<img src="img/tacorice-2.jpg">
```
![img-tag115c](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc115.png)
css-test.htmlに入力できました。
Webブラウザを更新すると、次のように表示されています。


![img-tagc116](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc116.png)
美味しそうなタコライスが表示されています。
初めて沖縄に行ったとき、　タコライスってこんなのなんだ！と思う人もいますね。ただ写真が大きすぎて、**たくさんスクロールしないと文字が見えなく、メニューとしてイマイチかな**と思います。


**見やすいようにheight(高さ)を250pxにしてみましょう。
css-test.cssに入力していきます。
**先ほどのcssに入力したimgをwidthプロパティ変えてみます。

```
img{
  height:250px;
}

```
![img-tagc117](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc117.png)
cssに入力できました。セーブしてWebブラウザで更新してみます。

![img-tagc118](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc118.png)
ちょうどいい感じになりました。
ソーキそばとタコライスの写真が同じ大きさじゃないので、バランス的にイマイチです。

このようなバランスを崩さないためには
写真サイズを最初から同じようにしておく事が必要になります。

ちなみに、実際にはやりませんが、下記のようにwidth(横プロパティとheight（縦）プロパティの2つを指定すると、バランスが崩れます。

**実際にはやりません。今回は画像を見るだけです。**
css-test.cssに
入力内容は下記の感じ。
```
img{
  width:500px;
  height:250px;
}

```

**「縦横をいい感じにしようと思って同時に指定してみた！」**と言う意図です。
css-test.cssに入力したのはこんな感じです。

![img-tagc119](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc119.png)

webブラウザをみてみると、こんな感じになっています。
![img-tagc120](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc120.png)
なんかへんな感じになっていますよね。
確かに縦横を指定することはできますが、画像は醜くなってしまっています。

最初から画像のサイズは決めておくのがベストです。





## background-imgeプロパティで、背景を変えることもできます。
このようなレイアウトも可能です。
![img-tagc130](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc130.png)

背景の画像を入れてみましょう。
先ほどはpタグの下に画像を入れていましたが、
今回はpタグの背景に画像を入れてみましょう。

css-test.htmlに入力します。


```
<div>
  <p>ソーキそば</p>
</div>

```
ソーキそばをdivタグで囲みます。

囲むと、以下のようになりました。
![img-tagc121](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc122.png)
これではまだ何も変化していません。


次はcss-test.cssに、background-imageプロパティを入力していきます。


```
div{
  background-image: url("img/sokisoba-2.jpg");
}

```
と入力します。
下記のようになりました。
![img-tagc122](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc122.png)

こうすることで、webブラウザはソーキそばの部分だけ、写真が反映されています。

写真の一番上の部分だけですね。

![img-tagc123](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc123.png)

ではここから、画像が全部見るように見栄えを整えていきます。
高さを1000pxにしてみましょう。
css-test.cssに入力します。

div{
  height:1000px;
  background-image: url("img/sokisoba-2.jpg");
}

css-test.cssの方は下記のようになっています。
![img-tagc124](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc124.png)


セーブして、Webブラウザを更新します。

![img-tagc125](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc125.png)
かなり大きく背景が適用されました。

しかし、今のままでは広がっているだけで全体的に見えていませんし、見栄えが悪いです。

**少しCSSを指定して、みやすく変えていきましょう。**

### background-sizeプロパティを使って背景画像を整えます。
background-sizeプロパティにcoverを指定することで、画像全部が表示されるようになります。
css-test.cssの
divタグに下記を追記します。
```
background-size: cover;

```
![img-tagc126](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc126.png)
入力すると、下記のようになります。

Webブラウザを更新すると、先ほどよりも写真が写るようになりました。
![img-tagc127](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc127.png)
なぜうまく表示されないのかというと
写真が大きすぎるからです。

ブラウザを横幅を広くすると、全体的に表示されてます。

![img-tagc128](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc128.png)
うまく表示されています。

ただ、これだけ広くブラウザを使ってくれる方も少ないので、サイズを指定してみましょう。


background-sizeプロパティは％で指定もできますので、50%で指定してみましょう。

```
background-size: 50%;

```

![img-tagc129](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc129.png)
サイズを50％に指定してみました。


Webブラウザを更新してみると
![img-tagc130](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc130.png)
きれいに分割されていますね。
このように％指定することで分割されますので、**背景に画像を繰り返したいときに使えます。**


### サイズは小さくしたいけど、リピートしなくていいときに使うbackground-repeatプロパティ


複数画像にはしたくない・・・そんな時は下記のプロパティを１行加えればそれで大丈夫です。

css-test.cssに入力します。
入力箇所は先ほどのdivタグの中です。

```
background-repeat: no-repeat;

```
![img-tagc131](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc131.png)
入力したら、Webブラウザを更新します。

![img-tagc132](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc132.png)

ちょうどいいサイズに収まりました。


backgroundプロパティはこの辺りが一番よく使うものになります。

画像の配置は
- widthプロパティ
- heightプロパティ
- background-colorプロパティ
- background-sizeプロパティ
- background-repeatプロパティ

が基礎なので、ぜひできるようになってください。

***

## よく使う横並びのやり方をdisplayプロパティでやってみましょう。
サイトのナビゲーションを作れます。
![img-tagc144](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc144.png)

![img-tagc133](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc133.png)
Webサイトのナビゲーションが横並びになっているのがわかるでしょうか？

これはブロック要素をdisplayプロパティを使うことでできます。

**ブロック要素と、インライン要素を覚えているでしょうか？**

ブロック要素を実際に使って思い出してみましょう。

css-test.htmlに入力します。
h1タグとh2タグの間に入れます。

```
<p>オススメメニュー</p>
<p>おいしい食べ方</p>
<p>セットメニュー</p>
<p>お持ち帰りメニュー</p>
```
入力すると、以下のようになります。
![img-tagc134](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc134.png)

Webブラウザを更新すると、下記のようになりました。

![img-tagc135](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc135.png)

これがブロック要素です。

イメージすると、pタグが1つずつブロックになって、積み重なっている感じです。

![img-tagc136](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc136.png)

だから改行されているんですね。

displayプロパティを使って、横並びにする事ができます。
これでナビゲーションメニューにするんです。
![img-tagc137](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc137.png)

pタグの部分を横並びにしますが、
pタグはたくさんあるので、divタグで囲んでしまいましょう。

先ほどのメニューの部分だけ囲みます。
divタグもソーキそばのところで使っているのでclassで名前をつけます。

css-test.htmlに入力します。
```
<div class="nav">
  <p>オススメメニュー</p>
  <p>おいしい食べ方</p>
  <p>セットメニュー</p>
  <p>お持ち帰りメニュー</p>
</div>
```

![img-tagc138](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc138.png)


次に、divに指定したnav classに対して、displayプロパティを適用させていきましょう。


css-test.cssに入力していきます。

```
.nav p{
  display: inline;
}
```
このようになりました。

![img-tagc139](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc139.png)

Webブラウザを更新してみると、
![img-tagc140](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc140.png)

- オススメメニュー
- おいしい食べ方
- セットメニュー
- お持ち帰りメニュー

の4つが横並びになりました。

**しかし、変な部分にソーキそばの写真が入ってしまっています。**


これはcssがうまくいっていないからおこっています。

### CSSのエラー解決
![img-tagc141](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc141.png)
今回Webブラウザの表示がおかしくなってしまった原因は上の画像の通りです。

**問題点**　：　このdivタグに、ソーキそばのbackground-imageが適応されてしまっています。

**解決策１**：　ソーキそばのbackground-imageのcssを消してしまう。


**解決策２**：　ソーキそばのbackground-imageのcssにclassをつける。

解決策は2つありますが、今回は背景画像を使わないので、cssを消してしまいましょう。


css-test.cssの、消すcssは以下です。

```
div{
  height:1000px;
  background-image: url("img/sokisoba-2.jpg");
  background-size: 50%;
  background-repeat: no-repeat;
}
```
cssを消す前は下記の画像です。
![img-tagc142](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc142.png)



消すと、下記のようになります。
![img-tagc143](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc143.png)

webブラウザを更新してみましょう。

うまくいきましたね！


![img-tagc144](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc144.png)


このように横並びにする方法でナビゲーションメニューは作られます。

実際にナビゲーションを作る時はプロフィールページの作成で実際にやりますので、楽しみにしていてください。

***
## サイトデザインを整える余白の作り方を学びます。
余白を学ぶことで、サイトのレイアウトを作ることができます。
![img-tagc181](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc181.png)

- borderプロパティ
- margin （外側の余白)
- padding (内側の余白)

の3つについて学びます。

### borderプロパティを使って、線を引き、目立たせたり仕切りをつけることができます。

先ほどのメニューに線を引いていきましょう。

今回はCSSからです。
**.nav pに追加していきます。**
css-test.cssに入力します。
```
border: solid red;

```

- solid １本線
- red   赤色

という意味があります。
赤色の１本線を引くというCSSです。


追加したcssは下記のようになりました。

![img-tagc145](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc145.png)

そしてWebブラウザを更新すると下記のようになりました。

![img-tagc146](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc146.png)
赤いラインで囲まれました。
これがborderプロパティです。
#### 色を変えることもできます。

これも統一感を出すために、沖縄のイメージの青に変更してみます。
css-test.cssに入力します。
```
border: solid blue;

```
cssは少し変更するだけですね。
![img-tagc147](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc147.png)

cssをセーブして、Webブラウザを更新します。
![img-tagc148](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc148.png)

#### さらに、線を細くして、スタイリッシュにします。
**border-width:thin;を使うと、線を細くできます。**

css-test.cssに入力します。
```
border-width:thin;
```

cssに１行追加すると線を細くすることができます。
![img-tagc149](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc149.png)

セーブしてWebブラウザを更新します。

![img-tagc150](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc150.png)

線が目立ちすぎず、いい感じになってきました。

**値には数値にpなどの単位を付けて細かく指定する方法と、thin（細い線）、medium(通常の線）、thick(太い線）などのキーワードをつかって大まかな設定も出来ます。**

### margin （外側の余白)とpadding (内側の余白)を使って、バランスをよくする
**まず、padding(パディングと読みます。)から設定していきましょう。**


先ほどと同じ、.nav pのCSSに追加で入力していきましょう。
```
padding:20px;
```
CSSは下記の通りになりました。

![img-tagc151](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc151.png)

セーブしてWebブラウザを更新すると、スペースがあいて、みやすくなりました。
![img-tagc152](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc152.png)

paddingは内側の余白を使うCSSです。

![img-tagc153](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc153.png)


pタグの文字から上、右、下、左の４方向に20pxずつ余白を開けて、線が引かれています。


**次にmargin(マージンと読みます。)を設定しましょう。**

先ほどと同じ、.nav pのCSSに追加で入力していきましょう。
```
  margin: 10px;
```


css-test.cssに入力したら下記のようになります。

![img-tagc154](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc154.png)

セーブしてWebブラウザを更新すると、下記のようになりました。
1つ1つが若干離れて、みやすくなりました。
![img-tagc155](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc155.png)


マージンは外側の余白を使うCSSなので、下記のようになります。
隣同士になると、今回のように10px+10pxずつ余白ができるので、20px空いているように見えます。

![img-tagc156](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc156.png)

### marginとpaddingの細かい指定方法を学んでみましょう。

h2タグである「沖縄にきたらこれ！オススメメニュー」にCSSを適用してみてみましょう。


まず、css-test.cssに入力します。

```
h2{
  border: solid blue;
  padding: 10px;
}

```
入力したら、以下のようになります。
![img-tagc157](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc157.png)

webブラウザを更新して、確認してみると以下のようになっています。
![img-tagc158](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc158.png)

ここから、まずpaddingの位置の指定を確認していきましょう。
**paddingを位置指定して入れ替えながら確かめます。**

```
padding-top:50px;

```
入力すると、下記のようになります。
![img-tagc159](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc159.png)

Webブラウザでは下記のようになっています。

![img-tagc160](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc160.png)
四角の中の上側の空間が空きました。

**次は右側を開けてみます。**

css-test.cssに入力します。
```
padding-right:500px;
```
- topをrightに変えました。
- 50pxから500pxに変えました。（50pxだとわからないので）

入力すると、下記のようになります。
![img-tagc161](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc161.png)


四角の中の右側が空きました。

![img-tagc162](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc162.png)

**次は下を開けてみます。**

css-test.cssに入力します。
```
padding-bottom:50px;
```
- rightをbottomに変えました。
- 500pxから50pxに変えました。

入力すると、下記のようになります。
![img-tagc163](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc163.png)


四角の中の下側が空きました。

![img-tagc164](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc164.png)

**次は左側を開けてみます。**

css-test.cssに入力します。
```
padding-left:500px;
```
- topをrightに変えました。
- 50pxから500pxに変えました。（50pxだとわからないので）

入力すると、下記のようになります。
![img-tagc165](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc165.png)


四角の中の左側が空きました。

![img-tagc166](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc166.png)

**上、右、下、左を一括で指定することができます。**

今の指定したものをまとめてcss-test.cssにに書き込んでみます。

```
h2{
  border: solid blue;
  padding-top:50px;
  padding-right:100px;
  padding-bottom:50px;
  padding-left:100px;

}
```
rightとleftの500pxは100pxに変更しています。

入力すると、下記のようになります。
![img-tagc167](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc167.png)

Webブラウザを更新すると、以下のようになりました。
よく目立つデザインになってきました。


![img-tagc168](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc168.png)

**さらに、もっと簡単にCSSをかけます**
ここで、ポイントとなるのは、
上、右、下、左の順だと言うことです。
```
h2{
  border: solid blue;
  padding:50px 100px 50px 100px;

}
```
入力すると、下記のようになります。
![img-tagc169](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc169.png)

Webブラウザを更新すると、以下のようになりました。
![img-tagc170](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc170.png)
先ほどと変わりません。

![img-tagc153](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc153.png)

このように、paddingは外枠と内側の文字の空間を設定することができます。

### margin(マージン)を設定してみましょう

![img-tagc156](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc156.png)
**設定はpaddingと一緒なので、さらっといきましょう。**


**まずは上を開けてみます。**
先ほどのpaddingの下に、追加で入力します。
```
margin-top:30px;

```
入力すると、下記のようになります。
若干上に隙間が空いています。
![img-tagc171](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc171.png)

Webブラウザでは下記のようになっています。

![img-tagc172](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc172.png)
わかりにくいですが、
四角の中の上側の空間が空きました。

ちなみに、大胆に100px開けてみると・・・。
![img-tagc173](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc173.png)
これはみるだけです。元に戻しますね。

**次は右側を開けてみます。**

css-test.cssに追加で入力します。
```
margin-right:60px;
```


入力すると、下記のようになります。
![img-tagc174](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc174.png)


四角の中の右側が空きました。

![img-tagc175](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc175.png)

**次は下を開けてみます。**

css-test.cssに追加で入力します。
```
margin-bottom:50px;
```


入力すると、下記のようになります。
![img-tagc176](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc176.png)


四角の中の下側が空きました。

![img-tagc177](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc177.png)

**次は左側を開けてみます。**

css-test.cssに入力します。
```
margin-left:60px;
```


入力すると、下記のようになります。
![img-tagc178](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc178.png)


四角の中の左側が空きました。

![img-tagc179](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc179.png)



**もうわかってきたかもしれませんが、もっと簡単にCSSをかけます**
ここで、ポイントとなるのは、marginも
上、右、下、左の順だと言うことです。
```
h2{
  border: solid blue;
  padding:50px 100px 50px 100px;
  margin: 30px 60px 50px 60px;

}
```
入力すると、下記のようになります。
![img-tagc180](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc180.png)

Webブラウザを更新すると、以下のようになりました。
![img-tagc181](https://blog.job555.info/wp-content/uploads/2020/06/img-tagc181.png)
先ほどと変わりません。

このように、marginとpaddingを使って、Webサイトの空間をデザインしていくことができます。




テキストにデザインを当てる方法の1つですが、画像にも使うことができます。
文字の色や大きさ,
背景色などを変えることができるようになります。



サイトデザインを整えるための余白の考え方でした。

- borderプロパティ
- margin(外側の余白)
- padding(内側の余白)

今回は上記の内容でした。

これでCSS講座は終了です。
