# Lab-7_202001464
# IT314 - Software Engineering

Name : Smit P. Bhavsar

Student Id : 202001464

Lab : 7

## Section A

- Consider a program for determining the previous date. Its input is triple of day, month and year with the following ranges 1 <= month <= 12, 1 <= day<= 31, 1900 <= year <= 2015.The possible output dates would be previous date or invalid date. Design the equivalence class test cases?
1. Equi. Class - 1: Valid dates (1, 1, 1900) to (31, 12, 2015) such that day, month and year are in the given ranges. ex: (15, 10, 2022), (1, 1, 2015),(31, 3, 2000) etc.
2. Equi. Class - 2: Invalid dates (1, 1, 1900) to (31, 12, 2015) such that day,month and year are in the given ranges but the input is invalid. ex: (29, 2,2001), (31, 4, 2010), (30, 2, 2000) etc.
3.  Equi. Class - 3: Invalid range (1, 1, 1900) to (31, 12, 2015) such that day, month and year are not in the given ranges. ex: (32, 2, 2022), (13,14,2003),(11,11,2020) etc.
4. Equi. Class - 4: Invalid input (1, 1, 1900) to (31, 12, 2015) such that day, month and year are in the given ranges but the input is invalid. ex: (2.2, 2,2022), (a, 4, 2010), (30, 2, 2000) etc.
- Tester Action and Input Data Expected Outcome:

**Valid dates:**

| Test Case 1:  | input: (10,10,2010) |
| --- | --- |
|  | output: (9,10,2010) |
| Test Case 2:  | input: (1,1,1900) |
|  | output: (31,12,1899) |

**Invalid dates:**

| Test Case 1: | input: (10,10,2010)|
| --- | --- |
|  | output: (9,10,2010) |
| Test Case 2:  | input: (1,1,1900)|
|  | output: (31,12,1899) |

**Out Of Range:**

| Test Case 1: | input: (32,2,2022)|
| --- | --- |
|  | output: Invalid date date |
| Test Case 3: | input: (11,11,2020)|
|  | output: Invalid date |
| Test Case 2: | input: (13,14,2003)|
|  | output: Invalid date |

**Boundary Value Analysis:**

| Test Case 1: | input: (1,1,1900) Valid First possible date output: (31,12,1899) not in range |
| --- | --- |
| Test Case 2: | input: (31,12,2015) Valid Last possible date , output: (30,12,2015) |
| Test Case 3: | input: (31,1,1899) one day before first possible date , output: Invalid input |
| Test Case 4: | input: (1,1,2016) one day after last possible date , output: Invalid input |
| Test Case 5: | input: (29,2,2000) Valid leap year date , output: (28,2,2000) |
| Test Case 6: | input: (29,2,1900) Invalid leap year date , output: Invalid input |
| Test Case 7: | input: (1,3,2000) valid date after leap year date , output: (29,2,2000) |
| Test Case 8: | input: (1,3,2019) valid date after non leap year date , output: (28,2,2019) |
| Test Case 9: | input: (1,3,2000) valid first day of month , output: (31,12,1999) |
| Test Case 10: | input: (1,1,2000) valid first day of year , output: (31,12,1999) |
- Based on these boundary test cases, we can design the following test cases:
Tester Action and Input Data Expected Outcome.

**Equivalence Class Testing**

| Tester Action and Input Data | Expected Outcome |
| --- | --- |
| Valid partition |  |
| (1,1,1900) | (31,12,1899) |
| (31,12,2015) | (30,12,2015) |
| Invalid partition |  |
| (32,2,2022)  | Invalid date |
| (13,14,2003)  | Invalid date |
| (11,11,2020) | Invalid date |
| (29,2,2001) | Invalid date |
| (31,4,2010) | Invalid date |
| (2.2, 2, 2022)  | Invalid date |
|  (30, 2, 2000) | Invalid date |
| (a, 4, 2010) | Invalid date |
| (31,1,1899) | Invalid date |

**Boundary Value Analysis:**

