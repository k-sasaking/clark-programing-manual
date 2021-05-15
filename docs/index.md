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
        <ol>
            <li> <a href="https://slack.com/intl/ja-jp/downloads/windows" target="_blank">Slack Download for Windows</a>からslackアプリケーションをダウンロードし、インストールをする（<a href="https://slack.com/intl/ja-jp/help/articles/207691318-%E3%83%A2%E3%83%90%E3%82%A4%E3%83%AB%E7%89%88-Slack-%E3%82%92%E3%83%80%E3%82%A6%E3%83%B3%E3%83%AD%E3%83%BC%E3%83%89%E3%81%99%E3%82%8B" target="_blank">スマホアプリ</a>もあります）</li>
            <li> 招待状のメール or <a href="https://join.slack.com/t/clark-programing/shared_invite/zt-pkyw2cmc-4GFSjpdGeAsmGxC5RTQR3w" target="_blank">こちらのリンク</a>から clark-programingの招待ページへアクセス<br/>
            ※招待メールが送られてきてない場合は、石井先生or佐々木先生に伝えてください。
            <br/>
            <p>招待メールの場合は、JoinNowをクリック</p>
            <img src="img/slack_join_now.png" width="500">
            </li>
            <li>
            アカウントを作成する。<br/>
            アカウント作成時に、名前とパスワードが聞かれますので入力してください。<br/>
            <img src="img/slack_create_account.png" width="500">
            <br/>
            <p>もし、以下のような画面が出てきたら、メールアドレスを入力してください。</p>
            <img src="img/slack_app.png" width="500">
            </li>
        </ol>
    </div>
</div>

<a data-toggle="collapse" href="#slackTodo" aria-expanded="false" aria-controls="slackTodo"> slackの登録できた人がやること </a>
<div class="collapse" id="slackTodo">
    <div class="border p-3">
        <ol>
            <li>Slackの通知の設定<br/>
                <ul>
                    <li>右上の「clark-programing▼」を押す</li>
                    <li>環境設定（Prefarence)を押す</li>
                    <li>
                    「ダイレクトメッセージ&メンション&キーワード」を選択する<br/>
                    <img src="img/slack_notification.png" width="500">
                    </li>
                </ul>
            </li>
            <li>チャンネルに参加<br/>
                <ul>
                    <li>「チャンネル +」を押す</li>
                    <li>チャンネル一覧（Browse）を押す<br/>
                    <img src="img/slack_browse_channel.png" width="500">
                    </li>
                    <li>
                    以下のチャンネルの「参加する」を押す<br/>
                        <ul>
                            <li>連絡</li>
                            <li>1-x_202X年度</li>
                        </ul>
                    <img src="img/slack_join_channel.png" width="500">
                    </li>
                </ul>
            </li>
            <li>
                自己紹介チャンネルに自己紹介を記載する<br/>
                ※他の授業中に送ると他の生徒に通知が入ってしまうので、授業時間を避けて投稿してください。
            </li>
        </ol>
    </div>
</div>

<a data-toggle="collapse" href="#slackRule" aria-expanded="false" aria-controls="slackRule"> slackの使い方とルール </a>

<div class="collapse" id="slackRule">
    <div class="border p-3">
        <span style="color:red;"><b>生徒間のDMは原則禁止です。</b></span><br/>
        SNS同様、slackの使い方にも情報モラルを持って使ってください。<br/>
        slack内でのコミュニケーションにおいて校則に反した場合は、生徒指導の対象になりますので、充分注意して使ってください。<br/>
    </div>
</div>

<div class="m-5"></div>

# 3.Paizaラーニングについて

<a data-toggle="collapse" href="#paizaList" aria-expanded="false" aria-controls="paizaList"> paizaの学習順番 </a>
<div class="collapse" id="paizaList">
    <div class="border p-3">
    <ol>
        <li>「<a href="https://paiza.jp/works/html/primer" target="_blank">HTML/CSS入門</a>」の全てのレッスン</li>
        <li>「<a href="https://paiza.jp/works/design/primer" target="_blank">Webデザイン入門</a>」一部のレッスン</li>
        <li>「<a href="https://paiza.jp/works/javascript/trial" target="_blank">Javascript体験</a>」の全てのレッスン</li>
        <li>「<a href="https://paiza.jp/works/js/primer" target="_blank">Javascript入門</a>」の全てのレッスン</li>
    </ol>
    </div>
