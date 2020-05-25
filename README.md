# iromonea

#利用アンケートにご協力ください
https://forms.gle/Ki7M2oo6E9GcrcpM9

## 概要
- ZoomやGooglemeetなどで、イロモネアを実現するアプリケーションです
- それぞれが必要なツールを揃える必要があります
- 一人でもお試しすることができ、理論上大多数の人数でもプレイできます
- 開発途中なので、技術的な問題が多々あります。おおらかな目でプレイしてください

## 遊び方
- Python環境→iromonea.pyを実行する
- exeで実行→releasesからwindows packageをダウンロードし、中にあるiromonea.exeを実行

### 最初に(毎回)やること
1. *まずメインメニューで"カメラの選択"ボタンを押します(この画面になるたび必要)*
2.  既に顔が写っていても必ず押してください
3. 次に、OBSなどでpythonの顔が写っているウィンドウを選択してください
4. Zoomのカメラをバーチャルカメラにし、反転していないか確かめましょう

### フリーモード
- 一人で笑顔の検出を試してみるモードです。パラメータをいじれます
### ゲームモード
- 複数人でプレイします。オンライン環境、バーチャルカメラが必要です
1. お名前、パスワードを入力します。
2. グループでプレイ人数と部屋ID、クリア条件を決めておいてください。必ず共通のものを使用します
ホストが複数人であっても大丈夫です。クリア条件を正確にしてください
3. 入室を一回押すとログインします。
4. もう一度入室を押してください。パスワードや人数が同じであれば次に進みます
5. 制限時間を決め、入力します。その他FPSや感知の敏感さなどを決めてください(これは個別の値です)
6. 開始を押します。全員が開始を押すとスタートします
7. 制限時間内にホストが規定の人数を笑わせたらクリア、他は失敗です

## 用意するもの
- OBS virtualcameraなどのバーチャルカメラ
- OBSなどのキャプチャアプリ

##注意事項
- **バックエンドにAWSを使用していますが、課金状況によっては取りやめることがあります**
- そのため、永続的な動作は保証できません
- Zoom最新版では、バーチャルカメラが無効になっている場合があるようです。
- 対処法はググればあります。一応Mac Catalina /Zoom5.0.2では動作を確認しています
- 動作が重いです。これは作者の設計やコードスキルによるところが大きくいと思われます

