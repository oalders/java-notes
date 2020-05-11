# Java Notes

Some of my notes for learning Java.

<!-- vim-markdown-toc GFM -->

* [Keywords](#keywords)
  * [abstract](#abstract)
  * [final](#final)
  * [return](#return)
  * [static](#static)
  * [throws](#throws)
  * [void](#void)
* [Types](#types)
* [Testing](#testing)

<!-- vim-markdown-toc -->

## Keywords

### abstract

`abstract` denotes a class which can be inherited but cannot be used to create objects directly.


### final

* When used with a method, `final` means that the method cannot be overridden in any inheriting class.
* When used with a variable, `final` is essentially declaring a constant: `private final String foo;`

### return

`return this;`

Returns the current object.  Useful for method chaining when building objects.

### static

> In general, static means "associated with the type itself, rather than an instance of the type."

[https://stackoverflow.com/a/1415968/406224](https://stackoverflow.com/a/1415968/406224)

A `static` method of a class does not require you to first create an instance of the class before calling it.

### throws

Indicates a class or classes of error which the method may throw. These should be explicitly handled via `try/catch`.

```java
throws IOException, URISyntaxException
```

### void

The method has no return values.

```java
public class MyClass {
  static void someMethod() {
    System.out.println("ok");
  }

  public static void main(String[] args) {
    someMethod();
  }
}
```

## Types

* `int port = 80;`
* `boolean useHttps = true;`
* `String host = "www.metacpan.org";`

Note that a string is both a type and a class.  So the following are equivalent:

```java
String host = "www.metacpan.org";
String host = new String("www.metacpan.org");`
```

To get the length of the string above:

```java
int len = host.length();
```

## Testing

Run tests: `mvn test -B`

Run test class: `mvn  -Dtest=TransactionReportTest test -B`
