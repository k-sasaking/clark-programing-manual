<!--

        ソースコードを見ましたね！
        
        プログラミング学習は、言語学習と同じで使えば使うほど上達します。
        
        どんどん上達するコツは、たくさん「アウトプット」をすることです。

        どんどんコードを書いて、スキルアップをしていきましょう！

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
.header--unpinned {
    display: none;
}
section ul {
    list-style-type: disc !important;
    list-style-image: none !important;
}
</style>


# 1. カリキュラムについて

<a class="btn btn-primary" data-toggle="collapse" href="#curriculum" aria-expanded="false" aria-controls="curriculum"> カリキュラム（一年間の流れ） </a>
<div class="collapse" id="curriculum">
    <div class="border p-3">
        <iframe src="https://docs.google.com/presentation/d/e/2PACX-1vQHBu3W-Qh2nCDJi9eC-vRLT83q9YhO7CpLByOwyEBahqT3PlFQXErvjlTVAe0oT9_sPmxIqtcBEi7U/embed?start=true&loop=false&delayms=60000" frameborder="0" width="500" height="297" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>
    </div>
</div>

<br/>

<a id="flow" class="btn btn-primary" data-toggle="collapse" href="#curriculumFlow" aria-expanded="true" aria-controls="curriculumFlow"> 学習の流れ詳細 </a>
<div class="collapse show" id="curriculumFlow">
    <div class="border p-3">
        <p class="text-center">HTML/CSS入門編 （<a href="#paizaRange">Paizaの学習範囲</a>）<br/>（全てのチャプター）</p>
        <p class="text-center">↓</p>
        <p class="text-center">Webデザイン入門（<a href="#paizaRange">Paizaの学習範囲</a>）<span style="color:red;">New 5/17</span><br/>
        <span style="color:red;">範囲</span>（Lesson1:全て  Lesson2:01〜06  Lesson3: 01,02）
        </p>
        <p class="text-center">↓</p>
        <p class="text-center"><a href="homepage.html" target="_blank">自己紹介HP製作</a> <span style="color:red;"> New 5/24</span></p>
        <p class="text-center">↓</p>
        <p class="text-center">JavaScript体験編 （<a href="#paizaRange">Paizaの学習範囲</a>）<br/>（全てのチャプター）</p>
        <p class="text-center">↓</p>
        <p class="text-center">JavaScript入門編 （<a href="#paizaRange">Paizaの学習範囲</a>）<br/>（全てのチャプター）</p>
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

<a class="btn btn-primary" data-toggle="collapse" href="#slackRegister" aria-expanded="false" aria-controls="slackRegister"> slackへの登録のやり方 </a>
<div class="collapse" id="slackRegister">
    <div class="border p-3">
        <ol>
            <li> <a href="https://slack.com/intl/ja-jp/downloads/windows" target="_blank">Slack Download for Windows</a>からslackアプリケーションをダウンロードし、インストールをする（<a href="https://slack.com/intl/ja-jp/help/articles/207691318-%E3%83%A2%E3%83%90%E3%82%A4%E3%83%AB%E7%89%88-Slack-%E3%82%92%E3%83%80%E3%82%A6%E3%83%B3%E3%83%AD%E3%83%BC%E3%83%89%E3%81%99%E3%82%8B" target="_blank">スマホアプリ</a>もあります）</li>
            <br/>
            <li> <p>招待状のメール or <a href="https://join.slack.com/t/clark-programing/shared_invite/zt-pkyw2cmc-4GFSjpdGeAsmGxC5RTQR3w" target="_blank">こちらのリンク</a>から clark-programingの招待ページへアクセス</p>
            <br/>
            <p>※招待メールが送られてきてない場合は、石井先生or佐々木先生に伝えてください。</p>
            <br/>
            <p>招待メールの場合は、<b>JoinNow</b>をクリック</p>
            <img src="img/slack_join_now.png" width="500">
            </li>
            <li>
            アカウントを作成する。<br/>
            アカウント作成時に、<b>名前とパスワード</b>が聞かれますので入力してください。<br/>
            <img src="img/slack_create_account.png" width="500">
            <br/>
            <p>もし、以下のような画面が出てきたら、<b>メールアドレス</b>を入力してください。</p>
            <img src="img/slack_app.png" width="500">
            </li>
        </ol>
    </div>
</div>

<br/>

