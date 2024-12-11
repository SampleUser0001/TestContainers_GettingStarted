# TestContainers_GettingStarted

TestContainersを使ってみる

## 概要

この辺が本体。  
mainディレクトリ配下は至って普通。（通常のclientからの接続実装。）

``` java
  static PostgreSQLContainer<?> postgres = new PostgreSQLContainer<>(
    "postgres:16-alpine"
  );
// 中略
  @BeforeAll
  static void beforeAll() {
    postgres.start();
  }

  @AfterAll
  static void afterAll() {
    postgres.stop();
  }

```

## 実行

``` bash
mvn clean compile test
```

## 参考

[Getting started with Testcontainers for Java : TestContainers](https://testcontainers.com/guides/getting-started-with-testcontainers-for-java/)