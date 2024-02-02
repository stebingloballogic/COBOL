PROJECT 1

Arithmetic Operations 

COBOL-85



IDENTIFICATION DIVISION.
       PROGRAM-ID. ArithmeticOperations.
       
       DATA DIVISION.
       WORKING-STORAGE SECTION.
       01 Num1              PIC 9(5).
       01 Num2              PIC 9(5).
       01 Result            PIC 9(10).
       
       PROCEDURE DIVISION.
       
           DISPLAY "Enter first number: ".
           ACCEPT Num1.
           
           DISPLAY "Enter second number: ".
           ACCEPT Num2.
           
           ADD Num1 Num2 GIVING Result.
           DISPLAY "Addition Result: " Result.
           
           SUBTRACT Num2 FROM Num1 GIVING Result.
           DISPLAY "Subtraction Result: " Result.
           
           MULTIPLY Num1 BY Num2 GIVING Result.
           DISPLAY "Multiplication Result: " Result.
           
           DIVIDE Num1 BY Num2 GIVING Result.
           DISPLAY "Division Result: " Result.
           
           STOP RUN.






COBOL-2002 VERSION


IDENTIFICATION DIVISION.
       PROGRAM-ID. ArithmeticOperations.
       
       DATA DIVISION.
       WORKING-STORAGE SECTION.
       01 Num1              PIC 9(5).
       01 Num2              PIC 9(5).
       01 Result            PIC 9(10).
       
       PROCEDURE DIVISION.
       
           DISPLAY "Enter first number: ".
           ACCEPT Num1.
           
           DISPLAY "Enter second number: ".
           ACCEPT Num2.
           
           COMPUTE Result = Num1 + Num2.
           DISPLAY "Addition Result: " Result.
           
           COMPUTE Result = Num1 - Num2.
           DISPLAY "Subtraction Result: " Result.
           
           COMPUTE Result = Num1 * Num2.
           DISPLAY "Multiplication Result: " Result.
           
           IF Num2 NOT = 0
               COMPUTE Result = Num1 / Num2.
               DISPLAY "Division Result: " Result.
           ELSE
               DISPLAY "Cannot divide by zero.".
           END-IF.


