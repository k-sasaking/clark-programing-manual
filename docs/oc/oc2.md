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

# Day2: プロから学ぶjavascriptで占いゲーム

本講義での最終成果物

<a href="uranai.html" target="_blank">占いゲーム</a>

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

## 1章：乱数の使い方

**乱数**は、**ランダムの数**のことです。 以下のコードで乱数を作ることができます。


```
Math.random()
```

乱数をコンソールに出力してみましょう。

```
console.log(Math.random())
```

出力結果が分かる通り、乱数は0.xxxxxxという値をランダムに表示します。

<br/>
<br/>


### １桁のランダムな数を作る
１桁のランダムな数を作りたい場合は、以下のような考え方で作ります。


**乱数×10倍 → 小数点を切り捨て**


コードで書くと以下のように書くことができます。

```
Math.floor(Math.random() * 10)
```

**Math.floor(少数)は、少数を切り捨てるという意味です。**


n桁のランダムな数を作る

２桁の場合は、×100

３桁の場合は、×1000

４桁の場合は、×10000

とするだけで、好きな桁の乱数が作れます。


```
Math.floor(Math.random() * 100) // 2桁
Math.floor(Math.random() * 1000) // 3桁
Math.floor(Math.random() * 10000) // 4桁
```

<br/>
<br/>


### その他の乱数
例えば、０、１、２のランダムの数を作りたい場合、以下のように考えます。

１桁の乱数を作る → ３で割った余りを出す

```
Math.floor(Math.random() * 10) % 3
```


もしくは、

乱数に3をかける

```
Math.floor(Math.random() * 3)
```

<br/>


<div class="enshu">
 演習問題1
</div>

<span style="color:blue;">乱数を作ろう★★★★☆</span>


① 0から100までの乱数を出力

② 0,1,2,3の乱数を出力


<br/>
<hr/>
<br/>


## 2章：配列

**配列**は、同じようなデータを一つにまとめることができる便利な機能です。

例えば...部活のメンバーの名前を変数にしたい時、以下のようにコードを書くのは大変ですよね？

```
var member1 = "田中さん"
var member2 = "中山さん"
var member3 = "山川さん"
var member4 = "川村さん"
var member5 = "村田さん"
```

上記のコードを配列を使って表すと以下のように書くことができます。

```
var membars = ["田中さん", "中山さん", "山川さん", "川村さん", "村田さん"]

console.log(members)
```

<br/>


### 配列の取得

配列の値を取得するには、番号を指定することで取得できます。

```
var membars = ["田中さん", "中山さん", "山川さん", "川村さん", "村田さん"]

console.log(members[0])
console.log(members[1])
console.log(members[2])
console.log(members[3])
console.log(members[4])
```

以下のように番号を、0,1,2,3,4....と指定することで１つの変数のように扱うことができます。

**※番号は0から始まることに注意！！**

```
members[番号]
```


※以下のように番号がないものを表示すると、**undifined**と表示されてしまうので気を付けましょう。

```
console.log(members[100])
```



### 配列の操作

① 配列の値を更新する

例）村田さんを村上さんに変更する

```
var members = ["田中さん", "中山さん", "山川さん", "川村さん", "村田さん"]

members[5] = "村上さん"

console.log(members[5])
```

② 配列の値を追加する

例）「田島さん」を追加する。

```
var members = ["田中さん", "中山さん", "山川さん", "川村さん", "村田さん"]

members.push("田口さん")

console.log(members)
```



<div class="enshu">
 演習問題2
</div>

<span style="color:blue;">配列を「りんご」「ばなな」「なし」「もも」「みかん」の５つの要素を持った配列を定義して、表示しましょう。★★★☆☆</span>

```
var fruits = [] //ここに追加

console.log(fruits)
```

<span style="color:blue;">出力結果になるように処理を書きましょう。★★★★☆</span>

① 出漁結果が「日本」になるように変更してください。

② 次の出力結果が「韓国」になるように、②に処理を追加しましょう。

③ 次の出力結果が[ '日本', 'アメリカ', '韓国', 'ロシア', 'ドイツ' ]となるように、③に処理を追加しましょう。

```
var countries = ["日本", "アメリカ", "中国", "ロシア"]

console.log() //①この行を変更する


// ②ここに処理を追加

console.log(countries[2])

// ③ここに処理を追加

console.log(countries)
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

