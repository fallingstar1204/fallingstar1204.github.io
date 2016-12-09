---
layout: post
title: "Homebrew installation"
date: 2016-06-26 11:22:06 +0800
comments: true
categories: Homebrew Mac
---

## Homebrew 簡介 
- Mac上的套件管理工具
- 使用 Ruby 語言開發
- 通常都是用來安裝一些系統指令，大部份是UNIX系統下的一些好用套件
- [官方網站][homebrewWebsite]

### 安裝要求
- 安裝 Xcode

```		
$ xcode-select --install	
$ xcode-select -p
```
		
- 安裝 Ruby 開發工具 (Optional)

因為 Mac 系統本身就已經內建安裝 Ruby 了, 這個步驟顯得有點多餘, 但是如果有 Ruby 版本切換的需求的話, 還是可以選擇透過 RVM 來管理 Ruby

```
$ curl -L https://get.rvm.io | bash -s stable --ruby
$ rvm rubygems latest
```

### 安裝指令
```
$ ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

### 常用指令

| 說明 				| 指令 						|
| :--		| :--						|
| 更新套件清單		| brew update 				|
| 搜尋套件    		| brew search (套件名稱)   	|
| 安裝套件     		| brew install (套件名稱)   	|
| 移除套件			| brew uninstall (套件名稱)	|
| 查詢套件資訊		| brew info (套件名稱) 		|
| 已安裝套件清單		| brew list 				|
| 查看需要更新的套件 	| brew outdated 			|
| 更新套件			| brew upgrade (套件名稱) 	|
| 檢查設定			| brew doctor 				|


## Homebrew Cask 簡介 
- Homebrew 的擴充套件, 也有人稱為 caskroom
- 通常用來安裝 GUI 的 App

### 安裝要求
- 需已經安裝 Homebrew

### 設定
 預設的cask安裝App會出現捷徑在個人目錄的Application目錄下，
如果你習慣用Launcher的話其實是沒有差的，但a如果你習慣用「應用程式」目錄的話，
可參考[官方說明][caskWebsite] 在 .bash_profile裡面加上
export HOMEBREW_CASK_OPTS="--appdir=/Applications"	

### 安裝指令
```
$ brew install caskroom/cask/brew-cask
```

## 詳細安裝步驟

```
# install xcode
$ xcode-select install
	
# check whether or nor xcode has already installed.
$ xcode-select -p

# install rvm and ruby 
$ curl -L https://get.rvm.io | bash -s stable --ruby
	
# install homebrew
$ ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
	
# check homebrew
$ brew docter

# update homebrew library
$ brew update
	
# install cask
$ brew install caskroom/cask/brew-cask

# check homebrew cask
$ brew cask docter
	
# update cask library
$ brew cask update

# setup install path for cask
$ echo export HOMEBREW_CASK_OPTS="--appdir=/Applications" >> ~/.bash_profile
$ source ~/.bash_profile

# install software
$ brew install git
$ brwe install wget
$ brew cask install alfred
$ brew cask install google-chrome
$ brew cask install skype
$ brew cask install vlc
$ brew cask install haroopad
$ brew cask install dropbox
$ brew cask install sourcetree
$ brew cask install caskroom-versions/sublime-text3
$ brew cask install evernote
$ brew cask install virtualbox
$ brew cask install r-name
$ brew cask install jing
$ brew cask install appcleaner
$ brew cask install teamviewer
$ brew cask install xmind
$ brew cask install staruml
$ brew cask install balsamiq-mockups
$ brew cask install mounty
$ brew cask install intellij-idea-ce
$ brew cask install java6
$ brew cask install java7
$ brew cask install java
$ brew install zsh zsh-completions

# install oh my zsh
$ sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

[homebrewWebsite]: http://brew.sh/index_zh-tw.html
[caskWebsite]: https://github.com/caskroom/homebrew-cask/blob/master/USAGE.md