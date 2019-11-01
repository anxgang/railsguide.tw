# Ruby On Rails 中文指南

## 首次執行

```sh
$ cd ../rails/guides
# 1. 安裝 gem
$ bundle install
# 2. 複製 source 到 source/zh-TW
$ mkdir zh-TW
$ cp -r source/. zh-TW
$ mv zh-TW source/zh-TW
```

## 編輯產生 html

```sh
# 執行產生 html 指令
$ cd ../rails/guides
$ rake guides:generate:html GUIDES_LANGUAGE=zh-TW RAILS_VERSION=v6.0.0
```

## Deploy

```
$ rm -rf v6.0.0
$ cp -r ../rails/guides/output/zh-TW/. v6.0.0
$ git add .
$ git commit -m "deploy"
$ git push -f origin master:gh-pages
```