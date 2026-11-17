# Experiment 7: PL/SQL – Variables, Control Structures and Loops

## AIM
To write and execute simple PL/SQL programs using variables, loops, and conditional statements.


## THEORY

PL/SQL, which stands for Procedural Language extensions to the Structured Query Language (SQL). It is a combination of SQL along with the procedural features of programming languages.

**Syntax:**
```sql
DECLARE 
   <declarations section> 
BEGIN 
   <executable command(s)>
EXCEPTION 
   <exception handling> 
END;
```

### Basic Components of PL/SQL Block:
- DECLARE: Section to declare variables and constants.
- BEGIN: The execution section that contains PL/SQL statements.
- EXCEPTION: Handles errors or exceptions that occur in the program.
- END: Marks the end of the PL/SQL block.

# PL/SQL Programs – Steps and Expected Output

## 1. Write a PL/SQL program to find the Greatest of Two Numbers

### Steps:
- Declare two numeric variables and initialize them.
- Use an `IF` statement to compare the values.
- Display the greater number using `DBMS_OUTPUT.PUT_LINE`.

### Program
```
-- Sudharsan S(212224040334)
DECLARE
    num1 NUMBER := 45;
    num2 NUMBER := 80;
BEGIN
    IF num1 > num2 THEN
        DBMS_OUTPUT.PUT_LINE('Greater number is: ' || num1);
    ELSE
        DBMS_OUTPUT.PUT_LINE('Greater number is: ' || num2);
    END IF;
END;

```
**Expected Output:**  
Greater number is: 80
---


### Output
<img width="769" height="829" alt="image" src="https://github.com/user-attachments/assets/e0e851b7-09c4-4e11-8607-f394c7411852" />



## 2. Write a PL/SQL program to Calculate Sum of First N Natural Numbers

### Steps:
- Declare a variable `n` and assign a value (e.g., 10).
- Initialize a `sum` variable to 0.
- Use a `WHILE` loop to iterate from 1 to `n`, adding each number to the sum.
- Display the result using `DBMS_OUTPUT.PUT_LINE`.

### Program
```
-- Sudharsan S(212224040334)
DECLARE
    n NUMBER := 10;
    i NUMBER := 1;
    total_sum NUMBER := 0;
BEGIN
    WHILE i <= n LOOP
        total_sum := total_sum + i;
        i := i + 1;
    END LOOP;
    DBMS_OUTPUT.PUT_LINE('Sum of first ' || n || ' natural numbers is: ' || total_sum);
END;

```

**Expected Output:**  
Sum of first 10 natural numbers is: 55

---
### Output
<img width="944" height="856" alt="image" src="https://github.com/user-attachments/assets/6939d5f5-fd96-4bb0-93a3-ed8b5e02f75b" />

## 3. Write a PL/SQL program to generate Fibonacci series

### Steps:
- Declare the variable `n` to indicate how many terms to generate.
- Initialize the first two Fibonacci numbers (0 and 1).
- Use a loop to generate the next terms using the formula `c = a + b`.
- Print each term in the series.

### Program
```
-- Sudharsan S(212224040334)
DECLARE
    n NUMBER := 7;
    a NUMBER := 0;
    b NUMBER := 1;
    c NUMBER;
BEGIN
    DBMS_OUTPUT.PUT_LINE('n = ' || n);
    DBMS_OUTPUT.PUT('Fibonacci sequence: ' || a || ', ' || b);
    FOR i IN 3..n LOOP
        c := a + b;
        DBMS_OUTPUT.PUT(', ' || c);
        a := b;
        b := c;
    END LOOP;
    DBMS_OUTPUT.NEW_LINE;
END;

```
**Expected Output:**  
n = 7  
Fibonacci sequence: 0, 1, 1, 2, 3, 5, 8

---

### Output
<img width="783" height="857" alt="image" src="https://github.com/user-attachments/assets/6f2d4403-5743-405f-a6e4-5418cda2a624" />


## 4. Write a PL/SQL Program to display the number in Reverse Order

### Steps:
- Declare a variable `n` and assign a value (e.g., 1535).
- Use a loop to extract each digit using modulo and reverse the number.
- Display the reversed number.

### Program
```
-- Sudharsan S(212224040334)
DECLARE
    n NUMBER := 1535;
    temp NUMBER := 1535;
    rev NUMBER := 0;
    rem NUMBER;
BEGIN
    WHILE temp > 0 LOOP
        rem := MOD(temp, 10);
        rev := (rev * 10) + rem;
        temp := TRUNC(temp / 10);
    END LOOP;
    DBMS_OUTPUT.PUT_LINE('n = ' || n);
    DBMS_OUTPUT.PUT_LINE('Reversed number is ' || rev);
END;
```
**Expected Output:**  
n = 1535  
Reversed number is 5351

---

### Output

<img width="758" height="863" alt="image" src="https://github.com/user-attachments/assets/51345f83-1835-452f-9e5b-eb8e8f0f970d" />

## 5. Write a PL/SQL program to find the largest of three numbers

### Steps:
- Declare three numeric variables `a`, `b`, and `c`.
- Use nested `IF-ELSIF-ELSE` conditions to find the largest among the three.
- Display the largest number.

### Program
```
-- Sudharsan S(212224040334)
DECLARE
    a NUMBER := 10;
    b NUMBER := 9;
    c NUMBER := 15;
BEGIN
    DBMS_OUTPUT.PUT_LINE('a = ' || a || ', b = ' || b || ', c = ' || c);
    IF a >= b AND a >= c THEN
        DBMS_OUTPUT.PUT_LINE('Largest of three number is ' || a);
    ELSIF b >= a AND b >= c THEN
        DBMS_OUTPUT.PUT_LINE('Largest of three number is ' || b);
    ELSE
        DBMS_OUTPUT.PUT_LINE('Largest of three number is ' || c);
    END IF;
END;
```
**Expected Output:**  
a = 10, b = 9, c = 15  
Largest of three number is 15

### Output

<img width="825" height="848" alt="image" src="https://github.com/user-attachments/assets/646f79ae-635a-49c6-aa60-fe82230cd8cd" />

## RESULT
Thus, the PL/SQL programs using variables, conditionals, and loops were executed successfully.
