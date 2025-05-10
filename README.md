# projeto2_maputo

## Requisitos
- Java 21+
- Maven 3+

## 1. Build do projeto
```sh
$ cd commons-cli-1.9.0-src/
$ mvn clean package
```

## 2. Compila o Driver (Fuzz Target)
```sh
$ javac -cp target/classes/:jazzer_standalone.jar ParserFuzzer.java
```

## 3. Fuzzing: Executa o Jazzer para exercitar o SUT usando o Driver passado como parâmetro
```sh
$ ./jazzer --cp=.:./target/commons-cli-1.9.0.jar  --agent_path=./jazzer_standalone.jar  --target_class=ParserFuzzer
```

