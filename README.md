# WebAppExamples

The following files are included in this repository

## 1) BasicCalcCompleted.html

This file is a basic calculator app. I have included the Style (CSS), Script (JavaScript 
and interface (HTML) in one page for simplicity:

<img src="https://github.com/NeilParkerBSDC/WebAppExamples/blob/main/BasicCalculator.png" alt="Basic Calculator screenshot" width=600>


[File Link](https://github.com/NeilParkerBSDC/WebAppExamples/blob/main/BasicCalcCompleted.html)

* * *
*Further Files Yet To Be added*

## 2) BasicCalcCompletedSeparateButtons.html

This is a variation on th files above with separate buttons for each operation. This means putting each operation (i.e. +, -, *, /) into different functions which are called in turn by the four seprate buttons. I have also tweeked the CSS to give the ```<div>``` and the buttons a drop shadow.

<img src="https://github.com/NeilParkerBSDC/WebAppExamples/blob/main/BasicCalculatorSeparateButtons.png" alt="Basic Calculator with separate operator buttons" width=600>

[File Link](https://github.com/NeilParkerBSDC/WebAppExamples/blob/main/BasicCalcCompletedSeparateButtons.html)

## 3) TradCalc.html

This calculator takes a different approach. The aim is to replicate a tradition hand held calculator. There are different buttons for all the input numbers and opertors etc. Each calls different function:

<img src="https://github.com/NeilParkerBSDC/WebAppExamples/blob/main/TradCalc.png" alt="An emulation of a tradition hand held calculator" width=600>

[File Link](https://github.com/NeilParkerBSDC/WebAppExamples/blob/main/TradCalc.html)

The operation of this app is as follows:

```mermaid

flowchart TD
    Start((Start)) --> FN1-1(Enter digit for first number)
    FN1-1 --> FN1-2(Digit added to display \n on the right of \n any numbers already \n being displayed)
    FN1-2 -->FN1-3{Enter another digit?}
    FN1-3 --> | Yes | FN1-1
    FN1-3 --> | No | FO(Click on operator button)
    FO --> FO1[/Number in display added \n to memory as No1/]
    FO1 --> FO2(Display cleared)
    FO2 --> FO3[/Operator stored based on which \n operator button was pressed/]
    FO3 --> FN2-1(Enter digit for second number)
    FN2-1 --> FN2-2(Digit added to display \n on the right of \n any numbers already \n being displayed)
    FN2-2 -->FN2-3{Enter another digit?}
    FN2-3 --> | Yes | FN2-1
    FN2-3 --> | No | Eq(Click on Equals button)
    Eq --> Eq1[/Number in display added \n to memory as No2/]
    Eq1 --> Eq2(Display cleared)
    Eq2{Which Operator}--> | Plus | EQ3-1(Answer=NO1 + NO2)
    Eq2--> | Minus | EQ3-2(Answer=NO1 - NO2)
    Eq2--> | Multiply | EQ3-3(Answer=NO1 * NO2)
    Eq2--> | Divide| EQ3-4(Answer=NO1 / NO2)
    EQ3-1 --> DA(Display Answer)
    EQ3-2 --> DA(Display Answer)
    EQ3-3 --> DA(Display Answer)
    EQ3-4 --> DA(Display Answer)
    DA --> End((End))

```


