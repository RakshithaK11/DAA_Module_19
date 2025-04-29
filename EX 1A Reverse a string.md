# EX 1A Reverse a String
## DATE:
## AIM:
To write a program to create a recursive function to reverse a string.

## Algorithm
1. Check if the string is empty 
2. If empty, return the string
3. If not empty, recursively call
4. Append the first character (n[0]) to the result of the recursive call.
5. Return the final reversed string.

## Program:
~~~
Program to implement Reverse a String

Developed by: RAKSHITHA K
Register Number:212223110039

n =input()
def rev(n):
    if len(n)==0:
        return n
    else:
        return rev(n[1:])+n[0] 
    
print(rev(n))
~~~
  


## Output:
![image](https://github.com/user-attachments/assets/9643a9c9-646e-43da-b21e-0ea2a697d2ad)



## Result:
The program successfully reverses the input string using recursion. When the user provides an input string, the output displays the reversed version of the string
