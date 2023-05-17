# Programming_Assingment-11


1. Write a Python program to find words which are greater than given length k?
sol:
def task1(list_of_words: list, k: int):
    output = []
    for i in list_of_words:
        if len(i) > k:
            output.append(i)
            
    return output
list_of_words = ['Apple', 'bananana', 'kiwi', 'berry', 'almond']
k = 5

task1(list_of_words, k)
['bananana', 'almond']



2. Write a Python program for removing i-th character from a string?
sol:
def task2(string: str, i):
    string = string.replace(string[i], '')
    return string
task2('abcdefgh', 4)
'abcdfgh'



3. Write a Python program to split and join a string?
sol:
string = "Write a Python program to split and join a string?"

split = string.split(' ')
print(split)

join = " ".join(split)
print(join)
['Write', 'a', 'Python', 'program', 'to', 'split', 'and', 'join', 'a', 'string?']
Write a Python program to split and join a string?




4. Write a Python to check if a given string is binary string or not?
sol:
string = input("Enter the string: ")
binary = ['0', '1']

is_binary = True
for i in string:
    if i not in binary:
        is_binary = False
    
if is_binary:
    print("Binary")
else:
    print("Not Binary")
Enter the string: 101010100001
Binary
string = input("Enter the string: ")
binary = ['0', '1']

is_binary = True
for i in string:
    if i not in binary:
        is_binary = False
    
if is_binary:
    print("Binary")
else:
    print("Not Binary")
Enter the string: asdcqwe
Not Binary




5. Write a Python program to find uncommon words from two Strings?
sol:
def task5(string1, string2):
    
    string1 = string1.split(' ')
    string2 = string2.split(' ')
    uncommon = []
    
    for i in set(string1):
        if i not in string2:
            uncommon.append(i)

    for i in set(string2):
        if i not in string1:
            uncommon.append(i)
            
    return uncommon
string1 = "Write a Python program to split and join a string"
string2 = "Write a Python program to find uncommon words from two Strings"

task5(string1, string2)
['and',
 'join',
 'string',
 'split',
 'words',
 'find',
 'from',
 'Strings',
 'uncommon',
 'two']
 
 
 
 
6. Write a Python to find all duplicate characters in string?
sol:
def task6(string: str):
    duplicate = []
    for i in string:
        if string.count(i) > 1:
            duplicate.append(i)
            
    return set(duplicate)
task6("find all duplicate characters in string")
{' ', 'a', 'c', 'd', 'e', 'i', 'l', 'n', 'r', 's', 't'}



7. Write a Python Program to check if a string contains any special character?
sol:
import re


string = input("Enter a string: ")
regex = re.compile('[@_!#$%^&*()<>?/\|}{~:]')  

if(regex.search(string) == None):
    print("Given string does not contain special characters")
else:
    print("Given string contains special characters")
Enter a string: qwe*213(*(&
Given string contains special characters
import re


string = input("Enter a string: ")
regex = re.compile('[@_!#$%^&*()<>?/\|}{~:]')  

if(regex.search(string) == None):
    print("Given string does not contain special characters")
else:
    print("Given string contains special characters")
Enter a string: 12312312
Given string does not contain special characters
