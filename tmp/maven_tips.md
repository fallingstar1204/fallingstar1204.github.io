#### How to install jar file to local repository
```
mvn install:install-file -Dfile=jar包的位置 -DgroupId=上面的groupId -DartifactId=上面的artifactId -Dversion=上面的version -Dpackaging=jar
```

e.g. mvn install:install-file -Dfile=D:\mvn\spring-context-support-3.1.0.RELEASE.jar -DgroupId=org.springframework -DartifactId=spring-context-support -Dversion=3.1.0.RELEASE -Dpackaging=jar

#### How can we automatically update the version of all child modules, plus the parent?
```
mvn versions:set -DnewVersion=your_new_version

then
mvn versions:commit
or
mvn versions:revert
```
當你在 parent POM 的目錄中使用 mvn versions:set 指令後, 會發現 Parent POM 跟 Child POM 的版本都更改了, 同時也會發現多了一堆 backup 的 POM files. 確認無誤後可以再下 mvn versions:commit 指令刪除 backup 的 POM files. 如果反悔的話可以用 mvn versions:revert 回到原本的狀態

You can refer to http://www.mojohaus.org/versions-maven-plugin