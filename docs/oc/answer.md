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

## 演習の答え


## Day1

### 演習問題１
①「自分の名前」を出力しなさい。 ★☆☆☆☆

```
console.log("クラーク太郎")
```

### 演習問題２
①「こんにちは」だけを出力しなさい。 ★☆☆☆☆

```
var morning = "おはよう"
var afternoon = "こんにちは"
var night = "こんばんは"

console.log(afternoon)
```


② name1とname2の値を入れ替えて表示しなさい。★★★☆☆

```
var name1 = "太郎"
var name2 = "花子"

var name3 = name1
name1 = name2
name2 = name3

console.log(name1)
console.log(name2)
```

### 演習問題３
① 計算練習をしてみよう。★★☆☆☆

```
var a = 100
var b = 3

// 100 + 3の結果を表示
console.log(a +b)

// 100 - 3の結果を表示
console.log(a -b)

// 100 × 3の結果を表示
console.log(a * b)

// 100 ÷ 3の商を表示
console.log(a / b)

// 100 ÷ 3の余りを表示
console.log(a % b)

// 100の3乗を表示
console.log(a ** b)
```

### 演習問題４

① 計算練習をしてみよう。★★★☆☆

```
var num = 100

// 変数numに7を足す
num += 7

console.log(num)


// 変数numに1を足す
num++

console.log(num)
```

### 演習問題５
演算をして結果を表示してみよう★★★★☆

```
var num1 = 100
var num2 = 3
var moji3 = "7"
var moji4 = "5"

// 103を結果表示
console.log(num1 + num2)
// 97を結果表示
console.log(num1 - num2)
// 300を結果表示
console.log(num1 * num2)
// 1を結果表示
console.log(num1 % num2)
// 57を結果表示
console.log(moji4 + moji3)
// 777を結果表示
console.log(moji3 + moji3 + moji3)
// 37を結果表示
console.log(num2 + moji3)
```

### 演習問題６

以下の実行結果になるようにfor文を作りましょう。★★★☆☆

①

```
0
1
2
3
4
```

解答

```
for(var i=0; i<5 ;i++){
    console.log(i)
}
```

②

```
1
2
3
4
```

解答

```
for(var i=1; i<5 ;i++){
    console.log(i)
}
```


③★★★★☆

```
4
3
2
1
```

解答

```
for(var i=1; i<5 ;i++){
    console.log(5 - i)
}
```

<br/>
<br/>


### 終わって暇な人向け！激ムズ応用問題

①出力結果になるように処理を書きましょう。★★★★★

※for文を使ってください。

```
○○○○○○○
```

解答

```
var maru = ""
for(var i=0; i<7 ;i++){
    maru += "○"
}
console.log(maru)
```


②出力結果になるように処理を書きましょう。★★★★★★

※for文を使ってください。

```
○○○○○○○
○○○○○○○
○○○○○○○
○○○○○○○
○○○○○○○
```

解答

```
for(var j=0;j<5;j++){
    var maru = ""
    for(var i=0; i<7 ;i++){
        maru += "○"
    }
    console.log(maru)
}
```


③出力結果になるように処理を書きましょう。★★★★★★★

※for文を使ってください。

```

○
○○
○○○
○○○○
```

解答

```
for(var j=0;j<5;j++){
    var maru = ""
    for(var i=0; i<j ;i++){
        maru += "○"
    }
    console.log(maru)
}
```

④出力結果になるように処理を書きましょう。★★★★★★★

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

解答

```
for(var j=0;j<5;j++){
    var maru = ""
    for(var i=0; i<j ;i++){
        maru += "○"
    }
    console.log(maru)
}

for(var j=0;j<5;j++){
    var maru = ""
    for(var i=0; i<5-j ;i++){
        maru += "○"
    }
    console.log(maru)
}
```

<br/>
<hr/>
<br/>

## Day2

### 演習問題1

乱数を作ろう★★★★☆

① 0から100までの乱数を出力

```
var random = Math.random() * 100

var result = Math.floor(random)

console.log(result)
```


② 0,1,2,3の乱数を出力

```
var random = Math.random() * 10

var result = Math.floor(random) % 4

console.log(result)
```

