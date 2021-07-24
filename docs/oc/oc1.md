<script>
(() => {
    // 不要なバナー & フッター削除
    let bannerTags = document.getElementById("banner");
    bannerTags.remove();
    setTimeout(() =>{
        let footerTags = document.getElementsByTagName("footer");
        footerTags[0].remove();

        let h2Tag = document.getElementsByClassName("tag-h2");
        if(h2Tag){
            let tags_count = h2Tag.length
            for(let i=0;i<tags_count;i++){
                h2Tag[0].remove();
            }
        }
    }, 300);
    // ヘッダー非表示
    let headers = document.getElementsByTagName("header");
    headers[0].classList.add('d-none');

})();
</script>
<style>
.enshu {
    color: white;
    background-color: blue;
    border: 1px solid;
    padding: 10px 30px;
    display: inline-block;
    margin-bottom: 20px;
}
</style>

# Day1: プロから学ぶjavscriptでプログラミング

<br/>

### 講義動画

<iframe width="560" height="315" src="https://www.youtube.com/embed/p-yH_HIJE-o" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<br/>

本講義ではJavascriptを勉強します。

<br/>
<hr/>

## Javascriptとは？

プログラミング言語の一つで、**Webサイトを表示する際に使われる言語**です。

<br/>

## プログラミングを学ぶコツは？

- **全角/半角**に注意しよう。
- **スペルミス**に注意しよう。
- **エラーのメッセージ**を見てみよう。（英語なので翻訳してみよう）

プログラムは**正直者**です。

**エラーが出たら何かが間違っているので、間違いを探してみよう！**

<br/>
<hr/>
<br/>

## 使うWebサイト

本日は、<a href="https://paiza.io/ja/projects/new" target="_blank">paiza IO</a>を使って実際のコードを書きます。

<br/>

## 使い方

<img src="paiza_io.png">

① 言語を選択

② コードを入力

③ コードを実行する

④ 結果を確認

**※今回は、JavaScriptの言語を使うので「JavaScript」を選択してください。**

<br/>
<hr/>
<br/>

## 1章：出力

文字を出力してみよう！

<br/>
<br/>

以下のコードをコピーして実行してみよう！


```
console.log("hello clark!!")
```

<br/>

すると...


```
hello clark!!
```

と表示されればOKです。

<br/>
<br/>

このように、文字を出力したい時は、以下のように使うと文字が出力されます。


```
console.log("ここに好きな文字を入れてね！")
```

<div class="enshu">
 演習問題１
</div>

<a href="answer.html">　</a>

<span style="color:blue;">①「自分の名前」を出力しなさい。 ★☆☆☆☆</span> 


<br/>
<hr/>
<br/>

## 2章：変数

**変数**とは、数学でいう**x**や**y**のことです。

プログラミングの世界でも変数を使っていろいろな処理をすることができます。

<br/>

以下のプログラムを実行してみよう！

```
var x = "これは変数です。"

console.log(x)
```

**var**は、変数を宣言するという意味です。

**x**は、変数の名前です。

<br/>

上記のコードは、xに「これは変数です。」という値を入れています。

「**=**」の記号は、**右の値を左に「代入する」**という意味です。

<br/>

さらに、x（変数）を出力すると、xの中に入っている値が出力されます。


<br/>
<br/>
<br/>

### 変数の特徴

変数は、**いくつも宣言**できます。

**変数名も自由**に決めることができます。

```
var ohayo = "おはよう"
var thanks = "ありがとう"

console.log(ohayo)
console.log(thanks)
```

<br/>
<br/>

代入は何回もできます。

```
var name = "太郎"
console.log(name)

name = "二郎"
console.log(name)

name = "三郎"
console.log(name)
```

<br/>
<br/>

変数から変数へ代入もできます。

```
var name1 = "太郎"
var name2 = "花子"

console.log(name1)

name1 = name2

console.log(name1)
```

<br/>
<br/>

<div class="enshu">
 演習問題2
</div>

<span style="color:blue;">①「こんにちは」だけを出力しなさい。 ★☆☆☆☆</span>

```
var morning = "おはよう"
var afternoon = "こんにちは"
var night = "こんばんは"

// こんにちはを出力しなさい。

```

<br/>

<span style="color:blue;">② name1とname2の値を入れ替えて表示しなさい。★★★☆☆</span>

```
var name1 = "太郎"
var name2 = "花子"


// ここに処理を追加


console.log(name1)
console.log(name2)
```

期待する出力結果

```
花子
太郎
```

<br/>

※以下のコードを使わないで実装してみよう。

```
name1 = "花子"
name2 = "太郎"
```


<br/>
<hr/>
<br/>


## 3章：型

変数には、「**数字が入る変数**」「**文字が入る変数**」のように、**型**が存在します。

<br/>

例えば、以下の２つの変数はそれぞれ

- name：**文字列の型**
- num：**数字の型**

です。

```
var name = "太郎"
var num = 1
```


<br/>

例えば、**数字が入る変数に文字を入れることはしません。**

一方で、**文字が入る変数に数字を入れることもしません。**

言語によっては、**エラー**になる場合があります。


```
var name = "太郎"
name = 100 // ←この書き方はNG
console.log(name)
```

<br/>
<hr/>
<br/>

## 4章：演算

プログラムは、算数同様に**演算**をすることができます。

いろいろな演算方法を学びましょう。

<br/>

以下のプログラム実行しましょう。

```
var a = 10
var b = 5

console.log(a + b)
console.log(a - b)
console.log(a * b)
console.log(a / b)
console.log(a % b)
console.log(a ** b)
```

<br/>

### それぞれの記号の意味

