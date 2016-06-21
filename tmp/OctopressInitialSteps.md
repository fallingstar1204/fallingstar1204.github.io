## Octopress 安裝步驟

Octopress 安裝不管是安裝在哪種環境, 基本是不外乎以下幾個步驟

### 設定 Ruby 環境 
1. 下載與安裝 Ruby
	[下載][rubyinstaller]
2. 設定 Ruby 路徑

3. 下載與安裝 Ruby Devkit
	[下載][rubyinstaller]
	
	````
	$ ruby dk.rb init
	$ ruby dk.rb install
	````
4. 更新 RubyGems

	````
	$ gem update --system
	````

### 設定 Git 環境
1. 安裝 Git

	````	
	$ homebrew install git
	$ git --version
	````

### 設定 Octopress

1. 下載 octopress

	````
	$ git clone git://github.com/imathis/octopress.git 	octopress
	````
2. 安裝 octopress 需要用到的 bundler 

	````
	$ cd octopress
	$ gem install bundler
	$ bundle install		
	````

3. 安裝預設主題

	````
	$ rake install
	````
4. 預覽 blog

	````
	$ rake preview
	````
	打開瀏覽器輸入 http://localhost:4000 即可瀏覽我們搭建的 blog.
	

### 設定 Github and Github pages
1. 設定 Github 
	
	申請 GitHub 的帳號，並且為您的 blog 建立一個 repo, 其命名規則是 [yourname].github.io
	建立成功後會得到一個 SSH 地址 ``git@github.com:[your_username]/[your_username].github.io.git``
	
2. 發佈到 Github pages

	````
	$ cd octopress
	$ rake setup_github_pages
	````	


### 開始使用
1. 建立撰寫文章

	````
	$ rake new_post["Post Title"]
	````
2. 預覽文章

	````
	$ rake generate
	$ rake preview
	````
3. 發佈

	````
	$ rake deploy
	````
[rubyinstaller]:http://rubyinstaller.org/downloads/