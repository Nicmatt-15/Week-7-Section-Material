# Basic of Arrays

## Table of Contents

1. [Array Indirect Declaration](#array-indirect-declaration)
2. [Array Direct Declaration](#array-direct-declaration)
3. [Printing an Array](#printing-an-array)
4. [Accessing Array Value](#accessing-array-value)
5. [Assigning and Changing Array Value](#assigning-and-changing-array-value)
6. [Array Traversal](#array-traversal)
7. [Array Semantic](#array-semantic)

---

## Array Indirect Declaration

You can create an array without knowing what value(s) you want to put inside the array. The template is as follow:

```java
type[] yourArrayName = new type[array_length];
```

For example:

```java
String[] bunchaTexts = new String[5];
```

The code above will generate an array with 5 "boxes" that you can start filling in!

> Remember that array indexing are similar to String. The first index / position starts from 0 and the last index is the length of array - 1.
>
> **For example:**
>
> An array with length 5 index starts from 0 and ends at 4.

---

## Array Direct Declaration

You can create an array and assign the value immediately. The template is as follow:

```java
type[] yourArrayName = {item1, item2, item3, item4};
```

For example:

```java
String[] bunchaTexts = {"Never", "Gonna", "Give", "You", "Up"};
```

---

## Printing an Array

You can print your whole array in a nicely formatted way using `Arrays.toString(yourArrayName)`.

For example:

```java
String[] bunchaTexts = {"Never", "Gonna", "Give", "You", "Up"};

String printedArray = Arrays.toString(bunchaTexts);
System.out.println(printedArray);
```

Output:

```
["Never", "Gonna", "Give", "You", "Up"]
```

---

## Accessing Array Value

You can access the value of an index / position in your array using `yourArrayName[index]`.

For example:

```java
String[] bunchaTexts = {"Never", "Gonna", "Give", "You", "Up"};

String firstWord = bunchaTexts[0];
String lastWord = bunhcaTexts[4];

```

Output:

```
Never
Up
```

---

## Assigning and Changing Array Value

You can assign or change the value of an index / position in your array using `yourArrayName[index] = new_value`.

For example:

```java
String[] bunchaTexts = {"Never", "Gonna", "Give", "You", "Up"};

bunchaTexts[2] = "Let"
bunchaTexts[4] = "Down"

String printedArray = Arrays.toString(bunchaTexts);
System.out.println(printedArray);
```

Output:

```
["Never", "Gonna", "Let", "You", "Down"]
```

---

## Array Traversal

You can loop through an array to print access and/or change all of it's value.

For example:

```java
String[] bunchaTexts = {"Never", "Gonna", "Give", "You", "Up"};

for (int index = 0; index < bunchaTexts.length; index++) {
    String currentText = bunchaTexts[index];

    System.out.println(currentText);
}
```

Output:

```
Never
Gonna
Give
You
Up
```

---

## Array Semantic

Remember that a few weeks ago, we learned that parameters sends <u>**a copy of your variable's value**</u>. However, this only applies to variable types like `String`, `int`, `double`, `boolean`, and `char`.

When you send an array through a parameter, you actually send <u>**the real array**</u>. Any changes made to the array from any parts of your code will change the real array itself.

Example:

```java
public static void main(String[] args) {
    int[] bunchaNumbers = { 1, 2, 3, 4 };
    changeNumber(bunchaNumbers);
    System.out.println(Arrays.toString(bunchaNumbers));
}

public static void changeNumber(int[] bunchaNumbers) {
    bunchaNumbers[0] = 99;
    bunchaNumbers[1] = 4139;
    bunchaNumbers[2] = 39;
    bunchaNumbers[3] = 4783;
}
```

Output:

```
[99, 4139, 39, 4783]
```

> Notice how the array's value is changed **not** in main. However, when we print the array back in main, we print out the **changed value** and **<u>not</u> the original array's value**.
