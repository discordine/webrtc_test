# P2Pしたい！
## WebRTC動作デモ用HTML(作: ChatGPT)
どうしてもWebRTCが使ってみたかったので、とりあえずChatGPTくんに作ってもらいました。

共用PCで動かすためにSignalingサーバは無しで、HTML/JSだけ実装です。最悪すぎる非機能要件。本当ならNuxtあたりでwebsocket使いたかった……

結果的にGitHub Pagesでも動く内容となったのでデプロイしています。ただし非機能要件が最悪なせいで現実的にはlocalhostと大して変わりません。理由は後述。
## サーバ無しでSignalingってどうするの？
Signaling情報を手動でコピペします。送信手段がないから仕方ないね♂（レ）。

これのせいで実質localhost専用です。あのさぁ……

Signaling時のCandidateとしてSTUNサーバ(Googleのやつ)を入れてあるので、NAT越えも最低限できるようにはなっているはずです。

他PCと通信する場合は、HTMLをメールなりDiscordなりで送りましょう。動作確認はReadmeを書いたらやります。

※WebRTCの規格はSignaling情報を受け渡しする方法について特に何も指定していないので、理論上は郵便でもメールでもOKということになります。すごい！
