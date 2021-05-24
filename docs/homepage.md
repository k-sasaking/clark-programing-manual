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
header h1 {
    margin-bottom: 30px;
}
header p {
    margin: 10px;
}
.wrapper h1 {
  border-bottom: solid 3px black;
  font-size: 30px;
  margin-top: 15px;
  margin-bottom: 30px;  
}
.wrapper h2 {
  padding: 0.4em 0.5em;
  font-size: 20px;
  color: #494949;
  background: #f4f4f4;
  border-left: solid 5px #7db4e6;
  border-bottom: solid 3px #d7d7d7;
  margin-top: 10px;
  margin-bottom: 15px;  
}
.wrapper h3 {
  border-bottom: solid 1px black;
  color: #7db4e6;
  margin-top: 5px;
  margin-bottom: 10px;  
}
ol li{
    padding-top: 10px;
    padding-bottom: 10px;
}
.header--unpinned {
    display: none;
}
section {
    margin-top: 30px;
}
ul {
    list-style-type: disc;
}
</style>


# ホームページ制作課題について

## 課題内容

以下のWebページを作る。

- 自身のプロフィールページを作成
- 好きな〇〇を紹介するページを作成


#### サンプルページ

佐々木プロフィールページ: [https://k-sasaking.github.io/clark-js/profile.html](https://k-sasaking.github.io/clark-js/profile.html)

石井プロフィールページ: [https://hiro-107.github.io/hirox/](https://hiro-107.github.io/hirox/)


<br/>

## 課題評価

### 評価の観点

#### 技術点
- 見出しタグが使われている ([参考](https://paiza.jp/works/html/primer/beginner-html1/11000))
- pタグが使われている ([参考](https://paiza.jp/works/html/primer/beginner-html1/11002))
- 画像が正しく表示されている ([参考](https://paiza.jp/works/html/primer/beginner-html3/11020))
- リンクが設置されている ([参考](https://paiza.jp/works/html/primer/beginner-html3/11020))
- リストが使えている ([参考](https://paiza.jp/works/html/primer/beginner-html3/11021))
- テーブルが使えている ([参考](https://paiza.jp/works/html/primer/beginner-html3/11022))
- グリッドシステムが使えている ([参考](https://paiza.jp/works/html/primer/beginner-html3/11025))
- Navigation barが使えている ([参考](https://paiza.jp/works/html/primer/beginner-html3/11021))

#### デザイン点
- レスポンシブなデザインになっている ([参考](https://paiza.jp/works/html/primer/beginner-html2/11014))
- 色使いが工夫されている ([参考1](https://paiza.jp/works/design/primer/design-1/19001))([参考2](https://paiza.jp/works/design/primer/design-1/19003) )
- 余白が見やすいように調整されている([参考1](https://paiza.jp/works/design/primer/design-1/19001))([参考2](https://paiza.jp/works/design/primer/design-1/19006))



#### その他加点項目
- ページの内容がわかりやすくまとまっている

<br/>


## 課題に取り組む上での注意点

- <a href="#">著作物の利用について</a>を一読すること。
- コードを見やすく書くことを意識すると、修正しやすくなります。
- 全てのページが作成完了したら、「好きな〇〇を紹介するページを作成」を２つ目追加しましょう。
- できた作品は校内のネットワークで見られるようにする予定です。
- また、良い作品は一般公開する場合があります（※一般公開する際は声かけます）。

<br/>


## 課題に取り組むヒント

### 何から取り組めばいいかわからない時どうする？

<p>下記サイトのように、HTMLのみでまずはプロフィールを書いてみましょう。</p>

[https://liginc.co.jp/230184](https://liginc.co.jp/230184)

※上記のWebサイトのコードを利用する場合、htmlタグ/headタグ/bodyタグが省略されていますのでご注意ください。（タグの省略について知りたい方は[コチラ](https://agohack.com/html-closetags/)を参照）


プロフィールの項目は、自分で好きに自由に変えて下さい。

<br/>

## Bootstrapの利用について

<p>paizaラーニングの教材では、古いversionのBootstrapを利用しているため、<b>Bootstrap4を利用してください。</b></p>

以下の<b>Bootstrap4</b>を利用するようにしてください。

<a href="https://getbootstrap.jp/docs/4.3/getting-started/introduction/" target="_blank">https://getbootstrap.jp/docs/4.3/getting-started/introduction/</a>

<br/>

<p>上記のサイトに「<a href="https://getbootstrap.jp/docs/4.3/getting-started/introduction/#%E3%82%B9%E3%82%BF%E3%83%BC%E3%82%BF%E3%83%BC%E3%83%86%E3%83%B3%E3%83%97%E3%83%AC%E3%83%BC%E3%83%88" target="_blank">スターターテンプレート</a>」があるので利用してください。</p>

<br/>

<p>※paizaのnavigation barが使えないので以下のリンクから好きなものをコピーして使ってください。</p>

<a href="https://getbootstrap.jp/docs/4.3/components/navbar/" target="_blank">Bootstrap Navigation bar サンプル</a>

<br/>
<br/>
<br/>

<hr/>
<hr/>

## 著作物の利用について

<p>Webページを作る際、<b>画像/音声/動画/文章/地図</b>などのデータを利用する場合、勝手に利用/編集した場合、最大で<b>10年以下の懲役又は1000万円以下の罰金</b>に課せられる可能性があります。<br/>
充分注意して正しく引用しましょう。</p>

<hr/>

### 正しい引用方法

- 原則、<b style="color:red;">著作物の引用方法などが記載されていない場合は使用しない。</b>また、<b>使用したい場合は、該当のWebサイトの利用規約/引用のルールに則って正しく引用する</b>こと。

- 引用していいか判断つかないものについては、過去の裁判の判例などを調べること。調べても判断つかないことについては極力やらない。

- 著作者が不快に思うことは<span style="color:red;">原則禁止</span>。

<hr/>

### 利用規約によっては無料で使えるWebサイト

使う場合は**ライセンスや利用規約は必ず確認する**こと。

#### アイコン

- [https://icooon-mono.com/](https://icooon-mono.com/)
- [http://pictogram2.com/](http://pictogram2.com/)
- [https://icon-rainbow.com/](https://icon-rainbow.com/)
- [https://kage-design.com/](https://kage-design.com/)

#### 写真

- [https://www.beiz.jp/summary.html](https://www.beiz.jp/summary.html)
- [https://photosku.com/](https://photosku.com/)


<hr/>

## 著作権ってどんな権利？

著作物（音楽、絵画、写真、図形、映画、など創作物）における、著作者の権利を保護するために認められた権利の総称です。

コピーライトとも呼ばれる。

主に、２つの権利がある。
- <b>著作者人格権</b>：著作者の了承なしに著作物の編集/著作者の公表などをしてはいけない等。
- <b>著作権(財産権)</b>：複製/展示/２次的著作物の利用の権利は著作者がもっている等。

<hr/>

## 著作物とは？

「**個人の思想や考えが反映されているもの**」は、**全て**著作物に該当する。

#### 著作権の対象になるもの
**画像/音楽/文章/記事/地図/作文/キャッチコピー/デザイン/ソースコード**など...

個人の思想や考えが含まれているものは、全て著作物です。

※みなさんの作成した作文なども著作物にあたります。


#### 著作権の対象にならないもの
- 客観的事実（ニュースの情報など）
- 著作者が死後70年経った著作物（昔のクラシック音楽など）

<a href="https://jrrc.or.jp/study/" target="_blank">著作権クイズにチャレンジする</a>
（※公益社団法人日本複製権センターより）

<a href="https://takizawalaw.com/1935/#3SNS" target="_blank">SNSを利用した著作権問題例</a>


<hr/>

## 正しい引用方法と画像の使い方

<pre style="background-color: #787878;color: #D7d7d7;">
（注5）引用における注意事項
他人の著作物を自分の著作物の中に取り込む場合，すなわち引用を行う場合，一般的には，以下の事項に注意しなければなりません。

（1）他人の著作物を引用する必然性があること。
（2）かぎ括弧をつけるなど，自分の著作物と引用部分とが区別されていること。
（3）自分の著作物と引用する著作物との主従関係が明確であること（自分の著作物が主体）。
（4）出所の明示がなされていること。（第48条）
（参照：最判昭和55年3月28日 ｢パロディー事件｣）
</pre>

<p>引用元:<a href="https://www.bunka.go.jp/seisaku/chosakuken/seidokaisetsu/gaiyo/chosakubutsu_jiyu.html">著作物が自由に使える場合 | 文化庁</a></p>

<br/>

以下のことを気をつけましょう。

- **引用する必然性のあるもの**を使うこと。
- 引用しているかどうかを**視覚的にわかりやすく**する。
- 引用が中心のコンテンツを避ける。（あくまで**補助として使用**）
- 引用元の **「サイト名、記事名、URL」などを明記** する。

<hr/>

## 画像を引用する時の注意点

### フリー素材orオリジナル画像・写真を使う
フリーだからと言って、なんでもかんでも使っていいものではありません。

必ず「<b style="color:red;">利用規約</b>」があるので、確認しましょう。
（実際に、**利用規約を読まずに使われて、裁判になった例もあり**ます。）

利用する場合は、以下の観点を見るようにしましょう。
- <b style="color:red;">商用利用が可能</b>か
- <b style="color:red;">引用元の表記などは必要</b>か
- **画像を加工可能か（記載ない場合は<span style="color:red;">原則禁止</span>）**

<br/>

### ネットで拾った画像は使わない。他者の画像を使いたい場合は許可をとる。

google画像検索やWebサイト上に**アップロードされている画像を無断で使うのは<span style="color:red;">原則禁止</span>**。

使いたい場合は、許可を得ること。（**生徒間でも同様**です）

<br/>

### 直リンク禁止（他社のサーバーに負荷をかけてはいけない）

**直リンク**とは、**aタグのhref属性の値に"https"がついているもの**を使うことです。（直リンクで利用可の場合はOK）

```
href ="https://xxxxxxxxxx.png"
```

直リンクは、相手のサーバーに負荷をかけてしまうため、<span style="color:red;">原則禁止</a>です。

基本は、**利用する画像を自分のPC上にダウンロード**して、利用します。



<script>
(()=>{
    var hd = document.getElementsByTagName('header')
    hd[0].remove();
})();
</script>




