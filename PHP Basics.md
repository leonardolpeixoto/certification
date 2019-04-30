# PHP Basics

## Basic Language Features
All statements in PHP must be terminated with a semicolon. An exception to this is if the statement happens to be the last statement before a closing tag.  

Whitespace has no semantic meaning in PHP. Whitespace may not appear in the middle of function names, variable names or keywords.  

Multiple statements are allowed on a single line.  

Code blocks are denoted by the brace symbols { }.  

Only variable and constant names are case-sensitive.  

## Inserting PHP into Web Pages
There are several ways to delimit PHP script, but only the first two in this table era commonly used:  


| Type     | Open                    | Close     | Note       |
|   ---    |           ---           |    ---    |    ---     |
| Standard | <?php                   | ?>        |            |
| Echo     | <?=                     | ?>        |            |
| Short    | <?                      | ?>        | Deprecated |
| Script   | <script language="php"> | </script> | Do not use |
| ASP      | <%                      | %>        | Deprecated |

It is quite common in PHP programs to omit the closing tag in a file. This is a useful way to prevent problems with newline characters appearing after the closing tag.  

Theses newline characters are sent as output by the PHP interpreter and could interfere with the HTTP headers or cause other unintended side-effects.  

## Language Constructs
| Used | For |
|  --- | --- |
| assert | Debug command to test a condition and do something if it is not true |
| echo | Outputting a value to stdout |
| print | Outputting a value to stdout |
| exit | Optionally outputting a message and terminating the program |
| die | This is an alias for exit |
| return | Terminates a function and returns control to the calling scope, or if called in the global scope, terminates the program |
| include | Includes a file and evaluates it. PHP will make issue a warning if the file is not found or cannot be read |
| include_once | If you specify include_once then PHP will make sure that it includes the file only once |
| require | PHP will include a file and evaluate it. If the file is not found or cannot be read, then a fatal error will be generated |
| require_once | As for incude_once, but a fatal error will be generated instead of a warning |
| eval | The argument is evaluated as PHP and affects the calling scope |
| empty | Returns a Boolean value depending on whether the variable is empty  or not. Empty variables include null variables, empty string, arrays with no elements, numeric values of 0, a string value of 0, and Boolean values of false |
| isset | Returns true if the variable has been set and false otherwise |
| unset | Clears a variable |
| list |Assigns multiple variables at one time from an array |

## Comments
There are three styles to mark comments:

```php
<?php
# Perl style comments
// C style comments
/*
 * Multiline comment 
 */
```

## Representing Numbers
There are four ways in which an integer may be expressed in php script:

| Notation    | Example      | Note                           |
|-------------|--------------|--------------------------------|
| Decimal     | 1234         |                                |
| Binary      | 0b1001110010 | Identified by leading 0b or 0B |
| Octal       | 02322        | Identified by leading 0        |
| Hexadecimal | 0x4D2        | Identified by leading 0x or 0X |

Floating point numbers can be expressed either in standard decimal format or in exponential format.

| Form        | Example          |
|-------------|------------------|
| Decimal     | 123.56           |
| Exponential | 0.12e2 or 0.12E2 |

## Variables
PHP is a loosely typed language.

PHP has three categories of variable:
- scalars is one that can only hold one value at a time
- composite can contain several values at a time
- resources points to somethings not native to PHP like a handle provide by OS to a file or a database connection. These variables cannot be cast.