| Tester Action and Input Data | Expected Outcome |
| --- | --- |
| (1,1,1900)  | (31,12,1899) |
| (1,1,2000) | (31,12,1999) |
| (1,3,2000)  | (31,12,1999) |
| (1,3,2019)  | (28,2,2019) |
| (1,3,2000)  | (29,2,2000) |
| (29,2,1900)  | Invalid input |
| (29,2,2000)  | (28,2,2000) |
| (1,1,2016)  | Invalid input |
| (31,1,1899)  | Invalid input |
| (31,12,2015) | (30,12,2015) |
- Write a set of test cases (i.e., test suite) – specific set of data – to properly test the programs. Your test suite should include both correct and incorrect inputs.
1. Enlist which set of test cases have been identified using Equivalence Partitioning and Boundary Value Analysis separately.
2. Modify your programs such that it runs on eclipse IDE, and then execute your test suites on the program. While executing your input data in a program, check whether the identified expected outcome (mentioned by you) is correct or not.

### Programs:

1. Program 1:
- equivalence Partitioning and Boundary Value Analysis

| Tester Action and Input Data | Expected Outcome |
| --- | --- |
| Equivalence Partitioning |  |
| a = [1, 2, 3, 4], v = 2 | 1 |
| a = [5, 6, 7, 8], v = 10 | -1 |
| a = [1, 1, 2, 3], v = 1 | 0 |
| a = null, v = 5 | An error message |
| Boundary Value Analysis |  |
| Minimum array length: a = [], v = 7 | -1 |
| Maximum array length: a = [1, 2, 3, 4, 5, 6, 7, 8,9, 10, 11, 12,13, 14, 15, 16, 17, 18, 19, 20], v = 3. | 2 |
| Minimum value of v: a = [5, 6, 7], v = 5 | 0 |
| Maximum value of v: a = [1, 2, 3], v = 3 | 2 |
1. Program 2:
- Maximum value of v: a = [1, 2, 3], v = 3

| Tester Action and Input Data | Expected Outcome |
| --- | --- |
| Equivalence Partitioning |  |
| Invalid input: v is not an integer | An error message |
| Empty array: a = [] | 0 |
| Single item array: a = [v], v = a[0] | 1 |
| Multiple item array with v appearing: |  |
| v appears once | 1 |
| v appears multiple times | count>1 |
| Multiple item array with v not appearing | 0 |
| Boundary Value Analysis |  |
| Minimum input values: v = a[0] = 1 | count>0 |
| Maximum input values: v = a[9999] = 10000 | count>0 |
| One occurrence of v: a = [1, 2, 3, …, 9999, v-1, 10000] | 1 |
| All occurrences of v: a = [v, v, v, …, v, v] | 1000 |
| No occurrences of v: a = [1, 2, 3, ... , 9999] | 0 |
1. Program 3
- Equivalence Partitioning:
- Test Cases for Correct Inputs:
    
    
    | Tester Action and Input Data | Expected Outcome |
    | --- | --- |
    | v = 5, a = [1, 3, 5, 7, 9] | 2 |
    | v = 1, a = [1, 3, 5, 7, 9] | 0 |
    | v = 9, a = [1, 3, 5, 7, 9] | 4 |
- Test Cases for Incorrect Inputs:
    
    
    | Tester Action and Input Data | Expected Outcome |
    | --- | --- |
    | v = 2, a = [1, 3, 5, 7, 9] | -1 |
    | v = 10, a = [1, 3, 5, 7, 9] | -1 |
    | v = 6, a = [] | -1 |
- Boundary Value Analysis:
- Test Cases for Correct Inputs:
    
    
    | Tester Action and Input Data | Expected Outcome |
    | --- | --- |
    | v = 5, a = [5, 6, 7] | 0 |
    | v = 6, a = [5, 6, 7] | 1 |
    | v = 7, a = [5, 6, 7] | 2 |
    | v = 5, a = [1, 5, 6, 7, 9] | 1 |
    | v = 6, a = [1, 5, 6, 7, 9] | 2 |
    | v = 7, a = [1, 5, 6, 7, 9] | 3 |
    | v = 9, a = [1, 5, 6, 7, 9] | 4 |
    | v = 1, a = [1] | 0 |
    | v = 5, a = [5] | 0 |
    | v = 1, a = [] | -1 |
