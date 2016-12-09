## 簡介
Log4j 是一套開放源碼的工具, 方便編程人員在程式中加入 log 機制, 並輸出到各種目標上.
Log4j 能夠透過外部的設定檔(properites 或 XML)進行設定. Log4j 能夠將 log message 寫到 console, 檔案, 串流, TCP 協定的伺服器, Unix Syslog daemon 等.
在感受到 SLF4J/Logback 帶來的威脅後, 終於推出了 Log4j 2.
Log4j 2 改善了許多 Log4j 的功能並增進其效能, 同時還修復了許多存在於Log4j, Logback 結構中固有的問題. 詳細的說明可以參考[官網][log4j]

## 安裝
從 Log4j 2 開始將原本的 jar 檔拆分為定義 interface 的 API 以及提供實作的 Core. 下面是 maven 的設定參數

__Log4j__
```
<dependencies>
    <dependency>
        <groupId>log4j</groupId>
        <artifactId>log4j</artifactId>
        <version>1.2.17</version>
    </dependency>
</dependencies>
```

__Log4j2__
```
<dependencies>
	<dependency>
    	<groupId>org.apache.logging.log4j</groupId>
    	<artifactId>log4j-api</artifactId>
        <version>2.6.2</version>
    </dependency>
    <dependency>
        <groupId>org.apache.logging.log4j</groupId>
        <artifactId>log4j-core</artifactId>
        <version>2.6.2</version>
    </dependency>
</dependencies>
```

## 主要元件

- Logger

- Appenders

- Layout

## 設定

## 範例
[log4j]:http://logging.apache.org/log4j/