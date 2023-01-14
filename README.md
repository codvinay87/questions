# questions

Q1 Write a function called swap_variables that takes two variables as input and swaps their values.
def swap_variables(x, y):
    x, y = y, x
    return x, y

Test Cases

input
x = 10
y = 20
output
20
10

input
x = 'hello'
y = 'world'
output
'world'
'hello'

Q2 Write a function called is_integer that takes a variable as input and returns True if the variable is an integer and False otherwise.

def is_integer(x):
    return isinstance(x, int)

Test Cases
input
10
output
True

input
10.5
output
false

input
hello
output
false

Q3 Write a function called is_string that takes a variable as input and returns True if the variable is a string and False otherwise.
def is_string(x):
    return isinstance(x, str)

Test Cases

input
hello
output
True

input
10
output
false

input
['a', 'b', 'c']
output
false



Q4 Write a function called is_list that takes a variable as input and returns True if the variable is a list and False otherwise.
def is_list(x):
    return isinstance(x, list)

Test Cases

input
['a', 'b', 'c']
output
True

input
10
output
false

input
hello
output
false


Q5 Write a function called is_tuple that takes a variable as input and returns True if the variable is a tuple and False otherwise.

def is_tuple(x):
    return isinstance(x, tuple)

Test Cases

input
('a', 'b', 'c')
output
True

input
10
output
false

input
hello
output
false


Q6 Write a function called is_dictionary that takes a variable as input and returns True if the variable is a dictionary and False otherwise.

def is_dictionary(x):
    return isinstance(x, dict)

 Test Cases

input
{'a': 1, 'b': 2, 'c': 3}
output
True

input
10
output
false

input
hello
output
false


Q7 Write a function called is_set that takes a variable as input and returns True if the variable is a set and False otherwise.


def is_set(x):
    return isinstance(x, set)

Test Cases
input
{1, 2, 3}
output
True

input
10
output
false

input
hello
output
false



Q8 waf to reverse a string
def reverse_string(string):
    return string[::-1]

input
hello
output
olleh

input
abcdef
output
fedcba

input
12345
output
54321

Q9 Write a function to check if a string is a palindrome (a word or phrase that reads the same backward as forward).
def is_palindrome(string):
    return string == string[::-1]

input
racecar
output
true

input
hello
output
false

input 
abcba
output
true


Q10 Write a function to check if a string is a pangram (a sentence that contains every letter of the alphabet at least once).


def is_pangram(string):
    alphabet = set(string.lower())
    return all(letter in alphabet for letter in string.lower())

input
The quick brown fox jumps over the lazy dog
output
True
input
Hello, World
output
False
input
abcdefghijklmnopqrstuvwxyz
output
True

Q11 Write a function to check if a string is composed only of digits.
def is_digits(string):
    return all(char.isdigit() for char in string)

input

12345
output
True
input
12345abc
output
False

input
123.45'
output
False

Q12 Write a function to remove all whitespace from a string.

def remove_whitespace(string):
    return ''.join(string.split())


input
'   abc   def   '
output
'abcdef'
input
'abc\n   def\n\tghi'
output
'abcdefghi'

Q13 Write a function to check if a string is composed only of uppercase letters.
Copy code
def is_upper(string):
    return all(char.isupper() for char in string)

Test Cases
input
'ABC'
output
True
input
'Abc'
output
False
input
'123'
output
False

Q14 Write a function to check if a string is composed only of lowercase letters.
Copy code
def is_lower(string):
    return all(char.islower() for char in string)

input
abc
output
True
input
'Abc'
output
False
input
'123'
output
False

Q15 Write a function to check if a number is odd.
Copy code
def is_odd(n):
    return n % 2 == 1
input
3
output
true
input
4
output
false
input
-5
output 
true

Q16 Write a function to check if a number is even.

def is_even(n):
    return n % 2 == 0
input
3
output
false
input
4
output
true
input
-5
output 
false



Q17 Write a function to check if a number is prime.

def is_prime(n):
    if n < 2:
        return False
    for i in range(2, int(n ** 0.5) + 1):
        if n % i == 0:
            return False
    return True


input
2
output
True
input
3
output
True
input
4
output
False
input
5
output
True
input
6
output
False


Q18 Write a function to find the greatest common divisor (GCD) of two numbers.
def gcd(a, b):
    if a == 0:
        return b
    if b == 0:
        return a
    return gcd(b, a % b)


input
3, 5
output
1
input
12, 16
output
4
input
60, 48
output
12

Q19 Write a function to find the least common multiple (LCM) of two numbers.
def lcm(a, b):
    return (a * b) // gcd(a, b)

input
3, 5
output
15
input
12, 
output
 48
input
60, 
output
 120

Q20 Write a function to find the sum of the digits of a number.
Copy code
def sum_digits(n):
    return sum(int(digit) for digit in str(n))


input
12345
output
15
input
1234)
output
10
input
123))
output
6

Q21 Write a function to find the factorial of a number.

def factorial(n):
    if n < 0:
        raise ValueError('Number must be non-negative')
    if n == 0:
        return 1
    return n * factorial(n - 1)

input
0
output
1
input
1
output
1
input
5
output
120
input
1
output
3628800

Q22 Write a function that returns True if two integers are equal, and False otherwise.

def are_equal(a, b):
    return a == b

input
5, 5
output
True
input
5, 6
output
False
input
-5, 
output
 False

Q23 Write a function that returns True if two integers are not equal, and False otherwise.
def are_not_equal(a, b):
    return a != b

input
5, 5
output
False
input
5, 6
output
True
input
-5, 
output
 True
Q24 Write a function that returns True if an integer is greater than another integer, and False otherwise.
def is_greater(a, b):
    return a > b

input
5, 5
output
False
input
5, 6
output
False
input
-5, 
output
False
input
5, 4
output
True

Q25 Write a function that returns True if an integer is less than another integer, and False otherwise.

def is_less(a, b):
    return a < b

input
5, 5
output
False
input
5, 6
output
True
input
-5, 
output
 True
input
5, 4
output
False

Q26 Write a function that returns True if an integer is greater than or equal to another integer, and False otherwise.

def is_greater_or_equal(a, b):
    return a >= b

input
5, 5
output
True
input
5, 6
output
False
input
-5, 
output
 False
input
5, 4
output
True

Q27 Write a function to check if a key is in a dictionary.

def is_key_in_dict(d, key):
    return key in d
d = {'a': 1, 'b': 2}
input
d, 'a'
output
True
input
d, 'c'
output
False


Q28  Write a function to check if a value is in a dictionary.
def is_value_in_dict(d, value):
    return value in d.values()

d = {'a': 1, 'b': 2}
input
d, '1'
output
True
input
d, '3'
output
False


Q29 Write a function to get the value for a given key in a dictionary.

def get_value(d, key):
    return d[key]

d = {'a': 1, 'b': 2}
input
d, 'a'
output
1
input
d, 'c'
output
KeyError


Q30 Write a function to get the length of a dictionary.
Copy code
def dict_length(d):
    return len(d)


input
d = {'a': 1, 'b': 2}
output
2
input
d = {'a': 1, 'b': 2,'c':3}
output
3
