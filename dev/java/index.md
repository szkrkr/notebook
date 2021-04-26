

## trouble shooting
* `No serializer found for class com.szkrkr.apidemo.app.models.Member and no properties discovered to create BeanSerializer`
実行時エラー。APIのレスポンス
response を jsonにできない。
lombok の @Data をつける。 C#の `@SerializableObject` のようなイメージ

* `'url' attribute is not specified and no embedded datasource could be configured.`
compile error.
src/main/resources/application.properties に設定
```
spring.jpa.hibernate.ddl-auto=update
spring.datasource.url=jdbc:mysql
spring.datasource.username=root
spring.datasource.password=
```

* `Failed to configure a DataSource: no embedded datasource could be configured.`
上の形間違い。
```
spring.jpa.hibernate.ddl-auto=update
spring.datasource.url=jdbc:mysql://localhost:3306/test
spring.datasource.username=root
spring.datasource.password=
spring.datasource.driverClassName=com.mysql.cj.jdbc.Driver
```

* `Warning:(14, 26) Raw use of parameterized class 'ArrayList'`
コード解析時ワーニング。
ArrayList() -> ArrayList<T>()

* `Warning:(13, 36) Explicit type argument Member can be replaced with <>`
コード解析時ワーニング。
List<Member> items;
items = ArrayList<>();




<!--		<dependency>-->
<!--			<groupId>org.springframework.boot</groupId>-->
<!--			<artifactId>spring-boot-starter-jooq</artifactId>-->
<!--		</dependency>-->














sudo lsof -i:8080
sudo kill 12345
