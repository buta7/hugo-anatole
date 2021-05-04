# README

## セットアップ

サイト作成

```shell
hugo new site hugo-anatole
```

レポジトリ初期化

```shell
cd hugo-anatole
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
git submodule add https://github.com/lxndrblz/anatole.git themes/anatole
```

(参考)submoduleの削除

```shell
git submodule deinit -f themes/anatole
git rm themes/anatole
rm -fr .git/modules/anatole
```

サイト設定

```shell
mv config.toml config.toml.bak
cp -pr themes/anatole/exampleSite/{content,config,static} .
```

## Link

* [Anatole \| Hugo Themes](https://themes.gohugo.io/anatole/)
