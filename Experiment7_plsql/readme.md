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

## PROGRAM:
```
DECLARE
    num1 NUMBER := 50;
    num2 NUMBER := 80;
BEGIN
    IF num1 > num2 THEN
        DBMS_OUTPUT.PUT_LINE('Greater number is: ' || num1);
    ELSE
        DBMS_OUTPUT.PUT_LINE('Greater number is: ' || num2);
    END IF;
END;
/
```

**Expected Output:**  
Greater number is: 80

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/1cfad715-dc54-43b9-95c4-6a54ec36997d" />


---

## 2. Write a PL/SQL program to Calculate Sum of First N Natural Numbers

### Steps:
- Declare a variable `n` and assign a value (e.g., 10).
- Initialize a `sum` variable to 0.
- Use a `WHILE` loop to iterate from 1 to `n`, adding each number to the sum.
- Display the result using `DBMS_OUTPUT.PUT_LINE`.

## PROGRAM:
```
DECLARE
    n NUMBER := 10;
    i NUMBER := 1;
    sum NUMBER := 0;
BEGIN
    WHILE i <= n LOOP
        sum := sum + i;
        i := i + 1;
    END LOOP;
    DBMS_OUTPUT.PUT_LINE('Sum of first ' || n || ' natural numbers is: ' || sum);
END;
/

```

**Expected Output:**  
Sum of first 10 natural numbers is: 55
<img width="1158" height="828" alt="image" src="https://github.com/user-attachments/assets/34752010-e512-40d7-a5f8-faad64518eb7" />


---

## 3. Write a PL/SQL program to generate Fibonacci series

### Steps:
- Declare the variable `n` to indicate how many terms to generate.
- Initialize the first two Fibonacci numbers (0 and 1).
- Use a loop to generate the next terms using the formula `c = a + b`.
- Print each term in the series.

## PROGRAM:
```
DECLARE
    n NUMBER := 7;
    a NUMBER := 0;
    b NUMBER := 1;
    c NUMBER;
    i NUMBER := 3;
BEGIN
    DBMS_OUTPUT.PUT_LINE('Fibonacci sequence:');
    DBMS_OUTPUT.PUT_LINE(a);
    DBMS_OUTPUT.PUT_LINE(b);
    
    WHILE i <= n LOOP
        c := a + b;
        DBMS_OUTPUT.PUT_LINE(c);
        a := b;
        b := c;
        i := i + 1;
    END LOOP;
END;
/

```

**Expected Output:**  
n = 7  
Fibonacci sequence: 0, 1, 1, 2, 3, 5, 8
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/51f3b580-19cb-4f33-9766-978164f2b9a8" />


---

## 4. Write a PL/SQL Program to display the number in Reverse Order

### Steps:
- Declare a variable `n` and assign a value (e.g., 1535).
- Use a loop to extract each digit using modulo and reverse the number.
- Display the reversed number.
  
## PROGRAM:
```
DECLARE
    n NUMBER := 1535;
    rev NUMBER := 0;
    rem NUMBER;
    temp NUMBER;
BEGIN
    temp := n;
    WHILE n > 0 LOOP
        rem := MOD(n, 10);
        rev := (rev * 10) + rem;
        n := TRUNC(n / 10);
    END LOOP;
    DBMS_OUTPUT.PUT_LINE('Reversed number is: ' || rev);
END;
/

```
**Expected Output:**  
n = 1535  
Reversed number is 5351
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/41e9f7c2-735e-40c7-a7da-7bbe58e8f0ed" />


---

## 5. Write a PL/SQL program to find the largest of three numbers

### Steps:
- Declare three numeric variables `a`, `b`, and `c`.
- Use nested `IF-ELSIF-ELSE` conditions to find the largest among the three.
- Display the largest number.

## PROGRAM:
```
DECLARE
    a NUMBER := 10;
    b NUMBER := 9;
    c NUMBER := 15;
BEGIN
    IF (a > b) AND (a > c) THEN
        DBMS_OUTPUT.PUT_LINE('Largest of three numbers is: ' || a);
    ELSIF (b > a) AND (b > c) THEN
        DBMS_OUTPUT.PUT_LINE('Largest of three numbers is: ' || b);
    ELSE
        DBMS_OUTPUT.PUT_LINE('Largest of three numbers is: ' || c);
    END IF;
END;
/
```
**Expected Output:**  
a = 10, b = 9, c = 15  
Largest of three number is 15
<img width="1124" height="842" alt="image" src="https://github.com/user-attachments/assets/b70c21d0-0d43-4697-863f-115fc8159dbd" />


## RESULT
Thus, the PL/SQL programs using variables, conditionals, and loops were executed successfully.


