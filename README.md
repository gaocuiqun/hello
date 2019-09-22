# hello
你好，世界Java Spring Boot项目。

## 先决条件

1. 安装[Java 8 SDK(jdk1.8)](http://oracle.com/javase)；
2. 安装[Maven](https://maven.apache.org)；
3. 安装[Git客户端](https://git-scm.com/download)； 
4. 安装[Idea](https://www.jetbrains.com/idea/download)；
5. 安装[MySQL服务器社区版](https://dev.mysql.com/downloads/mysql/)；
6. 安装[MySQL Workbench](https://dev.mysql.com/downloads/workbench/)；
7. 安装[Apache Tomcat 9](https://tomcat.apache.org)；
8. 安装[Google Protobuf 3.6.0](https://github.com/protocolbuffers/protobuf/releases)。
9. 安装[Sbt](https://www.scala-sbt.org/download.html)；
10. 注册[Github](https://github.com)帐户。

## 构建代码生成成器

### clone本仓库

```
git clone https://github.com/gaocuiqun/hello.git
```

### 构建代码生成成器

```
cd hello
mvn package
```

### 使用代码生成器生成样例项目

假设要将生成的项目放到当前目录，在Linux或macOS环境，取得当前路径可以用`$(pwd)`，在Windows上可以用想要的路径替代。

```
java -Doutput.dir=$(pwd) -Dsymbol.naming=unix_c -jar target/hello.jar generate-all sample-model.xml
```

### 构建使用代码生成器生的成样例项目

```
cd $(pwd)/my-sample
mvn package
```
### 创建数据库及表

数据库建表语句在`$(pwd)/my-sample/my-sample-dao/src/main/resources/`，MySQL建表语句脚本是`$(pwd)/my-sample/my-sample-dao/src/main/resources/sampledb-db-mysql-schema.ddl`

```
mysql -u root -p < $(pwd)/my-sample/my-sample-dao/src/main/resources/sampledb-db-mysql-schema.ddl
```

### 运行使用代码生成器生的成样例项目

```
java -jar my-sample-app/target/my-sample-app-1.0-SNAPSHOT.war
```


## 创建Github仓库


## clone 仓库
## 
2. 编译、打包项目。

```
cd hello
mvn package
```

3. 运行。

```
java -jar hello-app/target/hello-1.0-SNAPSHOT.jar
```
