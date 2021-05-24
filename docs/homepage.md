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


# ホームページ制作課題について

## 課題内容

以下のWebページを作る。

- 自身のプロフィールページを作成
- 好きな〇〇を紹介するページを作成


サンプルページ：

佐々木プロフィールページ: [https://k-sasaking.github.io/clark-js/profile.html](https://k-sasaking.github.io/clark-js/profile.html)

石井プロフィールページ: xxxxxxx




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



## 課題に取り組むヒント

### 何から取り組めばいいかわからない時どうする？

<p>下記サイトのように、HTMLのみでプロフィールを書いてみてください。どんな内容を</p>

[https://liginc.co.jp/230184](https://liginc.co.jp/230184)

※上記のWebサイトのコードを利用する場合、htmlタグ/headタグ/bodyタグが省略されていますのでご注意ください。（タグの省略について知りたい方は[コチラ](https://agohack.com/html-closetags/)を参照）


プロフィールの項目は、自分で好きに自由に変えて下さい。


## Bootstrapの利用について

<p>paizaラーニングの教材では、古いversionのBootstrapを利用しているため、<b>最新のBootstrapを利用してください。</b></p>

以下の<b>Bootstrap4</b>を利用するようにしてください。

<a href="https://getbootstrap.jp/docs/4.3/getting-started/introduction/" target="_blank">https://getbootstrap.jp/docs/4.3/getting-started/introduction/</a>



<p>上記のサイトに「[スターターテンプレート](https://getbootstrap.jp/docs/4.3/getting-started/introduction/#%E3%82%B9%E3%82%BF%E3%83%BC%E3%82%BF%E3%83%BC%E3%83%86%E3%83%B3%E3%83%97%E3%83%AC%E3%83%BC%E3%83%88)」があるので利用してください。</p>

<p>※paizaのnavigation barが使えないので以下のリンクから好きなものをコピーして使ってください。</p>

<a href="https://getbootstrap.jp/docs/4.3/components/navbar/" target="_blank"></a>


## 課題に取り組む上での注意点

- <a href="#copyright">著作物の利用について</a>
- コードを見やすく書くことを意識すると、修正しやすくなります。
- 全てのページが作成完了したら、「好きな〇〇を紹介するページを作成」を２つ目追加しましょう。
- 
- できた作品は校内のネットワークで見られるようにする予定です。
- また、良い作品は一般公開する場合があります（※一般公開する際は声かけます）。


<h2 id="copyright">著作物の利用について</h2>

<p>Webページを作る際、<b>画像/音声/動画/文章/地図</b>などのデータを利用する場合、勝手に利用/編集した場合、最大で<b>10年以下の懲役又は1000万円以下の罰金</b>に課せられる可能性があります。<br/>
充分注意して正しく引用しましょう。</p>


### 正しい引用方法

- 原則、<b>著作物の引用方法などが記載されていない場合は使用しない。</b>また、<b>使用したい場合は、該当のWebサイトの利用規約/引用のルールに則って正しく引用する</b>こと。

- 引用していいか判断つかないものについては、過去の裁判の判例などを調べること。調べても判断つかないことについては極力やらない。

- 著作者が不快に思うことは原則禁止。

<hr/>

### 利用規約によっては無料で使えるWebサイト

使う場合はライセンスや利用規約は必ず確認すること。

アイコン

- [https://icooon-mono.com/](https://icooon-mono.com/)
- [http://pictogram2.com/](http://pictogram2.com/)
- [https://icon-rainbow.com/](https://icon-rainbow.com/)
- [https://kage-design.com/](https://kage-design.com/)

写真

- [https://www.beiz.jp/summary.htmlhttps://www.beiz.jp/summary.html)
- [https://photosku.com/](https://photosku.com/)



### 著作権ってどんな権利？

著作物（音楽、絵画、写真、図形、映画、など創作物）における、著作者の権利を保護するために認められた権利の総称です。

コピーライトとも呼ばれる。

主に、２つの権利がある。
- <b>著作者人格権</b>：著作者の了承なしに著作物の編集/著作者の公表などをしてはいけない。
- <b>著作権(財産権)</b>：複製/展示/２次的著作物の利用の権利は著作者がもっている。



### 著作物とは？

「個人の思想や考えが反映されているもの」は、全て著作物に該当する。

#### 著作権の対象になるもの
画像/音楽/文章/記事/地図/作文/キャッチコピー/デザイン/ソースコードなど...

個人の思想や考えが含まれているものは、全て著作物です。

※みなさんの作成した作文なども著作物にあたります。


#### 著作権の対象にならないもの
- 客観的事実（ニュースの情報など）
- 著作者が死後70年経った著作物（昔のクラシック音楽など）















