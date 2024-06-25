```markdown
# HelloWorld Apache Beam Project

This is a simple Apache Beam project that demonstrates basic usage of Apache Beam with the DirectRunner.

## Prerequisites

- Java 17
- Apache Maven 3.8.5 or later

## Setup

### Clone the Repository

```sh
git clone <repository_url>
cd helloworld
```

### Update Dependencies

Ensure that all dependencies are correctly set up by running:

```sh
mvn clean install
```

### Compile the Project

Compile the project using the following command:

```sh
mvn compile
```

### Run the Main Class

Execute the main class with the DirectRunner:

```sh
mvn exec:java -Dexec.mainClass="com.example.Main" -Dexec.args="--runner=DirectRunner --parallelism=4"
```

## Project Structure

```plaintext
helloworld
│   README.md
│   pom.xml
└───src
    └───main
        └───java
            └───com
                └───example
                        Main.java
```

## Main Class

The main class is located at `src/main/java/com/example/Main.java`. It includes a simple Apache Beam pipeline that logs words and numbers.

## Dependencies

The `pom.xml` includes the following dependencies:
- Apache Beam Core SDK
- Apache Beam Direct Runner
- Apache Beam Model Pipeline
- SLF4J Simple Logger

Ensure that these dependencies are correctly included in your `pom.xml`.

```xml
<dependencies>
    <dependency>
        <groupId>org.apache.beam</groupId>
        <artifactId>beam-sdks-java-core</artifactId>
        <version>2.36.0</version>
    </dependency>
    <dependency>
        <groupId>org.apache.beam</groupId>
        <artifactId>beam-runners-direct-java</artifactId>
        <version>2.36.0</version>
    </dependency>
    <dependency>
        <groupId>org.apache.beam</groupId>
        <artifactId>beam-model-pipeline</artifactId>
        <version>2.36.0</version>
    </dependency>
    <dependency>
        <groupId>org.slf4j</groupId>
        <artifactId>slf4j-simple</artifactId>
        <version>1.7.32</version>
    </dependency>
</dependencies>
```

## Troubleshooting

If you encounter any issues, ensure that you have the correct versions of Java and Maven installed. Check the full stack trace of any errors by re-running Maven with the `-e` switch:

```sh
mvn exec:java -Dexec.mainClass="com.example.Main" -Dexec.args="--runner=DirectRunner --parallelism=4" -e
```

For detailed debug logging, use the `-X` switch:

```sh
mvn exec:java -Dexec.mainClass="com.example.Main" -Dexec.args="--runner=DirectRunner --parallelism=4" -X
```

## License

This project is licensed under the MIT License.
```