もしくは

```
var random = Math.random() * 4

var result = Math.floor(random)

console.log(result)
```

### 演習問題2

配列を「りんご」「ばなな」「なし」「もも」「みかん」の５つの要素を持った配列を定義して、表示しましょう。★★★☆☆

```
var fruits = ["りんご", "ばなな", "なし", "もも", "みかん"] //ここに追加

console.log(fruits)
```

<br/>

出力結果になるように処理を書きましょう。★★★★☆

① 出力結果が「日本」になるように変更してください。

② 次の出力結果が「韓国」になるように、②に処理を追加しましょう。

③ 次の出力結果が[ ‘日本’, ‘アメリカ’, ‘韓国’, ‘ロシア’, ‘ドイツ’ ]となるように、③に処理を追加しましょう。

```
var countries = ["日本", "アメリカ", "中国", "ロシア"]

console.log(countries[0]) //①この行を変更する


// ②ここに処理を追加
countries[2] = "韓国"

console.log(countries[2])

// ③ここに処理を追加
countries.push("ドイツ")

console.log(countries)
```

<br/>
<br/>

### 占いゲームを作ろう

① プログラムを実行したら、「大当たり」「当たり」「ハズレ」が表示するプログラムを書きましょう。

- ヒント１:　乱数を使って、大当たり/当たり/ハズレの３つを表示しましょう。（変数名をnumberにしてください。）
- ヒント２:　配列で「大当たり」「当たり」「ハズレ」を定義する。（配列の変数名をresultsにしてください。）

```
var results = ["大当たり", "当たり", "ハズレ"]
var random = Math.random() *10
var number = Math.floor(random) % 3
console.log(results[number])
```

② プログラムを実行したら、「大吉、中吉、小吉、吉、末吉、凶、大凶」のいずれかを表示しなさい。

- ヒント１:　①の配列を変更して実装してみよう。

```
var results = ["大吉","中吉","小吉","吉","末吉","凶","大凶"]
var random = Math.random() * 10
var number = Math.floor(random) % 7
console.log(results[number])
```


③ プログラムを実行したら、結果に合わせてメッセージも表示する。

例）

大吉 -> 今日は今まで最高の一日になるでしょう。

吉 -> 今日はいいことが起こるかも

凶 -> いまいち一日。


- ヒント１:　メッセージ用の配列を準備して、作ってみよう。（配列の名前をmessagesにしてください。）


```
var results = ["大吉","中吉","小吉","吉","末吉","凶","大凶"]
var messages = ["最高！！！","素晴らしい！！","いいね！","そこそこ","まぁまぁ","残念..","最悪..."]
var random = Math.random() * 10
var number = Math.floor(random) % 7
console.log(results[number])
console.log(messages[number])
```


④ HTMLファイルに組み込んでみましょう。

- やり方1：HTMLファイルをダウンロードしよう。<a href="uranai-tmp.html" download="" class="btn btn-success">HTMLファイルダウンロード</a>
- やり方2：画像をダウンロードしよう。<a href="uranai.jpeg" download="" class="btn btn-success">画像ダウンロード</a>
- やり方3：「uranai-tmp.htmlの上で右クリック」=> プログラムから開く => メモ帳
- やり方4：

ファイルを開いたら、34行目あたりの以下のソースコードを変更して、アプリを完成させましょう。

```
    /** >>>>>ここから編集  **/
    // 変数の表示
    var results = ["大吉","中吉","小吉","吉","末吉","凶","大凶"]
    var messages = ["最高！！！","素晴らしい！！","いいね！","そこそこ","まぁまぁ","残念..","最悪..."]
    // 乱数で結果を取得
    var random = Math.random() * 10
    var number = Math.floor(random) % 7

    /** ここまで編集<<<<<<<< **/
```

<br/>
<hr/>
<br/>


## Day3

### 演習問題1


①以下のプログラムを作成しなさい。

- dayが0の時、”平日”
- dayが1の時、”休日”
- それ以外、”不明”

```
var day =  1
var message = ""

if(day == 0){
    message = "平日"
}else if(day == 1){
    message = "休日"
}else{
    message = "不明"
}

console.log(message)
```

