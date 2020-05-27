# iromonea
笑わせるホスト、観客のゲストに分かれ、制限時間以内にゲストをn人笑わせれば勝ち、時間が来たら負けをオンラインで実現するアプリです

# 利用アンケートにご協力ください  
https://forms.gle/Ki7M2oo6E9GcrcpM9

## 概要
- ZoomやGooglemeetなどで、イロモネアを実現するアプリケーションです
- それぞれが必要なツールを揃える必要があります
- 一人でもお試しすることができ、理論上大多数の人数でもプレイできます
- 開発途中なので、技術的な問題が多々あります。おおらかな目でプレイしてください

## 用意するもの
**※(Zoomなどでカメラ出力する場合)** 
- OBSなどの配信ソフト
https://obsproject.com/ja/download  
- OBS virtualcameraなどのバーチャルカメラ  
win:https://obsproject.com/forum/resources/obs-virtualcam.539/  
win参考サイト:https://level69.net/archives/26918  
Mac:https://github.com/johnboiles/obs-mac-virtualcam/releases
Mac参考サイト:https://note.com/junky/n/neeeeddf57bde  
注意:MacだとZoomでうまく認識されず、署名を書き換えたりする場合があります(上記参照)

### 画面共有を駆使してバーチャルカメラを使わない方法も可能ですが非推奨です  
(ZoomとGooogleMeet、slackなどで繋ぎまくって一人一サービスで画面共有など)　　

## python環境導入についてはinstllation.mdを参照  

## 遊び方
- Python環境→iromonea/iromonea.pyを実行する
- exeで実行→releasesからwindows packageをダウンロードし、windowspackage/iromonea/iromonea.exeを実行

## OBS
1. OBSを起動する  
2. ツール→バーチャルカメラを起動   
3. 下のソース→"+"ボタン→ウィンドウキャプチャを選択  
4. python-cameraを探す  
5. なければshow hidden windowsにチェックして探す  
6. 赤枠で画面の位置を調整する（フルサイズだとzoomなどに収まらないので小さめで）
7. zoomなどで反転してないか確かめる

  
### 最初に(毎回)やること
1. **まずメインメニューで"カメラの選択"ボタンを押します(この画面になるたび必要)**
2. ***既に顔が写っていても必ず押してください***(ほとんどの人は0番です)  
※デフォルトのカメラは"1"になっていますが、0がバーチャルカメラの場合もあります。0,1,2...というように確かめてください
3. 次に、OBSなどでpythonの顔が写っているウィンドウを選択して、キャプチャーします
4. obsのバーチャルカメラを起動する
4. Zoomを起動し、カメラをバーチャルカメラに変更。反転していないか確かめましょう

### フリーモード
- 一人で笑顔の検出を試してみるモードです。パラメータをいじれます
- ***ここで光のあたり具合やカメラの向きを調整して検出しやすいポジションを見分けると良いでしょう***
### ゲームモード
- 複数人でプレイします。オンライン環境、バーチャルカメラが必要です
1. お名前、パスワードを入力します。
2. グループでプレイ人数と部屋ID、クリア条件を決めておいてください。必ず*共通のもの*を使用します
ホストが複数人であっても大丈夫です。クリア条件を正確にしてください
3. 入室を一回押すとログインします。
4. **もう一度入室を押してください。** パスワードや人数が同じであれば次に進みます
5. 制限時間を決め、入力します。その他FPSや感知の敏感さなどを決めてください(これは個別の値です)
6. 開始を押します。全員が開始を押すとスタートします
7. 制限時間内にホストが規定の人数を笑わせたらクリア、他は失敗です

## 注意事項
- **バックエンドにAWSを使用していますが、課金状況によっては取りやめることがあります**
- そのため、永続的な動作は保証できません
- **逆光などの条件ではうまく表情を判別しない時があります**
- うまく検出されない時はカメラの向きや距離、光のあたり具合を調整しましょう
- Zoom最新版では、バーチャルカメラが無効になっている場合があるようです。
- 対処法は上に書いてあります。一応Mac Catalina /Zoom5.0.2では動作を確認しています
- 動作が重いです。これは作者の設計やコードスキルによるところが大きいと思われます

