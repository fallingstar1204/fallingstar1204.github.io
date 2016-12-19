## GIT DIFF

用來比對兩個版本之間的差異

#### 四種基本的比較方式

1. 比對 ___工作目錄___ 與 ___索引___ 之間的差異
```
$ git diff
```

2. 比對的是 ___工作目錄___ 與 ___指定 commit 物件裡的那個 tree 物件___
```
$ git diff <commit_id>
```

3. 比對 ___當前的索引狀態___ 與 ___指定 commit 物件裡的那個 tree 物件___
```
$ git diff --cached <commit_id>
$ git diff --staged <commit_id>
```

4. 直接比對特定兩個版本
```
$ git diff <commit_id_1> <commit_id_2>
```