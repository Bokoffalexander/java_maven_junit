# Мой первый образец сборки java проекта

## Maven + junit (4 теста запускаются)

pom.xml

```xml
<project>
<modelVersion>4.0.0</modelVersion>
<groupId>calculator</groupId>
<artifactId>maven-junit</artifactId>
<version>1.0-SNAPSHOT</version>
<packaging>jar</packaging>

<properties>
    <maven.compiler.source>1.8</maven.compiler.source>
    <maven.compiler.target>1.8</maven.compiler.target>
</properties>


<dependencies>
<dependency>
    <groupId>org.junit.jupiter</groupId>
    <artifactId>junit-jupiter-engine</artifactId>
    <version>5.10.1</version>
    <scope>test</scope>
</dependency>
</dependencies>

<build>
<plugins>
	<plugin>
	<artifactId>maven-surefire-plugin</artifactId>
	<version>3.2.5</version>
	</plugin>
</plugins>
</build>

</project>
```

