# YouTube Playables 用ゲーム 3本

| フォルダ | ゲーム | 操作 |
|---|---|---|
| stack-tower | ブロックを積むタワー。ズレた分は削られる | タップ |
| dodge-drop | 落ちてくる岩を避ける。コインで加点 | 左右ドラッグ |
| color-tap | 文字が表す色をタップ（ストループ系） | 4ボタン |

各フォルダの index.html が本体（1ファイル完結、依存なし）。

## SDK対応済み
- `<script src="https://www.youtube.com/game_api/v1">` 読み込み
- firstFrameReady / gameReady
- onPause / onResume でゲーム停止・再開
- isAudioEnabled / onAudioEnabledChange で音のON/OFF
- saveData / loadData でベストスコア保存
- engagement.sendScore でスコア送信
- 3ゲームごとに requestInterstitialAd（広告）

ローカルでは SDK は no-op なので、そのままブラウザで開いて動作確認できる。

## 投稿手順（ざっくり）
1. Playables の Interest Form から申請（現状は早期アクセス、チャンネル単位で承認）
2. 承認後 Playables Developer Portal で「新しいゲームを追加」
3. フォルダごと zip でアップロード、サムネ・説明・広告設定を入力
4. SDK テストスイートで確認 → 審査提出
