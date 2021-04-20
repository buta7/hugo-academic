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
cp -pr themes/dream/exampleSite/config .
mv config.toml config.toml.bak
```

## Link

* [HumamAlwassel/hugo\-academic: 📝 The website builder for Hugo\. Build and deploy a beautiful website in minutes\!](https://github.com/HumamAlwassel/hugo-academic)
* [Hugo \+ Academic テーマを使ったブログの作り方 \- Qiita](https://qiita.com/harumaxy/items/58e7e4273c61e7e260b3)
