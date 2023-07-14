## Mutating values vs. reassigning variables

需要区分引用的可重新赋值和对象的可变性，比如不能重新赋值的引用指向可变对象：
```java
final StringBuilder sb = new StringBuilder("a");
sb.append("b");
```

还可以有可重新赋值的引用指向不可变对象：
```java
String s = "a";
s = "ab";
```

另外，Java中的参数传递是call by value，函数内部参数的变化不会影响caller：
```java
void f(String s, StringBuilder sb) {
  s.concat("b");
  s += "c";
  sb.append("d");  // s refers to "ac", sb refers to "ad"
}

String t = "a";
StringBuilder tb = new StringBuilder(t);
f(t, tb);  // t refers to "a", tb refers to "ad", 
```

## == vs. equals()

`==`用于基本类型时没问题，用于引用时则比较是否指向同一个对象，`equals`用于比较两个对象的值。

## Java Collections

