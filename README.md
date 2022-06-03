# The while Statement

## Learning Goals

- Use while statements

## The while Statement in Java

With the `if` statement, we saw that we can make the execution of a block of
code conditional based on the outcome of a conditional statement. In that
scenario, the conditional block of code gets executed exactly once. What if we
wanted to execute the same block of code multiple times, as long as a condition
stays true?

```java
while(true) {
    System.out.println("I'm a loop that never ends, aka an infinite loop");
}
```

In the code above, the statement
`System.out.println("I'm a loop that never ends, aka an infinite loop");` will
run as long as the condition specified in the `while` statement evaluates to
`true`. Since that condition is literally the `boolean` value `true`, the
condition will always be `true` and the loop will never stop executing. This is
an infinite loop, and although useful in some specific cases, it generally leads
to bugs.

Let's consider code where the content of the `while` loop actually changes the
condition:

```java
// simulate the passing of time
int startingYear = 2000;
int targetYear = 2011;
int currentYear = startingYear;
while (currentYear < targetYear) {
    System.out.println((currentYear - startingYear) + " year(s) have passed");
    // conditional logic based on the current year
    currentYear++;
}
```

In this code, you can see that the condition is now an actual expression:
`currentYear < targetYear`. Furthermore, since we change the value of the
variable inside the `while` loop, the value of the condition will change with
every iteration through the loop, which means that it's possible, although not
guaranteed, that the condition will eventually become `false` and the loop will
stop executing.
