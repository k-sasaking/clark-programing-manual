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

<a href="#">カリキュラム（一年間の流れ）</a>

<div class="m-5"></div>

# 2. Slackについて

<a href="#"> slackへの登録のやり方 </a>

<a href="#"> slackの登録できた人がやること </a>

<a href="#"> slackの使い方 </a>

<div class="m-5"></div>

# 3.Paizaラーニングについて

<a href="#"> paizaの学習順番 </a>


<div class="m-5"></div>

# 4. その他

## 4.1 授業について
<a href="#"> よくあるQ&A </a>

<br/>
<br/>

## 4.2 問い合わせ
それでも解決しない場合は、以下のフォームから連絡したら、先生に連絡が届きます。

<label>生徒氏名：</label><input id="studentName" class="form-control" type="text" />
<br/>
<label>問い合わせ内容：</label>
<br/>
<textarea id="studentText" class="form-control" rows="5"></textarea>
<br/>
<a id="inquiry" class="form-control btn btn-primary"> 送信 </a>

<script>
const url = 'https://hooks.slack.com/services/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'
const sendSlack = (messageText) => {
    const payload = {"text": messageText};
    const options =
    {
        "method":"POST",
        "headers":
        {
            "Content-Type":"application/json"
        },
        "body": JSON.stringify(payload)
    };
    fetch(url, options)
      .then((response) => {
        console.log(response)
        if (!response.ok) {
          alert('エラーです')
        }
        else {
                let studentName =  document.getElementById("studentName");
                let studentText = document.getElementById("studentText");
        }
      })
      .catch((error) => {
        console.log(error.message)
      })
  }

let inquiry = document.getElementById("inquiry");
inquiry.addEventListener("click", ()=>{
    if (!confirm("先生へメッセージを送信しますか？"))
        return
    
    let studentName =  document.getElementById("studentName");
    let studentText = document.getElementById("studentText");
    let message = "生徒: " + studentName;
    message += "\nメッセージ:\n" + studentText;
    sendSlack(message);    
})
</script>







