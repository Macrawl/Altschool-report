## CLASSWORK

 Describe 15 operators including the file operator in bash scripting and explain what each operator mean.

 ## SOLUTION

 Various operations and comparisons can be carried out using bash operators. These operators are necessary for command-line and scripting activities. A summary of various popular Bash operators is provided below:


 1. Arithmetic Operators

 2. Comparison Operators

 3. Logical Operators

 4. String Operators

 5. File Operators


 ## ARITHMETIC OPERATORS
 A set of symbols or signs that indicate a certain mathematical operation that is to be performed in a program is known as an arithmetic operator.

 These operators includes;

 -  Addition	(+)	: Adds one operand to the other

 - Subtraction	(-)	:  Subtracts the second operand from the first

- Multiplication(*)	:  Multiplies one operand by the other

- Division	(/)     :	Divides the first operand by the second

- Modulo	(%)     :	Divides the first INTEGER operand by the second, and returns the remainder


## COMPARISON OPERATORS


Comparison operators are able to evaluate and compare strings,numbers & values. In contrast to arithmetic expressions, comparison operator expressions do not return a numerical value. Expressions for comparison return either 1, which indicates "true," or 0, which indicates for "false."

These operators includs;

- = (Equal to)

- != (Not equal to)

- -eq (Equal, for numeric comparisons)

- -ne (Not equal, for numeric comparisons)

- -lt (Less than)

- -le (Less than or equal to)

- -gt (Greater than)

- -ge (Greater than or equal to)


## LOGICAL OPERATORS

Conditional operators gives you the ability to determine if one or more conditions are true or false,


1.  Logical AND  ( && ):
The AND operator (&& or -a) is used to combine two conditions in a way that the overall expression is true only if both conditions are true. The syntax for the AND operator is:

``` 
condition1 && condition2
```


2. Logical OR   ( || ):
The OR operator (|| or -o) is used to combine two conditions in a way that the overall expression is true if at least one of the conditions is true. The syntax for the OR operator is:


```
condition1 || condition2
```

3. Logical NOT  ( !  ):
The NOT operator (!) inverts the truthiness of a given condition. If the condition is true, the NOT operator returns false, and vice versa. The syntax for the NOT operator is:

```
!condition
```


## FILE OPERATORS

file operators are used to perform various tests and checks on files within a Bash script or on the command line. These operators help you determine various properties and conditions related to files. Here are some common Bash file operators:

- **-e:** This operator checks if a file exists. It returns true if the file exists, and false otherwise.

Example:

```
if [ -e "/path/to/file" ]; then

    echo "File exists"
fi
```

-  **-f:** This operator checks if a file is a regular file (not a directory or a special file). It returns true for regular files and false for directories, device files, and other special files.

Example:

```
if [ -f "/path/to/file" ]; then

    echo "It's a regular file"
fi
```

- **-d:** This operator checks if a path is a directory. It returns true if the path is a directory and false otherwise.

Example:

```
if [ -d "/path/to/directory" ]; then

    echo "It's a directory"
fi

```
- **-r:** This operator checks if a file is readable. It returns true if the file is readable and false if it's not.

Example:

```
if [ -r "/path/to/file" ]; then

    echo "File is readable"
fi

```

- **-w:** This operator checks if a file is writable. It returns true if the file is writable and false if it's not.

Example:

```
if [ -w "/path/to/file" ]; then

    echo "File is writable"
fi

```

- **-x:** This operator checks if a file is executable. It returns true if the file is executable and false if it's not.

Example:

```
if [ -x "/path/to/script.sh" ]; then

    echo "Script is executable"
fi

```

The existence, type, and permissions of files are frequently utilized in conditional statements within Bash scripts to make decisions, and these file operators are crucial when building strong and adaptable scripts that can handle diverse file-related tasks.