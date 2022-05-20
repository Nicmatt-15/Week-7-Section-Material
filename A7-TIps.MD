# Tips for Assessment 7

## Table of Content

1. [General Tips](#general-tips)
2. [Array Related Tips](#array-related-tips)
3. [Structure and Design](#structure-and-design)
4. [Document and Readability](#document-and-readability)

---

## General Tips

1. Read the files two lines at a time!
2. Remember that the answer is one long word / token. You cannot use a Scanner to read them. Use [String traversals](https://github.com/Nicmatt-15/Week-3-Section-Material/blob/main/String-Traversal.md) instead.
3. Don't forget to declare and use your class constant! (_read the spec_)
4. Don't hardcode `70` in your loop traversal. Use `.length()` instead!

---

## Array Related Tips

1. You should only need 2 arrays <u>**no more and no less**</u> to count the A's and B's answer
2. You should have 1 array to store the percentage of A's and B's. <u>**Reusing your array for a completely different purpose is not a good idea**</u>
3. Do not use arrays to return multiple unrelated things (_ex: an array to return output file and input file_)
4. You can declare all the 3 arrays I mentioned above in the main method to avoid using _return_ (**remember array semantic!**)
5. You can use 2 String arrays or 2 Strings along with a for-loop when determining the personality type to avoid having a lot of redundant conditionals.
6. You should use a loop to calculate the percentage of each dimension

---

## Structure and Design

1. You should only need 4 methods. The breakdown is as follow:
   - Method for program introduction
   - Method for counting A and B
   - Method for counting percentages
   - Method 1 for determining personality
2. You can make two methods (one for input and one for output file prompting), but you can also put these in main.
3. You must have a loop in main that's responsible for reading / going through the file.
4. You can print the output to a separate file in the main method.
5. You should use the formula we talked about in section to reduce the conditional redundancy when calculating the A's and B's.
6. Based on point 5, you should only have two conditional branches when calculating the A's and B's (one for checking A and one for checking B).
7. Based on point 5 in [Array Related Tips](#array-related-tips), you should only have 3 conditional branches to determine the personality type. Refer to the last slide [here](https://docs.google.com/presentation/d/1bYk5Rhh5-DSw4QRV1-daM6Vj2ibYOqAp/edit?usp=sharing&ouid=107575143277342440094&rtpof=true&sd=true).

---

## Document and Readability

1. Header, class, and method comment
2. Proper indentation
3. Parameter comment (if applicable)
4. Return comment (if applicable)
5. Lines < 100 characters
6. Blank line between methods
7. Descriptive and <u>**camelCased**</u> method name
8. Descriptive and <u>**camelCased**</u> variable name
