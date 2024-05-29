WebサイトのURL:   https://4lskittta-deno-shirit-10.deno.dev/

環境はdenoを使用しました。
デザインはバックグラウンドイメージを追加しました。//spy x family のanya/
　　　    background-image //　画像を入力
    background-size:cover//背景画像がサイトの全体を覆います。
    background-position: center//景画像を中心に配置します。   
    
server.jsファイルのモディファイでは
if (request.method === "POST" && pathname === "/reset") //htmlのほうで "reset" というpathnameで"POST"メソッドが要求されたら/      
        previousWord = "しりとり";// 初期化した単語を返す
        wordHistories = ["しりとり"]; // 既存の単語の履歴を初期化する
else if(nextWord.length===1){ // 入力されるたんごが１文字であれば
　　　　status:404でerrorMessage4を返す。
else if(wordHistories.includes(nextWord)){　// 入力された単語が "wordHistories"という配列の中にあれば
　　　　status:403でerrorMessage3を返す。
if (previousWord.slice(-1) === nextWord.slice(0, 1)) { // nextwordの０番目の文字から一つの文字がpreviousWordの最後の文字と同じであれば
    if(nextWord.slice(-1)==="ん"){ // nextWordの最後の文字が"ん"であれば
    　　status:402でerrorMessage2を返す
      
html ファイルのほうでは
const response = await fetch(
        "/reset", //pathnameは　reset
method: "POST",   //メソッドは  POST  
location.reload();// ページをリロードする
<button id="resetSendButton">リセット</button>　//　リセットbuttonを作る。
if (response.status === 401) { // status:401であれば
         const errorJson = await response.text(); //レスポンスからテキストデータを取得します。
         const errorObj = JSON.parse(errorJson); //取得したテキストデータをJSONオブジェクトに変換します
         alert(errorObj["errorMessage1"]); //JSONオブジェクトから特定のエラーメッセージを取得し、アラートダイアログに表示します
