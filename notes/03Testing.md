## Systematic testing

作为开发者，我们自然希望程序是正常运行的，但是作为测试者，我们希望make it fail。

选择test case时，应该首先将输入空间划分为若干个不相交且并集完整的子区域，从每个子区域中产生一个case作为测试集。比如对于`max(int a, int b)`函数，可以划分为`a < b; a > b; a = b`3个子区域。除了正常的子区域外，还要特别注意子区域的边界。

## Unit test
```java
public class MaxTest {
  ...

  @Test
  public void testALessThanB() {
      assertEquals(2, Math.max(1, 2));
  }

  @Test
  public void testBothEqual() {
      assertEquals(9, Math.max(9, 9));
  }

  @Test
  public void testAGreaterThanB() {
      assertEquals(10, Math.max(10, -9));
  }
}
```
