## GIT 配置

git config 指令主要用於查看與設定 git 相關參數的設定.

配置參數存放於下列位置, 配置檔案的影響範圍越小, 其設定參數的優先權越高
1. 以___容器___為影響範圍的配置, 檔案位置在 .git/config
2. 以___使用者___為影響範圍的配置, 檔案位置在 ~/.gitconfig
3. 以___系統___為影響範圍的配置, 檔案位置在 /etc/gitconfig

#### 設定
1. 設定___容器等級___的配置時, 使用 \-\-local 參數或者使用預設方式來操作
```
$ git config user.name "Hugh Yang(local)"
$ git config --local user.name "Hugh Yang(local)"
```

2. 設定___使用者等級___的配置, 使用 \-\-global 參數來操作
```
$ git config --global user.name "Hugh Yang(global)"
```

3. 設定___系統等級___的配置, 使用 \-\-system 參數來操作
```
$ git config --system user.name "Hugh Yang(system)"
```

#### 移除
1. 移除___容器等級___的配置時, 使用 \-\-local 參數或者使用預設方式來操作
```
$ git config --unset user.name
$ git config --local --unset username
```

2. 移除___使用者等級___的配置, 使用 \-\-global 參數來操作
```
$ git config --global --unset user.name
```

3. 移除___系統等級___的配置, 使用 \-\-system 參數來操作
```
$ git config --system --unset user.name
```

#### 查看
列出所有的參數. 如果我們在三個層級都有設定相同參數的話, 則三個參數都會被列出而且會依照配置檔影響的範圍(系統 > 使用者 > 容器) 依序列出所有的參數
```
$ git config -l
$ git config user.name
```

#### 建議配置參數
```
$ git config user.name "yyy" // 設定送交檔案的作者名稱
$ git config user.email "xxx@xxx.xx" // 設定送交檔案的作者信箱
$ git config --global core.editor "vim" // 設定預設編輯器為 vim
$ git config --global core.ignorecase true // 設定 git 忽略檔名大小寫
$ git config --global color.ui true
```

