---
title: 'Code Exercise: Greedy'
date: 2014-11-27 12:58:57
subtitle:
tags:
  - exercise
---


This week, one of the assignments from [Harvard's CS50](https://www.edx.org/course/introduction-computer-science-harvardx-cs50x#.VHaO21fF8Q4) class was a little exercise called **Greedy**. A greedy algorithm as defined by the National Institute of Standards and Technology is:

> An algorithm that always takes the best immediate, or local, solution while finding an answer. Greedy algorithms find the overall, or globally, optimal solution for some optimization problems, but may find less-than-optimal solutions for some instances of other problems.

In order to demonstrate this, imagine you are a cashier and you have a customer that needs change. A "greedy" cashier would want to reach into the drawer as few times as possible, giving away as few coins as possible. So, for each coin chosen, they want to take the largest chunk possible out of the change remaining. It turns out that using the largest coin possible for the change remaining will result in the least amount of coins used overall.

So the challenge is to be a "greedy" cashier. First, you need to prompt and ask how much change is needed. Then, calculate the least amount of coins necessary to give change only using quarters, dimes, nickels and pennies and tell me how many is needed of each coin.

For example, If I needed .42 in change, you should tell me:

`You need 5 coins. 1 quarter, 1 dime, 1 nickel, and 2 pennies.`

You'll need to handle corner cases if a negative number or string is entered.

Here is my implementation in C.

```c
#include <stdio.h>
#include <math.h>
#include <cs50.h>

float promptUser(void);
void checkNegNumbers(int);
int calculateCoins(int);

int main(void) {
  promptUser();
}

float promptUser(void) {
  printf("How much change is owed? ");
  float changeAmount = GetFloat();

  // convert change to integer of # of cents
  int intAmount = round(changeAmount * 100);

  checkNegNumbers(intAmount);
  return 0;
}

void checkNegNumbers(num) {
  if(num < 0){
    printf("Please enter a positive number for your change. ");
    float changeAmount = GetFloat();

    // convert change to integer of # of cents
    int intAmount = round(changeAmount * 100);

    checkNegNumbers(intAmount);
  } else {
    calculateCoins(num);
  }
}

int calculateCoins(centsAmount) {

  // define coin set
  int quarter = 25;
  int dime = 10;
  int nickel = 5;
  int penny = 1;

  // calculate max num of each coin and remove from total amount
  int numQuarters = (centsAmount / quarter);
  centsAmount = centsAmount - (numQuarters * quarter);

  int numDimes = (centsAmount / dime);
  centsAmount = centsAmount - (numDimes * dime);

  int numNickels = (centsAmount / nickel);
  centsAmount = centsAmount - (numNickels * nickel);

  int numPennies = (centsAmount / penny);

  // add the number of coins for each coin together
  int total = numQuarters + numDimes + numNickels + numPennies;

  printf("You need %d coins. %d quarters, %d dimes, %d nickels, and %d pennies.\n", total, numQuarters, numDimes, numNickels, numPennies);

  return 0;
}
```

There's a lot of copy / pasting going on in this one, which is a good sign that it could use some refactoring, but I'm moving on for now to some of the next challenges.