<a class="btn btn-primary" data-toggle="collapse" href="#slackTodo" aria-expanded="false" aria-controls="slackTodo"> slackの登録済みの人がやること４つ </a> <span style="color:red;">New 5/17</span>
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
        <p>※他の授業中に送ると他の生徒に通知が入ってしまうので、<b>授業時間を避けて投稿</b>してください。</p>
    </div>
</div>

<br/>

<a class="btn btn-primary" data-toggle="collapse" href="#slackRule" aria-expanded="true" aria-controls="slackRule"> slackの使い方とルール </a>（<span style="color:red;"><b>※必読</b></span>）<span style="color:red;">New 5/17</span>

<div class="collapse show" id="slackRule">
    <div class="border p-3">
        <span style="color:red;"><b>生徒間のDMは原則禁止です。</b></span><br/><i>※slackの登録しているメールアドレスも原則禁止。</i><br/>
        <br/>
        <b>SNS同様、slackの使い方にも情報モラルを持って</b>使ってください。<br/>
        slack内でのコミュニケーションにおいて、<b>校則に反した場合は、生徒指導の対象になります</b>ので、充分注意して使ってください。<br/>
    </div>
</div>

<br/>

<a class="btn btn-primary" data-toggle="collapse" href="#howToQuestion" aria-expanded="true" aria-controls="howToQuestion"> 質問のやり方 </a> <span style="color:red;">New 5/17</span>
<div class="collapse show" id="howToQuestion">
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
        <p>slackでの質問の回答については原則授業中の時間で回答します</p>
        <p>解決するのにどの方法を取るべきかは、自分で判断をしてください。<br/>
        （先生が他の質問対応している場合、返信するのに時間がかかる場合があります。）</p>
    </div>
</div>

<div class="m-5"></div>

# 3.Paizaラーニングについて


<a class="btn btn-primary" data-toggle="collapse" href="#howToLearning" aria-expanded="true" aria-controls="howToLearning"> 学習のやり方 </a>
<div class="collapse show" id="howToLearning">
    <div class="border p-3">
        <ol>
            <li><a href="https://paiza.jp/works/courses" target="_blank">paizaラーニング</a>にログインし、学習する<b>コース</b>を選択します。</li>
            <li><b>レッスン</b>を選択 -> <b>チャプター</b>を選択します。</li>
            <li>演習課題がある課題については、<b>演習課題を必ずやる</b>ようにしてください。<br/>
                <img src="img/paiza_practice.png" width="500"/><br/>
                <p>演習問題が複数ある場合もあるので注意</p>
                <img src="img/paiza_practice2.png" width="500"/><br/>
            </li>
            <li>
                <全ての演習課題がsuccessになったらチャプター完了です。<br/>以下の画面のように、<b>全ての演習課題をクリア</b>かつ<b>受講済</b>にしてください。<br/>
                <img src="img/paiza_chapter_finish.png" width="500"/><br/>                
            </li>
        </ol>
        <p>※<span style="color:red;"><b>イヤホンを必ず持参してください。</b></span>イヤホンは学校側で予備がありません。<br/></p>
    </div>
</div>

<br/>

<a class="btn btn-primary" id="paizaRange" data-toggle="collapse" href="#paizaList" aria-expanded="true" aria-controls="paizaList"> paizaの学習範囲 </a> <span style="color:red;">New 5/17</span>
<div class="collapse show" id="paizaList">
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
    <p>学習の順番は、<a href="#flow">カリキュラムの「学習の流れ詳細」</a>を参照してください。</p>
    </div>
</div>

<div class="m-5"></div>


# 4. Visual Studio Codeのインストール

<a class="btn btn-primary" data-toggle="collapse" href="#whatIsVSCode" aria-expanded="true" aria-controls="whatIsVSCode"> Visual Studio Codeとは </a> <span style="color:red;"> New 5/24</span>
<div class="collapse show" id="whatIsVSCode">
    <div class="border p-3">
        <p>エディターと言って、<b>ソースコードを作成/編集するためのソフト</b>の一つです。</p>
        <p>他にもメモ帳, サクラエディタ, Atom, Notepad++, Vimなど、さまざまなエディターがあります。</p>
        <p>今回は、Microsoft社が開発しているエディターで、性能も良く一般的に使われているVisual Studio Code(略:VS Code)をインストールして使用します。</p>
        <p> コーディングサポート機能や拡張性にも優れていて、 マルチプラットフォームにも対応しています。</p>
    </div>
</div>

<br/>

