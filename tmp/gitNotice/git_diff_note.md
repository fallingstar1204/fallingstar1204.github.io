## GIT 差異比較

git diff 指令主要是用來比對兩個版本之間的差異

### 四種基本的比較方式

1. 比對 ___工作目錄___ 與 ___索引___ 之間的差異. 用來列出哪些修改還沒放進索引中
```
$ git diff
```

2. 比對 ___索引___ 與 ___上次 commit 物件___ 之間的差異. 用來列出準備提交的修改
```
$ git diff --cached
$ git diff --staged
```

3. 比對 ___工作目錄___ 與 ___指定 commit 物件___ 之間的差異.
```
$ git diff HEAD
$ git diff <commit>
```

4. 直接比對特定兩個版本
```
$ git diff <commit_1> <commit_2>
```