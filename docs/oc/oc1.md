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


# Day1: プロから学ぶjavscriptでプログラミング

本講義ではJavascriptを勉強します。

## Javascriptとは？

プログラミング言語の一つで、Webサイトを表示する際に使われる言語です。

## プログラミングを学ぶコツは？

- 全角/半角に注意しよう。
- スペルミスに注意しよう。
- エラーのメッセージを検索してみよう。（英語なので理解しましょう）

プログラムは**正直者**です。

**エラーが出たら何かが間違っているので、間違いを探してみよう！**



## 使うWebサイト

<a href="https://paiza.io/ja/projects/new" target="_blank">paiza IO</a>


## 使い方

<img src="paiza_io.png">

① 言語を選択

② コードを入力

③ コードを実行する

④ 結果を確認

**※今回は、javascriptの言語を使うのでjavascriptを選択してください。**

<br/>
<br/>

## 出力

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

<br/>
<br/>

## 変数

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

**=**は、**右の値を左に「代入する」**という意味です。

つまり、変数xに「これは変数です。」という文字を代入しています。

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

### 演習問題

①「こんにちは」だけを出力しなさい。 ★☆☆☆☆

```
var morning = "おはよう"
var afternoon = "こんにちは"
var night = "こんばんは"

// こんにちはを出力しなさい。

```

<br/>

② name1とname2の値を入れ替えて表示しなさい。★★★☆☆

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
<br/>


## 型

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

## 演算

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

### 計算練習をしてみよう。★★☆☆☆

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

### 計算練習をしてみよう。★★★☆☆

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



### 演習問題★★★★☆

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
<br/>
<br/>

## 配列

**配列**は、同じようなデータを一つにまとめることができる便利な機能です。

例えば...部活のメンバーの名前を変数にしたい時、以下のようにコードを書くのは大変ですよね？

```
var member1 = "田中"
var member2 = "中山"
var member3 = "山川"
var member4 = "川村"
var member5 = "村田"
```

上記のコードを配列を使って表すと以下のように書くことができます。

```
var membars = ["田中", "中山", "山川", "山川", "川村", "村田"]
```




## 繰り返し処理



<br/>
<br/>
<br/>




<script>
(()=>{
    var hd = document.getElementsByTagName('header')
    hd[0].remove();
})();
</script>
<script src="https://code.jquery.com/jquery-3.3.1.slim.min.js" integrity="sha384-q8i/X+965DzO0rT7abK41JStQIAqVgRVzpbzo5smXKp4YfRvH+8abtTE1Pi6jizo" crossorigin="anonymous"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.14.7/umd/popper.min.js" integrity="sha384-UO2eT0CpHqdSJQ6hJty5KVphtPhzWj9WO1clHTMGa3JDZwrnQq4sF86dIHNDz0W1" crossorigin="anonymous"></script>
<script src="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/js/bootstrap.min.js" integrity="sha384-JjSmVgyd0p3pXB1rRibZUAYoIIy6OrQ6VrjIEaFf/nJGzIxFDsf4x0xIM+B07jRM" crossorigin="anonymous"></script>

