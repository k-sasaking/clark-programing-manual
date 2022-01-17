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
section ul {
    list-style-type: disc !important;
    list-style-image: none !important;
}
</style>


# ホームページ制作課題について

## 課題内容

以下のゲームを作成する

- 占いゲーム
- クイズゲーム
- ジャンケンゲーム

+ 時間がある人はオリジナルゲーム作成

<br/>

## 課題評価

### 評価の観点

#### 技術点
- 配列が使えている
- 乱数が使えている
- DOMの操作でIDから要素を取得できる
- クリックイベントを追加できる
- if文、for文が使える



<br/>

## 提出期限 <span style="color:red;"> </span>

<span style="color:red;"> 2/9（水） 23:59</span>


## 提出方法 <span style="color:red;"> </span>

■提出先URL

[https://drive.google.com/drive/u/0/folders/1S7t3_F88_bo_O1X083zOO795KR_dLYDq](https://drive.google.com/drive/u/0/folders/1S7t3_F88_bo_O1X083zOO795KR_dLYDq)


#### ① 自分のクラスを選択**
<img src="img/new_deploy_hp0.png">

### ②前期作成したフォルダを選択（ない場合は作成する）

#### ③ デスクトップのゲームフォルダをgoogle driveにドラッグ＆ドロップする。

<img src="img/new_deploy_hp2.png">


**※万が一、操作ミス等で他人のフォルダやクラスのフォルダなどを変更してしまった場合は、先生にDMで連絡してください。**


<script>
(()=>{
    var hd = document.getElementsByTagName('header')
    hd[0].remove();
})();
</script>
<script src="https://code.jquery.com/jquery-3.3.1.slim.min.js" integrity="sha384-q8i/X+965DzO0rT7abK41JStQIAqVgRVzpbzo5smXKp4YfRvH+8abtTE1Pi6jizo" crossorigin="anonymous"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.14.7/umd/popper.min.js" integrity="sha384-UO2eT0CpHqdSJQ6hJty5KVphtPhzWj9WO1clHTMGa3JDZwrnQq4sF86dIHNDz0W1" crossorigin="anonymous"></script>
<script src="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/js/bootstrap.min.js" integrity="sha384-JjSmVgyd0p3pXB1rRibZUAYoIIy6OrQ6VrjIEaFf/nJGzIxFDsf4x0xIM+B07jRM" crossorigin="anonymous"></script>




