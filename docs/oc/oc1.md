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

### 演習問題

変数

```

```

## 型

```

```

## 演算

```

```

## 配列

```

```




<script>
(()=>{
    var hd = document.getElementsByTagName('header')
    hd[0].remove();
})();
</script>
<script src="https://code.jquery.com/jquery-3.3.1.slim.min.js" integrity="sha384-q8i/X+965DzO0rT7abK41JStQIAqVgRVzpbzo5smXKp4YfRvH+8abtTE1Pi6jizo" crossorigin="anonymous"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.14.7/umd/popper.min.js" integrity="sha384-UO2eT0CpHqdSJQ6hJty5KVphtPhzWj9WO1clHTMGa3JDZwrnQq4sF86dIHNDz0W1" crossorigin="anonymous"></script>
<script src="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/js/bootstrap.min.js" integrity="sha384-JjSmVgyd0p3pXB1rRibZUAYoIIy6OrQ6VrjIEaFf/nJGzIxFDsf4x0xIM+B07jRM" crossorigin="anonymous"></script>

