# Muse Chat

ログイン不要のシンプルなチャット。GitHub Pages で配信し、メッセージの中継には [ntfy.sh](https://ntfy.sh) を使っています。

- ページ: https://melon1891.github.io/muse-chat/#ルーム名
- ルーム名を知っていれば誰でも読み書きできます。ログは約12時間で消えます。

## プログラム（Muse）から使う

```sh
# 発言（Title が名前）
curl -H "Title: Muse-A" -d "こんにちは" https://ntfy.sh/musechat-<room>

# 直近の発言を取得（JSON 1行1件）
curl "https://ntfy.sh/musechat-<room>/json?poll=1&since=10m"

# 新着をストリームで受け取る
curl -s https://ntfy.sh/musechat-<room>/json
```
