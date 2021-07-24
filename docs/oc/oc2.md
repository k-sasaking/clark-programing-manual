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
var random = Math.random()

console.log(random)
```

出力結果が分かる通り、乱数は0.xxxxxxという値をランダムに表示します。

<br/>
<br/>


### １桁のランダムな数を作る
１桁のランダムな数を作りたい場合は、以下のような考え方で作ります。


**乱数×10倍 → 小数点を切り捨て**


コードで書くと以下のように書くことができます。

```
var random = Math.random() * 10

var result = Math.floor(random)

console.log(result)
```

**Math.floor(少数)は、少数を切り捨てるという意味です。**


n桁のランダムな数を作る

２桁の場合は、×100

３桁の場合は、×1000

４桁の場合は、×10000

とするだけで、好きな桁の乱数が作れます。


```
var random2 = Math.random() * 100 // 2桁
var random3 = Math.random() * 1000 // 3桁
var random4 = Math.random() * 10000)// 4桁

var result2 = Math.floor(random2) //小数点切り捨て
var result3 = Math.floor(random3) //小数点切り捨て
var result4 = Math.floor(random4) //小数点切り捨て

console.log(result2)
console.log(result3)
console.log(result4)
```

<br/>
<br/>


### その他の乱数
例えば、０、１、２のランダムの数を作りたい場合、以下のように考えます。

１桁の乱数を作る → ３で割った余りを出す

```
var random = Math.random() * 10

var result = Math.floor(random) % 3

console.log(result)
```


もしくは、

乱数に3をかける

```
var random = Math.random() * 3

var result = Math.floor(random)

console.log(result)
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
var members = ["田中さん", "中山さん", "山川さん", "川村さん", "村田さん"]

console.log(members)
```

<br/>


### 配列の取得

配列の値を取得するには、番号を指定することで取得できます。

```
var members = ["田中さん", "中山さん", "山川さん", "川村さん", "村田さん"]

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

<br/>
<br/>


### 配列の操作

① 配列の値を更新する

例）村田さんを村上さんに変更する

```
var members = ["田中さん", "中山さん", "山川さん", "川村さん", "村田さん"]

members[4] = "村上さん"

console.log(members[4])
```

② 配列の値を追加する

例）「田口さん」を追加する。

```
var members = ["田中さん", "中山さん", "山川さん", "川村さん", "村田さん"]

members.push("田口さん")

console.log(members)
```

<br/>
<br/>


<div class="enshu">
 演習問題2
</div>

<span style="color:blue;">配列を「りんご」「ばなな」「なし」「もも」「みかん」の５つの要素を持った配列を定義して、表示しましょう。★★★☆☆</span>

```
var fruits = [] //ここに追加

console.log(fruits)
```

<span style="color:blue;">出力結果になるように処理を書きましょう。★★★★☆</span>

① 出力結果が「日本」になるように変更してください。

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

<br/>
<hr/>
<br/>

## 占いゲームを作ろう！

<div class="enshu">
 課題
</div>

<span style="color:blue;">① 「大当たり」「当たり」「ハズレ」の配列を表示するプログラムを書きましょう。</span>

- **ヒント**:　配列で「大当たり」「当たり」「ハズレ」を定義する。（配列の変数名をresultsにしてください。）


<span style="color:blue;">② 0,1,2のいずれかのランダムの数を出力しましょう。</span>

- **ヒント**:　乱数を使って、0,1,2を表示しましょう。（最後の結果を変数numberに入れて出力してください。）


<span style="color:blue;">③ プログラムを実行したら、「大当たり、当たり、ハズレ」のいずれかを表示しなさい。</span>

- **ヒント**:　①と②を合わせて使うとできます。


<span style="color:blue;">④ プログラムを実行したら、「大吉、中吉、小吉、吉、末吉、凶、大凶」のいずれかを表示しなさい。</span>

- **ヒント１**:　③の配列を変更して実装してみよう。


<span style="color:blue;">⑤ プログラムを実行したら、結果に合わせてメッセージも表示する。</span>

例）

```
大吉 -> 今日は今まで最高の一日になるでしょう。
吉 -> 今日はいいことが起こるかも
凶 -> いまいち一日。
```


- **ヒント１**:　メッセージ用の配列を準備して、作ってみよう。（配列の名前をmessagesにしてください。）


<span style="color:blue;">⑥ HTMLファイルに組み込んでみましょう。</span>

- **やり方1**：HTMLファイルをダウンロードしよう。<a href="uranai-tmp.html" download="" class="btn btn-success">HTMLファイルダウンロード</a>
- **やり方2**：画像をダウンロードしよう。<a href="uranai.jpeg" download="" class="btn btn-success">画像ダウンロード</a>
- **やり方3**：「uranai-tmp.htmlの上で右クリック」=> プログラムから開く => メモ帳
- **やり方4**：

ファイルを開いたら、34行目あたりの以下のソースコードを変更して、アプリを完成させましょう。

```
    /** >>>>>ここから編集  **/
    // 変数の表示
    var results = ['大吉'];
    var messages = ['おめでとう'];
    // 乱数で結果を取得
    var number = 0;

    /** ここまで編集<<<<<<<< **/
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

