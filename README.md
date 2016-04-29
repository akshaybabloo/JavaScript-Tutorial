# JavaScript-Tutorial
JavaScript Tutorial

<!-- MDTOC maxdepth:6 firsth1:2 numbering:0 flatten:0 bullets:1 updateOnSave:1 -->

- [1 Introduction](#1-introduction)   
   - [1.1 Issues](#11-issues)   
- [2 Lets Get Started](#2-lets-get-started)   
   - [2.1 Simple JavaScript](#21-simple-javascript)   
   - [2.2 Structure of JavaScript](#22-structure-of-javascript)   
   - [2.3 Position of the JavaScript Matters](#23-position-of-the-javascript-matters)   

<!-- /MDTOC -->

## 1 Introduction

JavaScript is a high-level programming language developed by Netscape (a subsidiary of AOL) for web and web browsers. JS syntax is derived from C programming language. In general JS itself does not have access to the system I/O i.e. file system, networking, etc. unless you are using a third party JS or if the web browser allows/supports it. So, JavaScript wasn't designed as a general purpose programming language, but it was designed to manipulate web pages.

Like HTML and CSS; JavaScript is a client side language. That means it is the browsers ability to interpret the code. Due to its high demand, JavaScript is now also available as server-side language, for example, Node.js.

In this tutorial we will look into the class JavaScript that can be used to manipulate the web pages.

**Things to Remember**

1. **`JavaScript ≠ Java`** - JavaScript is not a light version of Java. Nope.
2. JavaScript is case sensitive i.e. `a` is very much different from `A`

### 1.1 Issues

Following are the issues:

1. What if the user disabled JavaScript in his/her browser?

  Though this is not common, the only thing you can do is to write the code in such a way that the page would render but with limited functionality.

2. What if some browsers can't interpret JavaScript like others do?

  This was a problem when the JavaScript was developed in 1995. JavaScript was originally developed by Brendan Eich of Netscape to incorporate it in their web browser which is called Netscape 2. Later Microsoft developed its JavaScript edition called JScript which was only compatible with Internet Explorer.

  Fortunately, Netscape submitted JavaScript language to ECMA standards body to standardise the language in  1997. The standard edition of JavaScript is called ECMAScript.  Currently the word JavaScript is owned by Mozilla.

  So this means the same code will run everywhere.

## 2 Lets Get Started

**Requirements**

1. Text editor (I'm using [Atom](https://atom.io/))
2. Web browser ([Firefox Developer Edition](https://www.mozilla.org/en-US/firefox/developer/) preferred)
3. [Firebug](http://getfirebug.com/) (Firebug is preinstalled in Firefox Developer Edition)


### 2.1 Simple JavaScript

See [2_1_Simple_JavaScript.html](https://github.com/akshaybabloo/JavaScript-Tutorial/blob/master/2_1_Simple_JavaScript.html)

To write a JavaScript you would have to place it between

```javascript
<script>
  alert("hello world");
</script>
```

For now the placement is not important, we will discuss about this later. I have placed it in `body` tag.

When you open the file you will get an alert as `hello world`.

### 2.2 Structure of JavaScript

* JavaScript is written as a statement with a semicolon in the end.

  ```javascript
  alert("hello world");
  ```
* This means that you can pull multiple statements in each line without any new line
  ```javascript
  alert("hello"); alert("world");
  ```

* JavaScript can do some guess work; that is you don't always have to put a `;` at the end. But **don't** do that, alway close the statement, this is because some browser guesses the code correctly and some don't.

* JavaScript is whitespace insensitive that means your code can contain any number of spaces. For example:
  ```javascript
  alert("hello world");
  alert(    "hello world"    );
  alert("hello world"    );
  alert(
    "hello world"
);
  ```
  The only time space matters are in between the double quotes
  ```javascript
  alert("hello      world")
  ```
  This will print out `hello      world` with five spaces.

* You can add comments by putting two `//` before a sentence or a statement.
  ```javascript
  // This is a comment
  alert("hello world");
  ```
  A block comment could be something like this:
  ```javascript
  /* this is
  a block comment */
  ```

### 2.3 Position of the JavaScript Matters

See [2_3_1_Script_in_body.html](https://github.com/akshaybabloo/JavaScript-Tutorial/blob/master/2_3_Position_Matters/2_3_1_Script_in_body.html) and [2_3_2_Script_in_head.html](https://github.com/akshaybabloo/JavaScript-Tutorial/blob/master/2_3_Position_Matters/2_3_2_Script_in_head.html)

The place where you put the `script` tag does matter. That means browser renders the code sequentially (top to bottom), so if you put the script in the `head` tag the script is first executed and waits for the user to press `ok` and then renders the page, this is opposite when the script is placed in the body. Try to open the two HTML files and see for yours self.