</div>

<a data-toggle="collapse" href="#howToQuestion" aria-expanded="false" aria-controls="howToQuestion"> 質問のやり方 </a>
<div class="collapse" id="howToQuestion">
    <div class="border p-3">
        Comming Soon...
    </div>
</div>

# 4.よくあるQ&A

<a data-toggle="collapse" href="#qa1" aria-expanded="false" aria-controls="qa1"> Q1)paizaのログインパスワードを忘れました </a>
<div class="collapse m-3" id="qa1">
    <div class="border p-3">
        <ol>
            <li><a href="https://paiza.jp/password_resets" target="_blank">paizaのログインページへアクセス</a></li>
            <li>「パスワードを忘れた方はこちら」を押す</li>
            <li>「登録済みのメールアドレスを入力」し、「再設定メール送付」をする</li>
            <li>メールにログインをし、URLからパスワードを再設定する</li>
        </ol>
    </div>
</div>

<a data-toggle="collapse" href="#qa2" aria-expanded="false" aria-controls="qa2"> Q2)paizaに登録したメールにログインできません。 </a>
<div class="collapse m-3" id="qa2">
    <div class="border p-3">
        <ol>
            <li>中村先生もしくは石井先生に相談してください。</li>
        </ol>
    </div>
</div>

<a data-toggle="collapse" href="#qa3" aria-expanded="false" aria-controls="qa3"> Q3)slackの招待メールが来ません。 </a>
<div class="collapse m-3" id="qa3">
    <div class="border p-3">
        <ol>
            <li>
            石井先生か佐々木先生に相談してください。<br/>
            もしくは、<a href="https://join.slack.com/t/clark-programing/shared_invite/zt-pkyw2cmc-4GFSjpdGeAsmGxC5RTQR3w" target="_blank">こちらのリンク</a>から招待メールなしで参加できます。
            </li>
        </ol>
    </div>
</div>

<a data-toggle="collapse" href="#qa4" aria-expanded="false" aria-controls="qa4"> Q4)授業を休んだ時、どうすれば良いですか？ </a>
<div class="collapse m-3" id="qa4">
    <div class="border p-3">
        <p>個別学習の時間に休んだ場合かつ進度が遅い場合は、家庭などで学習</p>
    </div>
</div>

<a data-toggle="collapse" href="#qa5" aria-expanded="false" aria-controls="qa5"> Q5)タイピングが苦手です。何か良い方法はありますか？また、どのくらいのタイピング能力があると良いですか？ </a>
<div class="collapse m-3" id="qa5">
    <div class="border p-3">
        <p>
        <a href="https://www.pken.com/tool/typing.html">P検タイピング</a>がおすすめです。</p>
        <p>
        こちらのサイトの「<b>日本語入力</b>」のゲームを<b>5分</b>設定で実施すると、P検○級レベルと出ます。<br/>
        <b>3級レベルあると良い</b>かもです。<b>準2級レベルあれば十分</b>だと思います。
        </p>
        <p>
        タイピングは量をこなせば誰でも結果が出てくるので、基本ポジションを覚えて頑張りましょう！
        </p>
    </div>
</div>

<a data-toggle="collapse" href="#qa6" aria-expanded="false" aria-controls="qa6"> Q6)授業で実施するpaizaラーニングの講座以外の講座に興味があります。受講しても大丈夫ですか？ </a>
<div class="collapse m-3" id="qa6">
    <div class="border p-3">
        <p>授業では、HTML/CSSとJavascript体験、Javascript入門を実施しますが、それ以外の言語は授業内では扱いません。</p>
        <p>他の講座は、各々興味あるものを学習してもらって問題ありません。</p>
        <p>プログラミング言語は似ているところがあるので、Javascriptで学んだことを他の言語で生かせたり、他の言語で学んだことをJavascriptでも生かせ流ことができるので、多角的に学習し、理解を深めることができます。</p>
    </div>
</div>
