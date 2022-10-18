# Rewrite printf function

This project has been done by:

- Vincent Bakpatina
- Yonathan Tamyalew

**`_printf`**  writes out a format to stdout (standard output). The provided format may contain format specifiers

## Prototype

```c
 int printf (const char* format, ...);
```

- **Return Value**: If the function successfully executes, it returns the total number of characters written to the standard output.
- **Arguments**:  format is the string passed to the function. There can be additional arguments following format,

### Format Specifier

The format specifier follows this prototype:

```c
 %[flags][width][.precision][length]specifier
```

| Specifier | argument |
| --- | --- |
| d  | Signed INT |
| u | Unsigned INT |
| o | Unsigned Octal |
| x or X | Unsigned Hexadecimal |
| e or E | Floating Point |
| g or G | Shortest Representation |
| a or A | Hexadecimal Floating Point (lower/ upper case) |
| c | Character |
| s | String of characters |

| flag | description |
| --- | --- |
| - | Left-justify (default:right) |
| + | Force print + sign with positives |

| .precision | description |
| --- | --- |
| .number | specifies number of digits to write |

| width | description |
| --- | --- |
| (number) | Minimum number of character to print |

## Examples

```c

   _printf ("Integers: %i %u \n", -3456, 3456);
   _printf ("Characters: %c %c \n", 'z', 80);
   _printf ("Decimals: %d %ld\n", 1997, 32000L);
   _printf ("Preceding with empty spaces: %10d \n", 1997);
   _printf ("Width: %*d \n", 15, 140);
   _printf ("%s \n", "Alx");
   return 0;

```

<aside>
<img src="https://www.notion.so/icons/command-line_gray.svg" alt="https://www.notion.so/icons/command-line_gray.svg" width="40px" /> Output

Integers: -3456 3456
Characters: z P
Decimals: 1997 32000
Preceding with empty spaces:       1997
Width:             140
Alx

</aside>
