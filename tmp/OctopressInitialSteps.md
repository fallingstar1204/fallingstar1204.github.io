## Octopress 安裝步驟

Octopress 安裝不管是安裝在哪種環境, 基本是不外乎以下幾個步驟

1. 設定 Ruby 環境 
- 下載與安裝 Ruby
	[下載][rubyinstaller]
- 設定 Ruby 路徑

- 下載與安裝 Ruby Devkit
	[下載][rubyinstaller]

	$ ruby dk.rb init

	$ruby dk.rb install

- 更新gem

	$ gem update --system

2. 設定 Git 環境

	$ homebrew install git

3. 設定 Github 
	申請 GitHub 的帳號，並且為您的 blog 建立一個 repo, 其命名規則是 [yourname].github.io

4. 設定 Octopress

	git clone git://github.com/imathis/octopress.git octopress
	cd octopress
	gem install bundler
	bundle install
	rake install
	rake setup_github_pages

5. 編輯 _config.yml (Optional)

6. 建立撰寫文章
	$ rake new_post["Post Title"]

7. 預覽文章
	$ rake generate
	$ rake preview
	
8. 發佈	
	$ rake deploy

[rubyinstaller]:http://rubyinstaller.org/downloads/