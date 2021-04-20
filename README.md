# README

## セットアップ

サイト作成

```shell
hugo new site hugo-academic
```

レポジトリ初期化

```shell
cd hugo-academic
git init
echo '*~' >> .gitignore
echo '*.bak' >> .gitignore
echo '*.orig' >> .gitignore
echo '.env' >> .gitignore
echo 'public' >> .gitignore
echo 'resources' >> .gitignore
```

テーマ設定(submoduleはhttpsプロトコルで追加)

```shell
git submodule add https://github.com/HumamAlwassel/hugo-academic.git themes/academic
```

(参考)submoduleの削除

```shell
git submodule deinit -f themes/dream
git rm themes/academic
rm -fr .git/modules
```

サイト設定

```shell
cp themes/dream/exampleSite/config.toml .
```

config.toml

```toml
baseURL = "https://example.com/"
languageCode = "en-us"
defaultContentLanguage = "ja"
title = "My New Hugo Site"
theme = "ananke"
```

> github pagesやnetlifyで使う場合はbaseURLのプロトコルはhttpsにすること

起動確認(http://localhost:1313)

```shell
cp /path/to/someplace/Makefile .
make run
```

Githubレポジトリ作成後

```shell
git remote add origin git@github.com:buta7/buta7.netlify.app.git
git add .
git commit -m 'init'
git push -u origin master
```
### Netlifyの設定

* netlify.tomlの設置
* Site Settings>Build&deploy>Build settings
    * Repository: github.com/buta7/buta7.github.io
    * Build command: hugo --gc -minify

## 使い方

### 投稿

新規投稿

```shell
hugo new posts/2020/05/helloworld.md
content/posts/2020/05/helloworld.md created
```

```shell
SLUG=helloworld DATE=20200505 make post
```

文書作成

```shell
vi content/posts/2020/05/helloworld.md
```


下書きモード解除

```shell
vi content/posts/2020/05/helloworld.md
draft: false
```

## 注意

メディアファイル(css/js)を/から参照するのでnetlifyやgithub pagesのproject向き(github pagesのuserはだめ)

## Link

* [Hugo Theme Dream \| Hugo Themes](https://themes.gohugo.io/hugo-theme-dream/)
