---
layout: post
title: "Start To Use Octopress"
date: 2016-06-25 00:51:35 +0800
comments: true
categories: Octopress
---
### <span id="steps">安裝步驟</span>
步驟 1. [設定 Ruby 環境](#ruby)  
步驟 2. [設定 Git 環境](#git)  
步驟 3. [設定 Octopress](#octopress)  
步驟 4. [建立 Github repo 及設定 Github pages](#github)  
步驟 5. [開始使用](#using)  

### <span id="ruby">[設定 Ruby 環境](#steps)</span>

##### Windows (Win7)

- [下載][rubyinstaller] 並且安裝 Ruby
- 設定 Ruby classpath  
*如果您在安裝 Ruby 的時候有勾選 __Add Ruby executables to your PATH__ 這個選項的話就可以忽略此步驟

- [下載][rubyinstaller] 並且解壓縮 Ruby Devkit
- 安裝 Ruby Devkit
	請先切換到剛剛解壓縮 Devkit 的路徑後執行下列指令
```
$ ruby dk.rb init  
$ ruby dk.rb install
```

##### Mac OS(10.11.6)

- 安裝 Homebrew
```
$ ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```
- 安裝 [RVM][rvm_website], [Ruby][ruby_website]
```
$ curl -L https://get.rvm.io | bash -s stable --ruby=2.0.0
$ rvm rubygems latest
```

##### Ubuntu (16.04)

- 安裝 [RVM][rvm_website], [Ruby][ruby_website]
```
$ curl -L https://get.rvm.io | bash -s stable --ruby=2.0.0
$ rvm rubygems latest
```

### <span id="git">[設定 Git 環境](#steps)</span>

##### Windows (Win7)
- [下載][msysgit]並安裝 msysgit 
- [下載][tortoisegit]並安裝 TortoiseGit
- 使用 Git bash 設定 Git 參數
```
$ git config --global user.name "<使用者名字>"
$ git config --global user.email "<電子信箱>"
```

##### Mac (10.11.6)
- 安裝 Git
```
$ homebrew install git
$ git --version
```

- 設定 Git 參數
```
$ git config --global user.name "<使用者名字>"
$ git config --global user.email "<電子信箱>"
```

##### Ubuntu (16.04)
- 安裝 Git
```
$ apt-get install git
$ git --version
```

- 設定 Git 參數
```
$ git config --global user.name "<使用者名字>"
$ git config --global user.email "<電子信箱>"
```

### <span id="octopress">[設定 Octopress](#steps)</span>

##### 使用全新的 github pages

- 下載 octopress
```
$ git clone git://github.com/imathis/octopress.git octopress
```

- 安裝 octopress 需要用到的 bundler
```
$ cd octopress
$ gem update --system
$ gem install bundler
$ bundle install
```

- 安裝預設主題
```
$ rake install
```

- 預覽 blog
```
$ rake preview
```

打開瀏覽器輸入 http://localhost:4000 即可瀏覽我們搭建的 blog.

##### 使用現有的 github pages

- 下載現有的 blog
```
$ git clone -b source git@github.com:[your_username]/[your_username].github.io.git octopress
$ cd octopress
$ git clone git@github.com:[your_username]/[your_username].github.io.git _deploy
```

- 安裝 octopress 需要用到的 bundler
```
$ cd octopress
$ gem update --system
$ gem install bundler
$ bundle install
```

- 預覽 blog
```
$ rake preview
```

打開瀏覽器輸入 http://localhost:4000 即可瀏覽我們搭建的 blog.

### <span id="github">[建立 Github repo 及設定 Github pages](#steps)</span>
如果是使用先前已經建立過的 octopress 的話, 可以省略此步驟

- 設定 Github
申請 GitHub 的帳號，並為 blog 建立一個 repo, 其命名規則是 [yourname].github.io
建立成功後會得到一個 SSH 地址

> git@github.com:[your_username]/[your_username].github.io.git


- 設定與 Github pages 的相關設定
```
$ cd octopress
$ rake setup_github_pages
```

- 產生頁面並上傳到 github 
```
$ rake generate
$ rake deploy
```

- 上傳 source code
```
$ git add .
$ git commit -m 'your message'
$ git push origin source
```

### <span id="using">[開始使用](#steps)</span>

- 建立撰寫文章
```
$ rake new_post["Post Title"]
```

- 預覽文章
```
$ rake generate
$ rake preview
```

- 發佈
```
$ rake deploy
```

[rubyinstaller]:http://rubyinstaller.org/downloads/
[msysgit]:https://git-for-windows.github.io/
[tortoisegit]:https://tortoisegit.org/
[rvm_website]:https://rvm.io/
[ruby_website]:https://www.ruby-lang.org/zh_tw/