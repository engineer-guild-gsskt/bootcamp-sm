# Pull Request 練習

## 準備

任意の名前の練習用レポジトリを Github 上で作り、PC にクローンしておいてください。[やり方を忘れたら...?](https://github.com/engineer-guild-gsskt/bootcamp-sm/blob/main/Week1/3.HTML%E3%81%A8CSS%E3%81%A7%E9%9D%99%E7%9A%84%E3%81%AA%E3%82%B5%E3%82%A4%E3%83%88%E3%82%92%E4%BD%9C%E3%82%8D%E3%81%86.md)

この説明では、レポジトリ名を`pr-training`とします。

## 新規ブランチ

Pull Request を作る際や、追加、修正を行う際はその都度ブランチを切ることが推奨されています。特に、main ブランチを Vercel 等にデプロイしている場合、ブランチを分けないと、中途半端な更新が本番環境に反映されてしまうといった**事故**が発生しやすくなります。

`git branch`で新しく branch を作成し、`git checkout`で作成したブランチに移動します。

```shell
git branch [新branch名]
git checkout [新branch名]
```

`checkout`にオプション`-b`を付け加えることで、上記 2 つの動作を 1 つにまとめることができます。

```shell
git checkout -b [新ブランチ名]
```

この説明では、ブランチ名を`Yo`とします。

```shell
git checkout -b Yo
```

ファイルを編集して commit しましょう。

```shell
git add .
git commit -m "Tweak"
git push origin Yo
```

## Pull Request 作成

オリジナルと更新したブランチに差分がある状態で Github 上で Repository にアクセスすると、`Compare & pull request` ボタンが表示されます。

![a](https://i.imgur.com/OoxDxtf.png)

これを押すと Pull Request を作成する画面に移行します。
![b](https://i.imgur.com/kJWrhth.png)

title と description を記入して、問題なければ`Create pull request`しましょう。

## Merge

レポジトリの管理権を持ったアカウントで Pull request を開いた時、コンフリクトを起こしていなければ、`Merge pull request`ボタンが表示されています。
![aaa](https://i.imgur.com/WETDu6T.png)

Merge する commit を作成して、`Confirm merge`を行います。
![c](https://i.imgur.com/5Ip2d19.png)

Merge されると Pull Request は`Merged`状態で閉じられます。
![d](https://i.imgur.com/Ck7TlEP.png)

Branch が不要であれば`Delete branch`ボタンで Branch を削除しましょう。

また、local 内の branch も削除しておきます。

```script
git branch -d Yo
```

## 演習

[engineer-guild-gsskt/pr-training](https://github.com/engineer-guild-gsskt/pr-training)を Fork して、何でもいいので Pull Request を送ってみてください。

## 補足

### More Info

[Git 日本語版レファレンスガイド](https://tracpath.com/docs/)

ここでは紹介しきれないコマンド集など
[ryota の Git マニュアル](https://github.com/philip82148/env-setup/tree/main/%E9%96%8B%E7%99%BA%E3%81%AE%E6%89%8B%E9%A0%86)

### おすすめ書籍

[ゼロから学ぶ Git/GitHub 現代的なソフトウェア開発のために](https://www.amazon.co.jp/%E3%82%BC%E3%83%AD%E3%81%8B%E3%82%89%E5%AD%A6%E3%81%B6Git-GitHub-%E7%8F%BE%E4%BB%A3%E7%9A%84%E3%81%AA%E3%82%BD%E3%83%95%E3%83%88%E3%82%A6%E3%82%A7%E3%82%A2%E9%96%8B%E7%99%BA%E3%81%AE%E3%81%9F%E3%82%81%E3%81%AB-KS%E6%83%85%E5%A0%B1%E7%A7%91%E5%AD%A6%E5%B0%82%E9%96%80%E6%9B%B8-%E6%B8%A1%E8%BE%BA/dp/4065352193) 著:渡辺宙志
大学初年度の教科書みたいな感覚で学べる良書。ページ数も多くなく、解説のある演習問題付き。これの内容を覚えておけば使いこなせるようになると思います。