- Test Cases for Incorrect Inputs:
    
    
    | Tester Action and Input Data | Expected Outcome |
    | --- | --- |
    | v = 2, a = [1, 3, 5, 7, 9] | -1 |
    | v = 10,a = [1, 3, 5, 7, 9] | -1 |
    | v = 6, a = [1, 3, 5, 7, 9] | -1 |
    | v = 1, a = [2, 3, 4, 5, 6] | -1 |
    | v = 7, a = [2, 3, 4, 5, 6] | -1 |
    | v = 4, a = [5, 6, 7, 8, 9] | -1 |
1. Program 4
- Equivalence Partitioning and Boundary Value Analysis

| Tester Action and Input Data | Expected Outcome |
| --- | --- |
| Equivalence Partitioning: |  |
| a=b=c, where a, b, c are positive integers | EQUILATERAL |
| a=b<c, where a, b, and c are positive integers | ISOSCELES |
| a=b=c=0 | INVALID |
| a<b+c , b<a+c , c<a+b , where a, b, c are positive integers  | SCALENE |
| a=b>0, c=0  | INVALID |
| a>b+c | INVALID |
| Boundary Value Analysis: |  |
| a=1, b=1, c=1  | EQUILATERAL |
| a=1, b=2, c=2  | ISOSCELES |
| a=0, b=0, c=0  | INVALID |
| a=2147483647, b=2147483647, c=2147483647 | EQUILATERAL |
| a=2147483646, b=2147483647, c=2147483647  | ISOSCELES |
| a=1, b=1, c=2^31-1  | SCALENE |
| a=0, b=1, c=1 | INVALID |

  5.Program 5

- Equivalence Partitioning and Boundary Value Analysis
    
    
    | Tester Action and Input Data | Expected Outcome |
    | --- | --- |
    | Equivalence Partitioning: |  |
    | s1 is empty, s2 is non-empty string  | true |
    | s1 is non-empty string, s2 is empty | false |
    | s1 is a prefix of s2  | true |
    | s1 is not a prefix of s2 | false |
    | s1 has same characters as s2, but not a prefix  | false |
    | Boundary Value Analysis: |  |
    | s1 = "a", s2 = "ab" | false |
    | s1 = "ab", s2 = "a" s1 = "a", s2 = "a"  | true |
    | s1 = "a", s2 = "A” | false |
    | s1 = "abcdefghijklmnopqrstuvwxyz", s2 ="abcdefghijklmnopqrstuvwxyz” | true |
    | s1 = "abcdefghijklmnopqrstuvwxyz", s2 = "abcdefghijklmno” | true |
    | s1 = "", s2 = "” | true |