- 足し算: +
- 引き算: -
- 掛け算: *
- 割り算: /
- 剰余: %
- べき乗: **

<div class="enshu">
 演習問題3
</div>

<span style="color:blue;">① 計算練習をしてみよう。★★☆☆☆</span>

```
var a = 100
var b = 3

// 100 + 3の結果を表示
console.log()

// 100 - 3の結果を表示
console.log()

// 100 × 3の結果を表示
console.log()

// 100 ÷ 3の商を表示
console.log()

// 100 ÷ 3の余りを表示
console.log()

// 100の3乗を表示
console.log()
```

<br/>
<br/>
<br/>

### その他の演算方法

演算の書き方も**いろいろな書き方**があります。

<br/>

以下のプログラムを実行してみましょう。

```
var num = 10
num += 5
console.log(num)
```

<br/>

以下の２つのコードは同じ処理をします。

```
num = num + 5

num += 5
```

<br/>


以下のプログラムを実行しましょう。

```
var num = 10
num++
console.log(num)
```

<br/>

以下の２つのコードは同じ処理をします。

```
num = num + 1

num++
```

この「++」のことを**インクリメント**といいます。

<br/>
<br/>

<div class="enshu">
 演習問題4
</div>

<span style="color:blue;">① 計算練習をしてみよう。★★★☆☆</span>

```
var num = 100


// 変数numに7を足す


console.log(num)


// 変数numに1を足す



console.log(num)
```

<br/>
<br/>

### 文字列の演算

文字列も **＋の演算のみ** 使うことができます。

```
var moji = "私の名前は"
var name = "Tom"
var moji2 = "です。"

console.log(moji + name +moji2)
```

文字と数値の足し算はどうなる？

以下のプログラムを実行してみましょう。

```
var moji = "10"
var num = 5

console.log(num + moji)
```

この結果から分かる通り、**文字列と数値の足し算**は、**文字列**になります。

<div class="enshu">
 演習問題5
</div>

<span style="color:blue;">演算をして結果を表示してみよう★★★★☆</span>

```
var num1 = 100
var num2 = 3
var moji3 = "7"
var moji4 = "5"

// 103を結果表示
console.log()
// 97を結果表示
console.log()
// 300を結果表示
console.log()
// 1を結果表示
console.log()
// 57を結果表示
console.log()
// 777を結果表示
console.log()
// 37を結果表示
console.log()
```


期待する表示結果

```
103
97
300
1
57
777
37
```

<br/>
<hr/>
<br/>

## 5章：繰り返し処理 for文

例えば、以下のように同じ処理を繰り返したいときが出てきます。

```
console.log("おはよう")
console.log("おはよう")
console.log("おはよう")
console.log("おはよう")
console.log("おはよう")
```

例えば、これを100回、1000回繰り返すとなると、コードがとても長ーーーーくなりますね。

<br/>

以下のように書くことで、**5回繰り返す**処理を書くことができます。

```
for(var i=0; i<5 ;i++){
   console.log("おはよう") 
}
```

### for文の使い方

下記のように書くことで、繰り返し処理をすることができます。

```
for(var i=最初の値; i<最後の値; i++)
```

iを最初の値から最後の値まで+1ずつして処理をします。


例）

iが0から10まで繰り返す
```
for(var i=0; i<10 ;i++){
    console.log(i)
}
```

iが3から5まで繰り返す
```
for(var i=3; i<5 ;i++){
    console.log(i)
}
```

<div class="enshu">
 演習問題6
</div>

<span style="color:blue;">以下の実行結果になるようにfor文を作りましょう。★★★☆☆</span>

①

```
0
1
2
3
4
```

②

```
1
2
3
4
```

③★★★★☆

```
4
3
2
1
```

<br/>
<hr/>
<br/>



## 終わって暇な人向け！激ムズ応用問題

<span style="color:blue;">①出力結果になるように処理を書きましょう。★★★★★</span>

※for文を使ってください。

```
○○○○○○○
```

<br/>

<span style="color:blue;">②出力結果になるように処理を書きましょう。★★★★★★</span>

※for文を使ってください。

```
○○○○○○○
○○○○○○○
○○○○○○○
○○○○○○○
○○○○○○○
```

<br/>

<span style="color:blue;">③出力結果になるように処理を書きましょう。★★★★★★★</span>

※for文を使ってください。

```

○
○○
○○○
○○○○
```

<span style="color:blue;">④出力結果になるように処理を書きましょう。★★★★★★★</span>

※for文を使ってください。

```
○
○○
○○○
○○○○
○○○○○
○○○○
○○○
○○
○
```

<br/>
<br/>

### 激ムズ問題解説動画

<br/>

<iframe width="560" height="315" src="https://www.youtube.com/embed/HRelEQjeBwk" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<script>
(()=>{
    var hd = document.getElementsByTagName('header')
    hd[0].remove();
})();
</script>
<script src="https://code.jquery.com/jquery-3.3.1.slim.min.js" integrity="sha384-q8i/X+965DzO0rT7abK41JStQIAqVgRVzpbzo5smXKp4YfRvH+8abtTE1Pi6jizo" crossorigin="anonymous"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.14.7/umd/popper.min.js" integrity="sha384-UO2eT0CpHqdSJQ6hJty5KVphtPhzWj9WO1clHTMGa3JDZwrnQq4sF86dIHNDz0W1" crossorigin="anonymous"></script>
<script src="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/js/bootstrap.min.js" integrity="sha384-JjSmVgyd0p3pXB1rRibZUAYoIIy6OrQ6VrjIEaFf/nJGzIxFDsf4x0xIM+B07jRM" crossorigin="anonymous"></script>

