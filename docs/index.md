<script>
(() => {
    // パスワード認証
    let password = prompt('passwordを入力してください。');

    // 不要なバナー & フッター削除
    let bannerTags = document.getElementById("banner");
    bannerTags.remove();
    setTimeout(() =>{
        let footerTags = document.getElementsByTagName("footer");
        footerTags[0].remove();
    }, 100);
    // タイトルの設定
    let headers = document.getElementsByTagName("header");
    let titles = headers[0].getElementsByTagName("h1");
    titles[0].innerText = "プログラミング基礎 連絡掲示板"
    let descriptions = headers[0].getElementsByTagName("p");
    descriptions[0].innerText = "このページは、プログラミング基礎で伝えたことを休んだ人でも後から復習して見られるようにしたページです。\n授業を休んだり聞き逃したら、こちらのページを確認するようにしてください。"

    // パスワード認証失敗時
    if(password != "clark"){
        var  pageContents= document.getElementsByClassName("wrapper");
        pageContents[0].innerHTML = '<h1 style="margin: 50px;">このページにアクセスできませんでした。</h1>'
        headers[0].remove();
        return
    }

})();
</script>
<link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.4.1/css/bootstrap.min.css" integrity="sha384-Vkoo8x4CGsO3+Hhxv8T/Q5PaXtkKtu6ug5TOeNV6gBiFeWPGFN9MuhOf23Q9Ifjh" crossorigin="anonymous">
<script src="https://code.jquery.com/jquery-3.4.1.slim.min.js" integrity="sha384-J6qa4849blE2+poT4WnyKhv5vZF5SrPo0iEjwBvKU7imGFAV0wwj1yYfoRSJoZ+n" crossorigin="anonymous"></script>
<script src="https://cdn.jsdelivr.net/npm/popper.js@1.16.0/dist/umd/popper.min.js" integrity="sha384-Q6E9RHvbIyZFJoft+2mJbHaEWldlvI9IOYy5n3zV9zzTtmI3UksdQRVvoxMfooAo" crossorigin="anonymous"></script>
<script src="https://stackpath.bootstrapcdn.com/bootstrap/4.4.1/js/bootstrap.min.js" integrity="sha384-wfSDF2E50Y2D1uUdj0O3uMBJnjuUD4Ih7YwaYd1iqfktj0Uod8GCExl3Og8ifwB6" crossorigin="anonymous"></script>

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
</style>


# 1. カリキュラムについて

<a data-toggle="collapse" href="#curriculum" aria-expanded="false" aria-controls="curriculum"> カリキュラム（一年間の流れ） </a>
<div class="collapse" id="curriculum">
    <div class="border p-3">
        <iframe src="https://docs.google.com/presentation/d/e/2PACX-1vQHBu3W-Qh2nCDJi9eC-vRLT83q9YhO7CpLByOwyEBahqT3PlFQXErvjlTVAe0oT9_sPmxIqtcBEi7U/embed?start=true&loop=false&delayms=3000" frameborder="0" width="500" height="297" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>
    </div>
</div>


<div class="m-5"></div>


# 2. Slackについて

<a data-toggle="collapse" href="#slackRegister" aria-expanded="false" aria-controls="slackRegister"> slackへの登録のやり方 </a>
<div class="collapse" id="slackRegister">
    <div class="border p-3">
        <p>① <a href="https://slack.com/intl/ja-jp/downloads/windows" target="_blank">Slack Download for Windows</a>からslackアプリケーションをダウンロードし、インストールをする（<a href="https://slack.com/intl/ja-jp/help/articles/207691318-%E3%83%A2%E3%83%90%E3%82%A4%E3%83%AB%E7%89%88-Slack-%E3%82%92%E3%83%80%E3%82%A6%E3%83%B3%E3%83%AD%E3%83%BC%E3%83%89%E3%81%99%E3%82%8B" target="_blank">スマホアプリ</a>もあります）</p>
        <p>② 招待状のメール or <a href="https://join.slack.com/t/clark-programing/shared_invite/zt-pkyw2cmc-4GFSjpdGeAsmGxC5RTQR3w" target="_blank">こちらのリンク</a>から clark-programingの招待ページへアクセス</p>
        <p>※招待メールが送られてきてない場合は、先生に伝えてください。</p>
        <p>③ アカウントを作成する。（※すでにアカウントが存在する人はログイン）</p>
        <p>その際、名前とパスワードが聞かれます。</p>
        <p>④</p>
    </div>
</div>

<a data-toggle="collapse" href="#slackTodo" aria-expanded="false" aria-controls="slackTodo"> slackの登録できた人がやること </a>
<div class="collapse" id="slackTodo">
    <div class="border p-3">
        <ol>
            <li>チャンネルに参加</li>
            <li>チャンネルに参加</li>
            <li>チャンネルに参加</li>
        </ol>
    </div>
</div>

<a data-toggle="collapse" href="#slackRule" aria-expanded="false" aria-controls="slackRule"> slackの使い方とルール </a>

<div class="collapse" id="slackRule">
    <div class="border p-3">
        表示されました！
    </div>
</div>
<div class="m-5"></div>

# 3.Paizaラーニングについて

<a data-toggle="collapse" href="#paizaList" aria-expanded="false" aria-controls="paizaList"> paizaの学習順番 </a>
<div class="collapse" id="paizaList">
    <div class="border p-3">
        表示されました！
    </div>
</div>

<a data-toggle="collapse" href="#howToQuestion" aria-expanded="false" aria-controls="howToQuestion"> 質問のやり方 </a>
<div class="collapse" id="howToQuestion">
    <div class="border p-3">
        表示されました！
    </div>
</div>

# 4.よくあるQ&A

<a class="mt-3" data-toggle="collapse" href="#qa1" aria-expanded="false" aria-controls="qa1"> paizaのログインパスワードを忘れました </a>
<div class="collapse" id="qa1">
    <div class="border p-3">
        <ol>
            <li><a href="https://paiza.jp/password_resets" target="_blank">paizaのログインページへアクセス</a></li>
            <li>「パスワードを忘れた方はこちら」を押す</li>
            <li>「登録済みのメールアドレスを入力」し、「再設定メール送付」をする</li>
            <li>メールにログインをし、URLからパスワードを再設定する</li>
        </ol>
    </div>
</div>

<a class="mt-3" data-toggle="collapse" href="#qa1" aria-expanded="false" aria-controls="qa1"> paizaに登録したメールにログインできません。 </a>
<div class="collapse" id="qa1">
    <div class="border p-3">
        <ol>
            <li>中村先生もしくは石井先生に相談してください。</li>
        </ol>
    </div>
</div>