<a class="btn btn-primary" data-toggle="collapse" href="#installVSCode" aria-expanded="true" aria-controls="installVSCode"> Visual Studioのインストール方法 
</a><span style="color:red;"> New 5/24</span>
<div class="collapse show" id="installVSCode">
    <div class="border p-3">
        <h2>Visual Studio Codeのインストール</h2>
        <p>1. 下記のサイトからダウンロード</p>
        <p><a href="https://code.visualstudio.com/download" target="_blank">https://code.visualstudio.com/download</a></p>
        <img src="img/vscode_win.png" width="500"/>
        <br/>
        <p>2. ダウンロードしたファイル(VSCodeUserSetup-x64-X.XX.Xexe)を開く<br/>※Xの部分はバージョンの数字が入ります。</p>
        <br/>
        <p>3. 「次へ」を押す</p>
        <img src="img/vscode_1.png" width="500"/>
        <img src="img/vscode_2.png" width="500"/>
        <img src="img/vscode_3.png" width="500"/>
        <img src="img/vscode_6.png" width="500"/>
        <br/>
        <p>4. インストール完了</p>
        <img src="img/vscode_7.png" width="500"/>
    </div>
</div>

<br/>

<a class="btn btn-primary" data-toggle="collapse" href="#howToMakeHtmlVSC" aria-expanded="true" aria-controls="howToMakeHtmlVSC"> Visual Studio CodeでHTMLファイルを作成する方法
 </a> <span style="color:red;"> New 5/24</span>
<div class="collapse show" id="howToMakeHtmlVSC">
    <div class="border p-3">
        <h2>Visual Studio CodeでHTMLファイルを作成する方法</h2>
        <p>1. デスクトップにフォルダを作成<br/>※自分で管理できる人はデスクトップじゃなくてもOK</p>
        <img src="img/index_html.png" width="500">
        <br/>
        <p>2. 「右クリック → 新規フォルダ →　名前をつける」<br/>※フォルダ名はなんでもよし迷ったときは「プログラミング基礎」にする</p>
        <br/>
        <p>3. フォルダを開き、新規でファイルを作成する</p>
        <p>フィイルの拡張子を表示する。（表示タブ > ファイル名拡張子に✔️）</p>
        <img src="img/index_html_check_view.png" width="500">
        <br/>
        <p>ファイル作成時、名前をindex.htmlにする。</p>
        <img src="img/index_html2.png" width="500">
        <br/>
        <p>※ファイル名変更のやり方（ファイルの上で右クリック > 「名前の変更」）</p>
        <img src="img/index_html_name_change.png" width="500">
        <br/>
        <p>拡張子を変更するアラートが出たら、「はい」を押す。</p>
        <img src="img/index_html3.png" width="500">
        <br/>
        <p>4. Visual Studio Codeを開く</p>
        <p>「フォルダから開く」を押して、作成したフォルダを選択</p>
        <img src="img/index_html4.png" width="500">
        <p>index.htmlが表示されていればOK</p>
        <img src="img/index_html5.png" width="500">
        <br/>
        <p>5. VS Codeでindex.htmlを以下のように編集する</p>
        <pre>
        <code style="color:white;">
&lt;html lang=&quot;ja&quot;&gt;
  &lt;head&gt;
    &lt;!-- Required meta tags --&gt;
    &lt;meta charset=&quot;utf-8&quot;&gt;
    &lt;meta name=&quot;viewport&quot; content=&quot;width=device-width, initial-scale=1, shrink-to-fit=no&quot;&gt;
    &lt;!-- Bootstrap CSS --&gt;
    &lt;link rel=&quot;stylesheet&quot; href=&quot;https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css&quot; integrity=&quot;sha384-ggOyR0iXCbMQv3Xipma34MD+dH/1fQ784/j6cY/iJTQUOhcWr7x9JvoRxT2MZw1T&quot; crossorigin=&quot;anonymous&quot;&gt;
    &lt;title&gt;Hello, world!&lt;/title&gt;
  &lt;/head&gt;
  &lt;body class=&quot;text-center&quot;&gt;
    &lt;h1&gt;テストページです。&lt;/h1&gt;
    &lt;p&gt;Google chromeで確認できましたか？&lt;/p&gt;
    &lt;img src=&quot;lion.jpg&quot; height=&quot;500&quot;/&gt;
    &lt;!-- Optional JavaScript --&gt;
    &lt;!-- jQuery first, then Popper.js, then Bootstrap JS --&gt;
    &lt;script src=&quot;https://code.jquery.com/jquery-3.3.1.slim.min.js&quot; integrity=&quot;sha384-q8i/X+965DzO0rT7abK41JStQIAqVgRVzpbzo5smXKp4YfRvH+8abtTE1Pi6jizo&quot; crossorigin=&quot;anonymous&quot;&gt;&lt;/script&gt;
    &lt;script src=&quot;https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.14.7/umd/popper.min.js&quot; integrity=&quot;sha384-UO2eT0CpHqdSJQ6hJty5KVphtPhzWj9WO1clHTMGa3JDZwrnQq4sF86dIHNDz0W1&quot; crossorigin=&quot;anonymous&quot;&gt;&lt;/script&gt;
    &lt;script src=&quot;https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/js/bootstrap.min.js&quot; integrity=&quot;sha384-JjSmVgyd0p3pXB1rRibZUAYoIIy6OrQ6VrjIEaFf/nJGzIxFDsf4x0xIM+B07jRM&quot; crossorigin=&quot;anonymous&quot;&gt;&lt;/script&gt;
  &lt;/body&gt;