② 以下のプログラムを作成しなさい。

xが偶数の場合、「偶数」です。

xが奇数の場合、「奇数」です。

```
var x =  6
var message = ""

if( x % 2 == 0){
    message = "偶数"
}else{
    message = "奇数"
}

console.log(message)
```

③ 以下のプログラムを作成しなさい。

(a)xが0未満かつyが0未満の場合、”掛け算をしたら正になります。”と表示する

(b)xかyどちらか0未満の場合は、掛け算をしたら負になります。”と表示する

(c)それ以外の時は、”掛け算をしたら正になります。”と表示する

```
var x = 10
var y = -10

var message = ""

if( x < 0 && y < 0){
    message ="掛け算をしたら正になります。"

}else if(x < 0 || y < 0){
    message ="掛け算をしたら負になります。"

}else {
    message ="掛け算をしたら正になります。"
}

console.log(message)
```


### ジャンケンゲームを作ろう

① ジャンケンの手を配列で定義し、表示しなさい。

ヒント１:　ジャンケンの手（グー、チョキ、パー）を配列で定義しよう。（変数名はhandsを使用してください。）

ヒント２:　console.logでヒント１を表示

```
var hands = ["グー", "チョキ", "パー"]
console.log(hands)
```
② 自分の手が0の時が「グー」。1の時「チョキ」。2の時「パー」と出力しよう。

ヒント１:　自分の手（my_hand）を定義する。（例: var my_hand = 0 )

ヒント２:　hands配列を使って、自分の手を表示してみよう。

```
var hands = ["グー", "チョキ", "パー"]
var my_hand = 0

console.log(hands[my_hand])
```

③ 相手の手をランダムで決めて表示しなさい。

ヒント１:　相手の手（cp_hand）を乱数を使って定義する。

ヒント２:　hands配列を使って、相手の手を表示してみよう。

```
var hands = ["グー", "チョキ", "パー"]
var my_hand = 0

// 乱数を作ってcp_handに代入
var random = Math.random() * 10
var cp_hand = Math.floor(random) % 3

console.log(hands[cp_hand])
```

④ ジャンケンの勝敗を決めよう。

ヒント１:　自分の手（my_hand）と相手の手（cp_hand）を比較して、「勝ち、負け、あいこ」を判定（if文）
ヒント２:　「勝ち、負け、あいこ」に合わせてメッセージを表示しましょう。

```
var hands = []
var my_hand = 0

// 乱数を作ってcp_handに代入
var cp_hand = //乱数

var message = ""


console.log()
```
④ HTMLファイルに組み込んでみましょう。

やり方1：HTMLファイルをダウンロードしよう。HTMLファイルダウンロード
やり方2：画像をダウンロードしよう。画像ダウンロード
やり方3：「uranai-tmp.htmlの上で右クリック」=> プログラムから開く => メモ帳
やり方4：
ファイルを開いたら、40行目あたりの以下のソースコードを変更して、アプリを完成させましょう。

/** >>>>>ここから編集  **/

// ジャンケンの手を配列で定義
var hands = ["グー"]
// 乱数で結果を取得
var cp_hand = 0
// 勝ち負けの判定
var message = ""

/** ここまで編集<<<<<<<< **/


<script>
(()=>{
    var hd = document.getElementsByTagName('header')
    hd[0].remove();
})();
</script>
<script src="https://code.jquery.com/jquery-3.3.1.slim.min.js" integrity="sha384-q8i/X+965DzO0rT7abK41JStQIAqVgRVzpbzo5smXKp4YfRvH+8abtTE1Pi6jizo" crossorigin="anonymous"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.14.7/umd/popper.min.js" integrity="sha384-UO2eT0CpHqdSJQ6hJty5KVphtPhzWj9WO1clHTMGa3JDZwrnQq4sF86dIHNDz0W1" crossorigin="anonymous"></script>
<script src="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/js/bootstrap.min.js" integrity="sha384-JjSmVgyd0p3pXB1rRibZUAYoIIy6OrQ6VrjIEaFf/nJGzIxFDsf4x0xIM+B07jRM" crossorigin="anonymous"></script>

