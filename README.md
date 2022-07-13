# 0x11. C - printf

### Description

------------

> This is a group project with two memmbers workng on it. We are creating a mini-version of the normal "printf" function found in the <stdio.h> Library. The version that we will create will work the same way as the normal "printf", in that it will allow us to print any argument given to the standard output, that will include printing any combination of strings, integers, characters, among other different datatypes.

------------


#### Resources

------------


[Secrets of printf](https://www.cypress.com/file/54761/download)

------------



#### Authorized functions and macros

------------


write (man 2 write)
malloc (man 3 malloc)
free (man 3 free)
va_start (man 3 va_start)
va_end (man 3 va_end)
va_copy (man 3 va_copy)
va_arg (man 3 va_arg)

------------

#### Compilation

------------



The code must be compiled this way:

**$ gcc -Wall -Werror -Wextra -pedantic *.c**

As a consequence, be careful not to push any c file containing a main function in the root directory of your project (you could have a test folder containing all your tests files including main functions)

The main files will include your main header file (main.h): **#include main.h**

------------

###### Specifiers

Specifier                |Output                        |Examples |
|----------------|-------------------------------|-----------------------------|
| `c` | Character | y |
| `d` or `i` | Signed integer | 1024, -1024 |
| `s` | String of characters | Hello Holberton |
| `b` | Binary Representation of unsigned integer | 01010110 |
| `u` | Unsigned integer | 1024 |
| `o` | Unsigned octal | 432 |
| `x` | Unsigned hexadecimal integer | 3ca |
| `X` | Unsigned hexadecimal integer (uppercase) | 3CA |
| `S` | String with hex-ascii value replacing special chars | \x0A\x0A |
| `p` | Pointer address | 0x403212 |
| `r` | Reversed string of characters | dlroW olleH |
| `R` | ROT13 Translation of string | Uryyb |

###### Flags (In development...)

|Flag                |Description                        |
|----------------|-------------------------------|
| `-` |Left-justify the output within the field width that was given; Right justification is the default (see _width_ sub-specifier). |
| `+` |Preceeds the result with a plus or minus sign (`+` or `-`) even for positive numbers. By default, only negative numbers are preceded with a `-` sign. |
| `(space)` |If no sign is going to be written, a blank space is inserted before the value. |
| `#` |Used with `o`, `x` or `X` specifiers the value is preceeded with 0, 0x or 0X respectively for values different than zero. |
| `0` |Left-pads the number with zeroes (`0`) instead of spaces when padding is specified (see _width_ sub-specifier). |

###### Width (In development...)

|Width                |Description                        |
|----------------|-------------------------------|
| `(number)` |Minimum number of characters to be printed. If the value to be printed is shorter than this number, the result is padded with blank spaces. The value is not truncated even if the result is larger.|
| `*` | The _width_ is not specified in the _format_ string, but as an additional integer value argument preceding the argument that has to be formatted.|

### Precision (In development...)

|.Precision               |Description                        |
|----------------|-------------------------------|
| `.(number)` |**For integer specifiers (`d`, `i`, `o`, `u`, `x`, `X`):** _precision_ specifies the minimum number of digits to be written. If the value to be written is shorter than this number, the result is padded with leading zeros. The value is not truncated even if the result is longer. A _precision_ of 0 means that no character is written for the value 0. **For `s`**: this is the maximum number of characters to be printed. By default all characters are printed until the ending null character is encountered. If the period is specified without an explicit value for _precision_, 0 is assumed. |

### Lenght modifiers (In development...)

|Modifier/Specifier  |`d` & `i`  |`u`, `o`, `x`, `X` |`c` |`s` |`p` |
|----------------|---------|------------|-------------|-----|-------|
| `none` | int |unsigned int | int| char pointer| void pointer |
| `h` |short int|unsigned short int |     |     |              |
| `l` |long int |unsigned long int  |     |     |              |

------------

#### Tasks required for this project


------------

0. ######  I'm not going anywhere. You can print that wherever you want to. I'm here and I'm a Spur for life 
Write a function that produces output according to a format.
Handle the following conversion specifiers:
- c
- s
- %

1. ###### Education is when you read the fine print. Experience is what you get if you dont
Handle the following conversion specifiers:
- d
- i

2. ###### With a face like mine, I do better in print
Handle the following conversion specifiers:
- b

3. ###### What one has not experienced, one will never understand in print
Handle the following conversion specifiers:
- u
- o
- x
- X

4. ###### Nothing in fine print is ever good news
Use a local buffer of 1024 chars in order to call write as little as possible.

5. ###### Handle the following custom conversion specifier
- S : prints the string.
- Non printable characters (0 < ASCII value < 32 or >= 127) are printed this way: \x, followed by the ASCII code value in hexadecimal (upper case - always 2 characters).

6. ###### How is the world ruled and led to war? Diplomats lie to journalists and believe these lies when they see them in print
Handle the following conversion specifier: p

7. ###### The big print gives and the small print takes away
Handle the following flag characters for non-custom conversion specifiers:
- ´+´
- space
- ´#´ 

8. ###### Sarcasm is lost in print
Handle the following length modifiers for non-custom conversion specifiers:
- l
- h
Conversion specifiers to handle: d, i, u, o, x, X

9. ###### Print some money and give it to us for the rain forests
Handle the field width for non-custom conversion specifiers.

10. ###### The negative is the equivalent of the composer's score, and the print the performance
Handle the precision for non-custom conversion specifiers.

11. ###### It's depressing when you're still around and your albums are out of print
Handle the 0 flag character for non-custom conversion specifiers.

12. ###### Every time that I wanted to give up, if I saw an interesting textile, print what ever, suddenly I would see a collection
Handle the - flag character for non-custom conversion specifiers.

13. ###### Print is the sharpest and the strongest weapon of our party
Handle the following custom conversion specifier:
 - r : prints the reversed string

14. ###### The flood of print has turned reading into a process of gulping rather than savoring 
Handle the following custom conversion specifier:
- R: prints the rot13'ed string

15. ###### *
All the above options work well together.

### Authors
* [Miyanda Hakooma](https://github.com/mhakooma/printf)
* [Adetoun Lawal](https://github.com/mhakooma/printf/tree/Adetounl)
