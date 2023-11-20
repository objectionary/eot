EO Optimizations Testing Framework.

In you unit test, use it like this:

```java
import org.eolang.eot.Script;
@Test
void optimizesCorrectly() {
  assertThat(
    new Script(
      "eo source here",
      (xmir) -> optimizeIt(xmir)
    ),
    is(true)
  );
}
```

The `optimizeIt()` method should accept and return `com.jcabi.xml.XML`