Stream API 可以声明性地通过 parallel() 与 sequential() 在并行流与顺序流之间进行切换。

####  函数式接口：

1. Predicate<T>，表示一个接受单个输入参数并返回布尔值结果的断言。

   ```
   Predicate<String> isEmpty = String::isEmpty;
   System.out.println(isEmpty.test("")); // 输出 true
   ```

2. Consumer<T>，表示一个接受单个输入参数并且不返回结果的操作。

   ```
   Consumer<String> print = System.out::println;
   print.accept("Hello, Consumer!");
   ```

3. Function<T, R>，表示一个接受一个输入参数并且返回结果的函数。

   ```
   Function<Integer, String> intToString = String::valueOf;
   System.out.println(intToString.apply(123)); // 输出 "123
   ```

4. Supplier<T>，表示一个提供结果的供应商。

   ```
   Supplier<String> supplier = () -> "Hello, Supplier!";
   System.out.println(supplier.get())
   ```

5. BinaryOperator<T>，表示一个作用于两个同类型操作数的操作，并且返回同类型的结果。是一个特殊的`BiFunction<T，T，T>`。

   ```
   BinaryOperator<Integer> sum = Integer::sum;
   System.out.println(sum.apply(2, 3)); // 输出 5
   ```

6. UnaryOperator<T>，表示一个作用于单个操作数的操作，并且返回操作数的类型。是一个特殊的 `Function<T, T>`。

   ```
   UnaryOperator<Integer> square = x -> x * x;
   System.out.println(square.apply(5)); // 输出 25
   ```

7. 自定义函数式接口

   ```
   @FunctionalInterface
   public interface MyFunction {
       int apply(int a, int b);
   }
   ```

   



