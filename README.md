# README

## セットアップ

サイト作成

```shell
hugo new site hugo-airspace
```

レポジトリ初期化

```shell
cd hugo-airspace
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
git submodule add https://github.com/themefisher/airspace-hugo.git themes/airspace
```

(参考)submoduleの削除

```shell
git submodule deinit -f themes/airspace
git rm themes/airspace
rm -fr .git/modules
```

サイト設定

```shell
cp -pr themes/dream/exampleSite/config .
mv config.toml config.toml.bak
```

## Link

* [Airspace Hugo \| Hugo Themes](https://themes.gohugo.io/airspace-hugo/) 