&lt;/html&gt;
        </code>
        </pre>
        <p>編集できたら 「ctrl」+「s」を押して保存する。</p>
        <br/>
        <p>6. 画像をダウンロードして、作成したフォルダ内に保存をしてください。<a href="img/lion.jpg" download class="btn btn-success">画像ダウンロード</a></p>
        <p>ダウンロードしたファイルを作成したフォルダの中にドラッグ＆ドロップする</p>
        <img src="img/index_html_copy_img.png" width="500">
        <br/>
        <p>以下の画像のようにフォルダ内に、index.htmlとlion.pngがあればOKです。</p>
        <img src="img/index_html_img.png" width="300">
        <br/>
        <p>7. Google Chromeを開く</p>
        <p>Google Chromeへ「index.html」をドラッグ＆ドロップする</p>
        <img src="img/index_html6.png" width="500">
    </div>
</div>

# 5.オリジナル教材

<a data-toggle="collapse" href="#original" aria-expanded="true" aria-controls="original"> エクストリーム授業 </a><span style="color:red;"> New 7/8</span>
<div class="collapse m-3" id="original">
    <div class="border p-3">
      <ul>
        <li><a href="https://k-sasaking.github.io/clark-programing-manual/practice/p1.html">エクストリームHTML講座</a></li>
        <li><a href="https://k-sasaking.github.io/clark-programing-manual/practice/p2.html">エクストリームCSS講座</a></li>
        <li><a href="https://k-sasaking.github.io/clark-programing-manual/practice/p3.html">エクストリームBootstrap講座1</a></li>
        <li><a href="https://k-sasaking.github.io/clark-programing-manual/practice/p4.html">エクストリームBootstrap講座2</a></li>
        <li><a href="https://k-sasaking.github.io/clark-programing-manual/practice/p5.html">ホームページの作り方講座</a></li>
      </ul>
    </div>
</div>


# 6.よくあるQ&A

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
        <p>こちらのWebサイト、slackのクラスチャンネル、連絡チャンネルより、どんなことをしたか<b>自身でキャッチアップ</b>をしてください。</p>
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

<a data-toggle="collapse" href="#qa7" aria-expanded="false" aria-controls="qa7"> Q7)Visual Studio Codeの日本語設定の方法は？ </a><span style="color:red;"> New 6/1</span>
<div class="collapse m-3" id="qa7">
    <div class="border p-3">
    <p>日本語化したい人は、以下のURLに詳しい手順が載っているので、参考にしてください。</p>
    <p>
        <a href="https://www.javadrive.jp/vscode/install/index4.html" target="_blank">https://www.javadrive.jp/vscode/install/index4.html</a>
    </p>
    </div>
</div>


<script>
(()=>{
    var hd = document.getElementsByTagName('header')
    var hd_size = hd[0].clientHeight; 
    var pos = 0;
    window.addEventListener('scroll', () => {    
        var current_pos = window.pageYOffset; 
        // UP
        if (current_pos < pos || current_pos > hd_size) {
            console.log("up")
            if(hd[0].classList.length != 0){
                hd[0].classList.remove('d-none');
            }            
        }
        // DOWN
        else {
            if(current_pos > hd_size){
                if(hd[0].classList.length == 0){
                    hd[0].classList.add('d-none');
                }
            }
        }
        pos = current_pos;
    });
})();
</script>
