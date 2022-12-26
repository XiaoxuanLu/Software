#### static typing

Java is a **statically-typed language**. The types of all variables are known at compile time (before the program runs), and the compiler can therefore deduce the types of all expressions as well.

###### static checking can catach:
-   syntax errors, like extra punctuation or spurious words. Even dynamically-typed languages like Python do this kind of static checking. If you have an indentation error in your Python program, you’ll find out before the program starts running.
-   misspelled names, like `Math.sine(2)`. (The correct spelling is `sin`.)
-   wrong number of arguments, like `Math.sin(30, 20)`.
-   wrong argument types, like `Math.sin("30")`.
-   wrong return types, like `return "30";` from a function that’s declared to return an `int`.
###### dynamic checking can catch:
-   illegal argument values. For example, the integer expression `x/y` is only erroneous when `y` is actually zero; for other values of `y`, its value is well-defined. So in this expression, divide-by-zero is not a static error, but a dynamic error.
-   illegal conversions, i.e., when the specific value can’t be converted to or represented in the target type. For example, `Integer.valueOf("hello")` is a dynamic error, because the string `"hello"` cannot be parsed as a decimal integer. So is `Integer.valueOf("8000000000")`, because 8 billion is outside the legal range of `int` values in Java.
-   out-of-range indices, e.g., using a negative or too-large index on a string.
-   calling a method on a `null` object reference (`null` is like Python’s `None`).
###### immutable
An immutable type is a type whose values can never change once they have been created. The string type is immutable in both Python and Java.
Java also gives us immutable references: variables that are assigned once and never reassigned. To make a reference unreassignable, declare it with the keyword `final`

##### Which of the following ideas discussed in this reading help make your code more **safe from bugs**?
* dynamic checking
* final variables
* static typing