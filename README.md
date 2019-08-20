### hystrix
---
https://github.com/Netflix/Hystrix

```java
public class CommandHelloWorld extends HystixCommand<String> {
  
  private final String name;
  
  public CommandHelloWorld(String name) {
    super(HystrixCommandGroupKey.Factory.asKey("ExampleGroup"));
    this.name = name;
  }
  
  @Override
  protected String run() {
    return "Hello " + name + "!";
  }
}

String s = new CommandHelloWorld("Bob").execute();
Future<String> s = new CommandHelloWorld("Bob").queue();
Observable<String> s = new CommandHelloWorld("Bob").observer();
```

```sh
mvn -f download0hystrix-pom.xml dependency:copy-dependencies
./gradlew build
```

```
```


