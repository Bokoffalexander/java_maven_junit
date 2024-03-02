# Мой первый образец сборки java проекта

## Maven + junit (4 теста запускаются)

```sh
├── pom.xml
├── README.md
├── src
    ├── main
    │   └── java
    │       └── calculator
    │           └── Calculator.java
    └── test
        └── java
            └── calculator
                └── CalculatorTest.java
```

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

Calculator.java

```java
package calculator;
public class Calculator {
	public static void main(String[] args){
		System.out.println("Calculator!");
	}

	public int sum(int a, int b){
		return a+b;
	}

	public int minus(int a, int b){
		return a-b;
	}

	public int multiply(int a, int b){
		return a*b;
	}

	public float division(int a, int b){
		if (b==0) return -1.0f;
		return (1.0f*a)/b;
	}
}
```

