---
title: 'Code Exercise: Mario'
date: 2014-11-25 12:59:19
subtitle:
tags:
  - exercise
---


## Introduction to Computer Science Course

Being a self-taught developer, I've never really taken a basic "computer science" course. I've mostly learned within the confines of one language: JavaScript. In an effort to broaden my understanding of writing programs and languages, I signed up for [Harvard's CS50 course - Introduction to Computer Science](https://cs50.harvard.edu/).

Harvard offers the CS50 course for free online through various channels including [YouTube](https://www.youtube.com/user/cs50tv) and [iTunes](https://itunes.apple.com/us/course/this-is-cs50-2011./id529181544). I'm taking the course through [edX](https://www.edx.org/), a site that aggregates courses from universities all over the world.

The course offers enthusiastic lectures from David Maran accompanied with short videos, reading materials, walkthroughs and hands-on homework. The syllabus explains the material best:

> This course teaches students how to think algorithmically and solve problems efficiently. Topics include abstraction, algorithms, data structures, encapsulation, resource management, security, software engineering, and web development. Languages include C, PHP, and JavaScript plus SQL, CSS, and HTML. Problem sets inspired by real-world domains of biology, cryptography, finance, forensics, and gaming. Designed for concentrators and non-concentrators alike, with or without prior programming experience.

## Mario

One of the first problem sets is an exercise called "Mario". The objective is to create a program where you can enter a height in blocks for a mario-like pyramid (like the one Mario runs up to reach the flag-pole). Once the height is specified, you then build the pyramid using hashes and spaces.



If I were to enter the number 9, then the end result should look something like this:

```
        ##
       ###
      ####
     #####
    ######
   #######
  ########
 #########
##########
```

Notice the top of the pyramid has 2 blocks. You also need to make sure to handle corner cases like someone entering a negative number or string.

You could really implement this in any language you like. The CS50 course starts out writing C, so here is my implementation in C. **Note:** I've included a header file given to CS50 students found [here](http://dkui3cmikz357.cloudfront.net:80/library50/c/cs50-library-c-3.0/cs50.h). This file contains the code for my `GetInt()` function.


```C
#include <stdio.h>
#include <cs50.h>

void buildPyramid(blocks) {
  // build pyramid
  for(int j = 0; j < blocks; j++) {

    // type spaces on every row
    int space = blocks - (j + 1);
    for(int i = 0; i < space; i++) {
      printf(" ");
    }

    // type 2 hashes on every row
    printf("##");

    // type extra hashes on every row
    int hash = blocks - (blocks - j);
    for(int k = 1; k <= hash; k++){
      printf("#");
    }

    // return for new row
    printf("\n");
  }
}

void checkNumber(num) {
  if(num <= 0) {
    // warn them if a negative num
    printf("Please enter a positive number. ");
    int numBlocks = GetInt();
    checkNumber(numBlocks);
  }
  else {
    buildPyramid(num);
  }
}

int main(void) {
  // get number of blocks to build
  printf("How many blocks high do you want the pyramid? ");
  int numBlocks = GetInt();
  checkNumber(numBlocks);
}
```

This was a nice exercise for anyone needing practice with loops and a good starter for any new language.
