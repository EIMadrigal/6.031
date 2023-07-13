## 类型

Java有一些基本类型`int/long/boolean/double/char`，还有object类型`String/BigInteger`，对数据的操作包括3种形式：operator，对象的成员方法，类的方法。

## 静态类型

不同于Python/JS，Java是一种静态类型语言，变量类型在编译时就被确定，可以在运行前就发现程序中的部分bug。一些动态类型语言也逐渐开始支持静态类型检查，比如Python的type hints。

静态检查通常只能发现类型错误，对于某种类型具体的某个值引起的错误只能通过动态检查发现，如divide by zero, index out of range。

一些比较坑的地方在于，对于原始数据类型，整除截断、溢出、浮点数非法运算（除0、负数求平方根）本应进行动态检查并报错，但实际上会默认产生`NaN`, `POSITIVE_INFINITY`等，如果不进行处理而直接使用，将会导致错误的结果。

## Arrays and collections

Array是固定长度的数组，可以声明并赋值一个`int[]`类型的数组：
```java
int[] a = new int[100];
```

通过`List`可以创建可变长度的数组：
```java
List<Integer> list = new ArrayList<Integer>();
```
`List`接口不能直接创建对象，其只是规定了`List`必须提供的操作，具体的实现包括`ArrayList`和`LinkedList`。另外，`List`无法采用原始数据类型`int`等作为参数，需要使用等价的object类型。

## Methods

Java的每个方法都必须在类中，`static`修饰的方法中，`this`参数会隐式传递，不会显式地出现在参数列表中。

## Mutating values vs. reassigning variables

可以通过`final`使得引用不能被重新赋值（重新指向另一个对象）：
```java
final int n = 5;
```
编译器会对这些`final`变量进行静态检查并及时报错。

## 工程习惯

写代码时需要将相应参数、返回值的假设（约束）明确写在注释里。
