<!--

        ソースコードを見ましたね！
        
        プログラミング学習は、言語学習と同じで使えば使うほど上達します。
        
        どんどん上達するコツは、たくさんコードを書くことです。

        一緒に頑張りましょう！

-->
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

        let h2Tag = document.getElementsByClassName("tag-h2");
        if(h2Tag){
            let tags_count = h2Tag.length
            for(let i=0;i<tags_count;i++){
                h2Tag[0].remove();
            }
        }
    }, 300);
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

    // スクロール時のheader
    const hH = headers[0].clientHeight;
    let pos = 0;
    const onScroll = () => {
        if(pos > hH) {
            headers[0].classList.add('header--unpinned');
        } else {
            headers[0].classList.remove('header--unpinned');
        }
    };
    window.addEventListener("scroll", () => {
        // スクロールするごとにpos（現在地）の値を更新
        pos = window.scrollY;
        onScroll();
    });
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
ol li{
    padding-top: 10px;
    padding-bottom: 10px;
}
</style>


# 1. カリキュラムについて

<a data-toggle="collapse" href="#curriculum" aria-expanded="true" aria-controls="curriculum"> カリキュラム（一年間の流れ） </a>
<div class="collapse show" id="curriculum">
    <div class="border p-3">
        <iframe src="https://docs.google.com/presentation/d/e/2PACX-1vQHBu3W-Qh2nCDJi9eC-vRLT83q9YhO7CpLByOwyEBahqT3PlFQXErvjlTVAe0oT9_sPmxIqtcBEi7U/embed?start=true&loop=false&delayms=60000" frameborder="0" width="500" height="297" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>
    </div>
</div>

<br/>

<a data-toggle="collapse" href="#curriculumFlow" aria-expanded="true" aria-controls="curriculumFlow"> 学習の流れ詳細 </a>
<div class="collapse show" id="curriculumFlow">
    <div class="border p-3">
        <p class="text-center">HTML/CSS入門編 （<a href="#paizaRange">Paizaの学習範囲</a>）</p>
        <p class="text-center">↓</p>
        <p class="text-center">Webデザイン入門（<a href="#paizaRange">Paizaの学習範囲</a>）</p>
        <p class="text-center">↓</p>
        <p class="text-center">自己紹介HP製作</p>
        <p class="text-center">↓</p>
        <p class="text-center">JavaScript体験編 （<a href="#paizaRange">Paizaの学習範囲</a>）</p>
        <p class="text-center">↓</p>
        <p class="text-center">JavaScript入門編 （<a href="#paizaRange">Paizaの学習範囲</a>）</p>
        <p class="text-center">↓</p>
        <p class="text-center">JavaScript 基礎（佐々木/石井の教材）関数＋DOM操作</p>
        <p class="text-center">↓</p>
        <p class="text-center">JavaScript 実践（佐々木/石井の教材）</p>
        <p class="text-center">↓</p>
        <p class="text-center">個人/グループ製作（HTML＆CSS＆JavaScript）</p>
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

<br/>

<a data-toggle="collapse" href="#slackTodo" aria-expanded="false" aria-controls="slackTodo"> slackの登録済みの人がやること４つ </a>
<div class="collapse" id="slackTodo">
    <div class="border p-3">
        <h2>①Slackの通知の設定</h2>
        <ol>
            <li>アプリ左上の「<b>clark-programing▼</b>」を押す</li>
            <li>「<b>環境設定（Preferences)</b>」を押す</li>
            <li>
            「<b>ダイレクトメッセージ&メンション&キーワード</b>」を選択する<br/>
            <img src="img/slack_notification.png" width="500">
            </li>
        </ol>
        <br/>
        <br/>
        <h2>②チャンネルに参加</h2>
        <ol>
            <li>「<b>チャンネル +</b>」を押す</li>
            <li>「<b>チャンネル一覧（Browse）</b>」を押す<br/>
            <img src="img/slack_browse_channel.png" width="500">
            </li>
            <li>
            以下のチャンネルの「<b>参加する</b>」を押す<br/>
                <ul>
                    <li><b>連絡</b></li>
                    <li><b>1-x_202X年度</b></li>
                </ul>
            <img src="img/slack_join_channel.png" width="500">
            </li>
        </ol>
        <br/>
        <br/>
        <h2>③名前の変更</h2>
        <p>slackの表示名が自分の名前の人は大丈夫です。</p>
        <ol>
            <li>アプリ右上の<b>ユーザーアイコン</b>を押す</li>
            <li>「<b>プロフィールの編集(Edit Profile)</b>」を押す</li>
            <li>氏名/表示名を編集する</li>
        </ol>
        <br/>
        <h2>④自己紹介（宿題）</h2>
        <p> 自己紹介チャンネルに自己紹介を記載する</p>
        <p>※他の授業中に送ると他の生徒に通知が入ってしまうので、授業時間を避けて投稿してください。</p>
    </div>
