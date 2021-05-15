<script>
(() => {
    // パスワード認証
    let password = prompt('passwordを入力してください。');

    // 不要なバナー & フッター削除
    let bannerTags = document.getElementById("banner");
    bannerTags.remove();


    // パスワード認証失敗時
    if(password != "clark"){
        var pageContents = document.getElementById("main_content_wrap");
        pageContents.innerHTML = "このページにアクセスできませんでした。"
        return
    }
    // タイトルの設定
    let headers = document.getElementsByTagName("header");
    let titles = headers[0].getElementsByTagName("h1");
    titles[0].innerText = "プログラミング基礎 連絡掲示板"
    let descriptions = headers[0].getElementsByTagName("p");
    descriptions[0].innerText = "このページは、プログラミング基礎で伝えたことを休んだ人でも後から復習して見られるようにしたページです。\n授業を休んだり聞き逃したら、こちらのページを確認するようにしてください。"

    setTimeout(() =>{
        let footerTags = document.getElementsByTagName("footer");
        footerTags[0].remove();
    }, 1000);

})();


</script>
<link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.4.1/css/bootstrap.min.css" integrity="sha384-Vkoo8x4CGsO3+Hhxv8T/Q5PaXtkKtu6ug5TOeNV6gBiFeWPGFN9MuhOf23Q9Ifjh" crossorigin="anonymous">
<script src="https://code.jquery.com/jquery-3.4.1.slim.min.js" integrity="sha384-J6qa4849blE2+poT4WnyKhv5vZF5SrPo0iEjwBvKU7imGFAV0wwj1yYfoRSJoZ+n" crossorigin="anonymous"></script>
<script src="https://cdn.jsdelivr.net/npm/popper.js@1.16.0/dist/umd/popper.min.js" integrity="sha384-Q6E9RHvbIyZFJoft+2mJbHaEWldlvI9IOYy5n3zV9zzTtmI3UksdQRVvoxMfooAo" crossorigin="anonymous"></script>
<script src="https://stackpath.bootstrapcdn.com/bootstrap/4.4.1/js/bootstrap.min.js" integrity="sha384-wfSDF2E50Y2D1uUdj0O3uMBJnjuUD4Ih7YwaYd1iqfktj0Uod8GCExl3Og8ifwB6" crossorigin="anonymous"></script>

<div class="m-5"></div>

# カリキュラムについて

<a href="#">カリキュラム（一年間の流れ）</a>

<div class="m-5"></div>

# Slackについて

<a href="#"> slackへの登録のやり方 </a>

<a href="#"> slackの登録できた人がやること </a>

<a href="#"> slackの使い方 </a>

<div class="m-5"></div>

# Paizaラーニングについて

<a href="#"> paizaの学習順番 </a>


<div class="m-5"></div>

# その他

## 授業に関することについて

<a href="#"> よくあるQ&A </a>

それでも解決しない場合は、以下のフォームから連絡したら、先生に連絡が届きます。

<form>
<label>生徒氏名：</label><input class="form-control" type="text" />
<br/>
<label>問い合わせ内容：</label>
<br/>
<textarea  class="form-control" rows="5"></textarea>
<br/>
<button type="submit" class="form-control btn btn-primary"> 送信 </button>
</form>








