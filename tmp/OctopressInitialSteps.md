# Octopress 安裝步驟

## 設定 Ruby 環境 
---
### For Windows

- [下載][rubyinstaller] 並且安裝 Ruby

- 設定 Ruby classpath
	 
- [下載][rubyinstaller] 並且解壓縮 Ruby Devkit

- 安裝 Ruby Devkit
		
	````
	$ cd ${devkit unzip folder path}
	$ ruby dk.rb init
	$ ruby dk.rb install
	````
- 更新 RubyGems

	````
	$ gem update --system
	````

### For Mac

- 安裝 Homebrew

	````
	$ ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
	````
- 安裝 [RVM][rvm_website], [Ruby][ruby_website]
 	
	````
	$ curl -L https://get.rvm.io | bash -s stable --ruby=2.0.0
	$ rvm rubygems latest
	````
- 更新 RubyGems

	````	
	$ gem update --system
	````

## 設定 Git 環境
---
### For Windows
- [下載][msysgit]並安裝 msysgit 

- [下載][tortoisegit]並安裝 TortoiseGit

- 使用 Git bash 設定 Git 參數

	````
	$ git config --global user.name "<使用者名字>"
	$ git config --global user.email "<電子信箱>"
	````

### For Mac 
- 安裝 Git  
	
	````	
	$ homebrew install git
	$ git --version
	````
- 設定 Git 參數

	````
	$ git config --global user.name "<使用者名字>"
	$ git config --global user.email "<電子信箱>"
	````
	
## 設定 Octopress
---
- 下載 octopress

	````
	$ git clone git://github.com/imathis/octopress.git 	octopress
	````
- 安裝 octopress 需要用到的 bundler 

	````
	$ cd octopress
	$ gem install bundler
	$ bundle install		
	````

- 安裝預設主題

	````
	$ rake install
	````
- 預覽 blog

	````
	$ rake preview
	````
	打開瀏覽器輸入 http://localhost:4000 即可瀏覽我們搭建的 blog.
	

## 設定 Github and Github pages
---
- 設定 Github 
	
	申請 GitHub 的帳號，並且為您的 blog 建立一個 repo, 其命名規則是 [yourname].github.io
	建立成功後會得到一個 SSH 地址  
	``git@github.com:[your_username]/[your_username].github.io.git``
	
- 發佈到 Github pages

	````
	$ cd octopress
	$ rake setup_github_pages
	````	


## 開始使用
---
- 建立撰寫文章

	````
	$ rake new_post["Post Title"]
	````
- 預覽文章

	````
	$ rake generate
	$ rake preview
	````
- 發佈

	````
	$ rake deploy		
	````

[rubyinstaller]:http://rubyinstaller.org/downloads/
[msysgit]:https://git-for-windows.github.io/
[tortoisegit]:https://tortoisegit.org/
[rvm_website]:https://rvm.io/
[ruby_website]:https://www.ruby-lang.org/zh_tw/