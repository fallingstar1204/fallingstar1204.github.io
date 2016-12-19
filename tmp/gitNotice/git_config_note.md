### GIT CONFIG

用於查看與設定 git repository 相關參數.

#### 設定
Git 將配置參數存放於下列位置, 越前面的檔案有越高的優先權
1. 以___容器___為影響範圍的配置, 檔案位置在 .git/config, 使用 --local 參數或者使用預設方式來操作
```
$ git config user.name "Hugh Yang(local)" // 新增
$ git config --local user.name "Hugh Yang(local)" // 新增
$ git config --unset user.name // 移除
$ git config --local --unset username // 移除
```

2. 以___使用者___為影響範圍的配置, 檔案位置在 ~/.gitconfig, 使用 --global 參數來操作
```
$ git config --global user.name "Hugh Yang(global)" // 新增
$ git config --global --unset user.name // 移除
```

3. 以___系統___為影響範圍的配置, 檔案位置在 /etc/gitconfig, 使用 --system 參數來操作
```
$ git config --system user.name "Hugh Yang(system)" // 新增
$ git config --system --unset user.name // 移除
```

#### 查看
Git 會依照配置檔影響的範圍(系統 > 使用者 > 容器)依序列出所有的參數
```
$ git config -l
```

#### 建議配置參數
```
$ git config --global user.name "yyy" // 設定送交檔案的作者名稱
$ git config --global user.email "xxx@xxx.xx" // 設定送交檔案的作者信箱
$ git config --global core.editor "vim" // 設定預設編輯器為 vim
$ git config --global core.ignorecase true // 設定 git 忽略檔名大小寫
```

