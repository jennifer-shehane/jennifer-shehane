---
title: Sass Mixin for Setting Column Widths on Tables
date: 2014-04-09 13:01:49
subtitle:
tags:
  - sass
---


Mixins are one of my favorite features of [Sass](http://sass-lang.com/). It allows you to write logic within css. I often use mixins to reduce the amount of code needed for commonly used styles of a project.

When designing our web app at [InspectAll](http://www.inspectall.com/), I found myself writing the same css styles over and over to set column widths on our fixed-width tables. As of this writing I found 70 tables in our web app styled this way. So I wrote a mixin to help me more easily set column widths for each table.

## Sass Mixin

```sass
@mixin th-width($col, $width) {
    #{$col} {  
        width: $width;  
    }
}

@mixin table-columns($widths...) {
    table-layout: fixed;
    width: 100%;

    th, td {
        overflow: hidden;
        text-overflow: ellipsis;
        white-space: nowrap;
    }

    $n: 1;
    $var: "th:nth-child(" + $n + ")";
    @each $width in $widths {
        @include th-width($var, $width);
        $n: $n + 1;
        $var: "th:nth-child(" + $n + ")";
    }
}
```

Now I can just write one line of code that passes in each column's width as an argument to our table-columns mixin. It works the same whether I need 2 columns or 10 columns.

```sass
#activities-list {  
    @include table-columns(4%, 68%, 16%, 11%);
}
```

## Output

```sass
#activities-list {
    table-layout: fixed; width: 100%;
}

#activities-list td, #accounts-list th {
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
}

#activities-list th:nth-child(1) {
    width: 4%;
}

#activities-list th:nth-child(2) {
    width: 68%;
}

#accounts-list th:nth-child(3) {
    width: 16%;
}

#activities-list th:nth-child(4) {
    width: 11%;
}
```

This works great for tables, but most of the "tables" in our application are actually lists that have just been styled to look like tables. We often do this because they're easier to style or they work better with the way we've built our [Marionette](http://marionettejs.com/) views.

Here's how we set column-widths using our `list-columns` Sass mixin:

### Sass Mixin

```
@mixin el-width($col, $width) {
  #{$col} {
    $width: $width;
  }
}

@mixin list-columns($widths...) {
    width: 100%;

    li {
        overflow: auto;  
        border-bottom: 1px solid #eeeeee;  
        display: block;
        &>div {
             float: left;
            &>div {
                padding: 6px 12px;
                overflow: hidden;
                text-overflow: ellipsis;
                white-space: nowrap;
            }
        }
    }


    $n: 1;
    $var: "li>div:nth-child(" + $n + ")";
    @each $width in $widths {
        @include el-width($var, $width);
        $n: $n + 1;
        $var: "li>div:nth-child(" + $n + ")";
    }
}
```

### Include Mixin on List's id or class

```
#activities-list {  
    @include list-columns(4%, 68%, 16%, 11%);
}
```

### Output

```
#activities-list {
    width: 100%;
}

#activities-list li {
    overflow: auto;
    border-bottom: 1px solid #eeeeee;
    display: block;
}

#activities-list > div {
    float: left;
}

#activities-list > div > div {
    padding: 6px 12px;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
}

#activities-list li>div:nth-child(1) {
    width: 4%;
}

#activities-list li>div:nth-child(2) {
    width: 68%;
}

#accounts-list li>div:nth-child(3) {
    width: 16%;
}

#activities-list li>div:nth-child(4) {
    width: 11%;
}
```

That's it! Sass mixins have allowed me to get our tables and lists styled in no time and reduced the amount of styling errors introduced to our project.