- Modify your programs such that it runs on eclipse IDE, and then execute your test suites on the program. While executing your input data in a program, check whether the identified expected outcome(mentioned by you) is correct or not.
- I have taken 20 test cases (4 test cases per program). Where eight are
wrong or invalid, and the other 12 are correct.
- There are screenshots of code snippets with coverage of the code.
    
    ![Untitled (1)](https://user-images.githubusercontent.com/107932317/232736511-e8a34901-36a1-4e94-9b88-56ac55f0d02d.png)
    
    ![Untitled (2)](https://user-images.githubusercontent.com/107932317/232736599-c6950d38-2f43-4472-a268-4c50e783fa3b.png)
    
- Modified Java codes of given programs (P1 – P5)
    
    ![image](https://user-images.githubusercontent.com/107932317/232736837-d1bcd7f0-b5bb-4093-95ae-5ffcdc6be1c0.png)
    
    ![image](https://user-images.githubusercontent.com/107932317/232736947-d0a325ef-d014-4319-946d-96cf6aa97c16.png)
    
    ![image](https://user-images.githubusercontent.com/107932317/232737045-59738feb-5127-45fe-9edb-7bd113785683.png)
    
- **Testing code with converge:**
    
    ![image](https://user-images.githubusercontent.com/107932317/232737135-275822e3-5cb8-48d9-a635-f3d59a84d8af.png)
    
    ![image](https://user-images.githubusercontent.com/107932317/232737185-3cbf0246-67aa-495a-9fdc-3deb17bec229.png)
    
    ![image](https://user-images.githubusercontent.com/107932317/232737265-40a94086-db95-4d61-bbcc-96a8f35d1051.png)
    
    ![image](https://user-images.githubusercontent.com/107932317/232737362-89483b21-8546-4943-a1ed-ce4acf41b3f5.png)
    
- P6: Consider again the triangle classification program (P4) with a slightly different specification: The program reads floating values from the standard input. The three values A, B, and C are interpreted as representing the lengths of the sides of a triangle. The program then prints a message to the standard output that states whether the triangle, if it can be formed, is scalene, isosceles, equilateral, or right angled. Determine the following for the above program:
    1. Equivalence classes for the system are:
    Class 1: Invalid inputs (negative or zero values)
    Class 2: Non-triangle (sum of the two shorter sides is not greater than the
    longest side)
    Class 3: Scalene triangle (no sides are equal)
    Class 4: Isosceles triangle (two sides are equal)
    Class 5: Equilateral triangle (all sides are equal)
    Class 6: Right-angled triangle (satisfies the Pythagorean theorem
    2. Test cases to cover the identified equivalence classes:
    Class 1: -1, 0
    Class 2: 1, 2, 5
    Class 3: 3, 4, 5
    Class 4: 5, 5, 7
    Class 5: 6, 6, 6
    Class 6: 3, 4, 5
    Test case 1 covers class 1, test case 2 covers class 2, test case 3 covers class 3,test case 4 covers class 4, test case 5 covers class 5, and test case 6 covers class 6.
    3. Test cases to verify the boundary condition A + B > C for the scalene
    triangle:
    (1) 2, 3, 6
    (2) 3, 4, 8
    Both test cases have two sides shorter than the third side and should not form a
    triangle.
    4. Test cases to verify the boundary condition A = C for the isosceles
    triangle:
    (1) 2, 3, 3
    (2) 5, 6, 5
    Both test cases have two equal sides and should form an isosceles triangle.
    5. Test cases to verify the boundary condition A = B = C for the equilateral
    triangle:
    (1) 5, 5, 5
    (2) 9, 9, 9
    Both test cases have all sides equal and should form an equilateral triangle.
    6. Test cases to verify the boundary condition A^2 + B^2 = C^2 for the
    right-angled triangle:
    (1) 3, 4, 5
    (2) 5, 12, 13
    Both test cases satisfy the Pythagorean theorem and should form a right -angled
    triangle.
    7. For the non-triangle case, identify test cases to explore the boundary.
    (1) 2, 2, 4
    (2) 3, 6, 9
    Both test cases have two sides that add up to the third side and should not form
    a triangle.
    8. For non-positive input, identify test points.
    (1) 0, 1, 2
    (2) -1, -2, -3
    Both test cases have at least one non-positive value, which is an invalid input.
    
    ## Section B.
    
    1. Convert the Java code comprising the beginning of the doGraham method
    into a control flow graph (CFG).
    
    ![Untitled](https://user-images.githubusercontent.com/107932317/232735997-c322eb14-4b92-4e3c-bf6c-8e21fc3cf816.png)
    
    2.Construct test sets for your flow graph that are adequate for the
    a. following criteria:
    To satisfy statement coverage, we need to ensure that each statement in the CFG is executed at least once. We can achieve this by providing a test case with a single point in the vector. In this case, both loops will not execute, and the return statement will be executed. A test set that satisfies statement coverage would be:
    
    p = [Point (0,0)]
    
    b. Branch Coverage:
    To satisfy branch coverage, we need to ensure that each branch in the CFG isexecuted at least once. We can achieve this by providing a test case with two points such that one of the points has the minimum y-coordinate, and the other has a greater x-coordinate than the minimum. In this case, both loops will execute, and the second branch in the second loop will be taken. A test set that satisfies branch coverage would be:
    
    p = [Point (0,0), Point (1,1)]
    
    c. Basic Condition Coverage:
    
    → To satisfy basic condition coverage, we need to ensure that each condition in the CFG is evaluated to both true and false at least once. We can achieve this by providing a test case with three points such that two of the point s have the same y-coordinate, and the other has a greater x-coordinate than the minimum. In this case, both loops will execute, and the second condition in the second loop will be evaluated to true and false. A test set that satisfies basic condition coverage would be:
    
    p = [Point (0,0), Point (1,1), Point (2,0)]
