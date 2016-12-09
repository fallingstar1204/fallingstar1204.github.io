## 建立本機儲存庫
開始使用 Git 的初始指令不外乎就是透過 `git init` 或者 `git clone` 本機端的儲存庫. 至於要使用哪個指令則是取決於你的版本控管資料來自於哪邊！

無任何現有儲存庫的情況
```
$ git init
```

已有儲存庫的情況
```
$ git clone [REPO_URI]
```

## 建立分享儲存庫

- 共用儲存庫 (Shared repository/Bare repository)
在當前目錄建立一個<font color='red'>___不包含工作目錄___</font>的儲存庫! 必須特別注意的是這個資料夾不能直接拿來做開發用途，只能用來儲存 Git 的相關資訊，大多數情況下，你都不應該手動編輯這個資料夾的任何檔案，最好透過 git 指令進行操作。
```
$ git init --bare
```

- 遠端儲存庫 (Remote repository)
通常指的是在 Git 平台 (e.g. Github) 建立遠端的儲存庫

其實兩種方式幾乎是一樣的，差別僅在於「共用儲存庫」大多使用直接的檔案存取，而「遠端儲存庫」通常使用 SSH, Git protocol, HTTP 等協定可「遠端」存取 Git 儲存庫，其他的使用方式基本上是一樣的。


$ git remote add <name> <url>

$ git push [-u | --set-upstream]
$ git branch --track branch名稱 遠端branch
$ git branch (--set-upstream-to=<upstream> | -u <upstream>) [<branchname>]

$ git branch --track branch名稱 遠端branch 
建立一個 tracking 遠端 branch 的 branch，這樣以後 push/pull都會直接對應到該遠端的branch。
$ git branch --set-upstream branch名稱 遠端branch 
將一個已存在的 branch 設定成 tracking 遠端的branch。



Compute object ID and optionally creates a blob from a file
```
$ git hash-object 
```
Provide content or type and size information for repository objects
```
$ git cat-file 
```