</div>

<br/>

<a data-toggle="collapse" href="#slackRule" aria-expanded="true" aria-controls="slackRule"> slackの使い方とルール（<span style="color:red;"><b>※必読</b></span>） </a>

<div class="collapse show" id="slackRule">
    <div class="border p-3">
        <span style="color:red;"><b>生徒間のDMは原則禁止です。</b></span><br/><i>※slackの登録しているメールアドレスも原則禁止。</i><br/>
        <br/>
        <b>SNS同様、slackの使い方にも情報モラルを持って</b>使ってください。<br/>
        slack内でのコミュニケーションにおいて、<b>校則に反した場合は、生徒指導の対象になります</b>ので、充分注意して使ってください。<br/>
    </div>
</div>

<br/>

<div class="m-5"></div>

# 3.Paizaラーニングについて

<a id="paizaRange" data-toggle="collapse" href="#paizaList" aria-expanded="false" aria-controls="paizaList"> paizaの学習範囲 </a>
<div class="collapse" id="paizaList">
    <div class="border p-3">
    <table>
        <tr>
            <th>#</th>
            <th>講座</th>
            <th>範囲</th>
        </tr>
        <tr>
            <td>1</td>
            <td><a href="https://paiza.jp/works/html/primer" target="_blank">HTML/CSS入門</a></td>
            <td>全てのレッスン</td>
        </tr>
        <tr>
            <td>2</td>
            <td><a href="https://paiza.jp/works/html/primer" target="_blank">Webデザイン入門</a></td>
            <td>
            <ul>
                <li>Lesson1: 全てのチャプター</li>
                <li>Lesson2: 01〜06まで</li>
                <li>Lesson3: 01,02のみ</li>
            </ul>
            </td>
        </tr>
        <tr>
            <td>3</td>
            <td><a href="https://paiza.jp/works/javascript/trial" target="_blank">Javascript体験</a></td>
            <td>全てのレッスン</td>
        </tr>
        <tr>
            <td>4</td>
            <td><a href="https://paiza.jp/works/js/primer" target="_blank">Javascript入門</a></td>
            <td>全てのレッスン</td>
        </tr>
    </table>
    </div>
</div>

<br/>

<a data-toggle="collapse" href="#howToQuestion" aria-expanded="false" aria-controls="howToQuestion"> 質問のやり方 </a>
<div class="collapse" id="howToQuestion">
    <div class="border p-3">
        <h2>わからないことがあった時の手順</h2>
        <ol>
            <li>まずは<b>自分で10分以上調べる</b>。</li>
            <li> <b>各クラスのチャンネル（＃1-x_2021年度）でクラスのみんなに質問</b> <br/>
            <b>先生にslackでDM</b>で質問する/<b>直接手を上げて質問</b>する。</li>
        </ol>
        <h2>クラスチャンネルでの質問について</h2>
        <p><b>クラスのチャンネルでの質問は生徒間で教え合うこと</b>がメインです。</p>
        <p>クラスチャンネルで質問が投稿されていたら、答えられる人がいたら教えてあげてください。</p>
        <p>時間が経っても解決されない場合は、先生から回答することがあります。</p>
        <br/>
        <h2>先生に質問する際の注意点</h2>
        <ul>
            <li>slackでの質問の回答については原則授業中の時間で回答します</li>
            <li>解決するのにどの方法を取るべきかは、自分で判断をしてください。<br/>
            （先生が他の質問対応している場合、返信するのに時間がかかる場合があります。）</li>
        </ul>
    </div>
</div>

<br/>

<div class="m-5"></div>


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
        <p>※上記の方法でダメな場合は、石井先生に相談してください。</p>
    </div>
</div>

<a data-toggle="collapse" href="#qa2" aria-expanded="false" aria-controls="qa2"> Q2)paizaに登録したメールにログインできません。 </a>
<div class="collapse m-3" id="qa2">
    <div class="border p-3">
        <ol>
            <li>石井先生に相談してください。</li>
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
        <p>こちらのWebサイト、slackのクラスチャンネル、連絡チャンネルより、どんなことをしたかキャッチアップをしてください。</p>
        <p>また、paizaの個別学習については、休んだ時間分取り組めると、極端に遅れることはないので、取り組んでみてください。</p>
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

<a data-toggle="collapse" href="#qa6" aria-expanded="false" aria-controls="qa6"> Q6)slackが英語なのですが、日本語設定の方法は？ </a>
<div class="collapse m-3" id="qa6">
    <div class="border p-3">
        <ol>
            <li>アプリ左上の「<b>clark-programing▼</b>」を押す</li>
            <li>「<b>Preferences</b>」を押す</li>
            <li>「<b>Language & reagion</b>」を選択する
            </li>
            <li>「<b>Language</b>」の選択を「<b>日本語</b>」にする</li>
        </ol>
    </div>
</div>


