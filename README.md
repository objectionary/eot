In you unit test, use it like this (in combination with 
[JUCS](https://github.com/objectionary/jcucs)):

```java
import org.eolang.eot.Script;
import org.eolang.jucs.ClasspathSource;

@Test
@ClasspathSource(value = "", glob = "**.eo")
void optimizesCorrectly(String eo) {
  assertThat(
    new Script(
      eo,
      (xmir) -> optimizeIt(xmir)
    ),
    is(true)
  );
}
```

The `optimizeIt()` method should accept and return `com.jcabi.xml.XML`