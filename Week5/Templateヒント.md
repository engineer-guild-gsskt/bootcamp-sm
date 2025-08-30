# template ヒント

[bootcamp-library-template](https://github.com/engineer-guild-gsskt/bootcamp-library-template)の演習で何をすればいいかわからなくなった方向けにヒントをいくつか置いておきます。

## Fork 先の Update

先週レポジトリを各自 Fork してもらってからいくつか追加コミットがあります。この差分を自分の Fork 先に反映しておきましょう。
自分の Fork 先のページを開くと、オリジナルに変更があったと表示されているので、`Sync fork`しましょう。

![a](https://i.imgur.com/wiQLkUq.png)

remote の更新分を local にも反映させましょう。

```script
git pull origin main
```

## 開発一例

特にこちらから指定する要件は無いため自由に作ってもらって構わないのですが、何からしていいかわからない方のために一例を示しておきます。

### フロントエンド

画面表示(UI)の設計から始めましょう。蔵書検索に必要な部品は何か？
例えば、[国会図書館オンライン](https://ndlsearch.ndl.go.jp/)など。

[Figma](https://www.figma.com/ja-jp/)なり白紙なりに書き起こしましょう。(こちらから白紙を用意することは出来ません。)

全てのページの UI のイメージが出来たら、App Router のルール通りに page.jsx に書き起こしていきます。

### バックエンド

フロントエンドがおおよそ実装できたら、ロジックを実装しましょう。
基本的には`app/api/`に実装していきます。ロジックをフロントエンド側から呼び出せるように page.jsx に加筆するのも忘れずに。

### 困ったら

Gemini や Claude など生成 AI に聞いてみましょう。可能なら Pro などコーディング特化のモデルの使用を推奨。Github のレポジトリごと読み込ませると理解してもらいやすいかも。

### 資料集

[CSS 早見表](https://campers.hateblo.jp/entry/programming-tag-table)  
[Daisy UI](https://daisyui.com/)  
[CSS スタイリングのコツ【レイアウト編】](https://zenn.dev/sassan/articles/4ae67ad2897124)
