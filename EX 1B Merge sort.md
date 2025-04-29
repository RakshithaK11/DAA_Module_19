# EX 1B Merge Sort
## DATE:
## AIM:
To write a python program to sort the first half of the list using merge sort.

## Algorithm
1.Divide the array into two halves: left (arr[l..m]) and right (arr[m+1..r]).
2.Recursively sort the left and right halves by calling mergeSort.
3.Merge the two sorted halves using the merge function.
4.Compare elements from both halves and merge them in sorted order.
5.Handle remaining elements from either half if any exist and place them in the original array.
## Program:
~~~
Program to implement Merge Sort
Developed by: RAKSHITHA K
Register Number: 212223110039

def merge(arr, l, m, r):
    n1 = m - l + 1
    n2 = r - m
    L = [0] * (n1)
    R = [0] * (n2)
    for i in range(0, n1):
        L[i] = arr[l + i]
 
    for j in range(0, n2):
        R[j] = arr[m + 1 + j]
 
    i = 0     
    j = 0     
    k = l     
 
    while i < n1 and j < n2:
        if L[i] <= R[j]:
            arr[k] = L[i]
            i += 1
        else:
            arr[k] = R[j]
            j += 1
        k += 1
 
    # Copy the remaining elements of L[], if there
    # are any
    while i < n1:
        arr[k] = L[i]
        i += 1
        k += 1
 
    while j < n2:
        arr[k] = R[j]
        j += 1
        k += 1

def mergeSort(arr, l, r):
    if l < r:
        m = l+(r-l)//2
        mergeSort(arr, m+1, r)
        merge(arr, l, m, r)

arr =[]               
n =int(input())
for i in range(n):
    arr.append(float(input()))
print("Given array is")
for i in range(n):
    print("%.1f" % arr[i],end=" ")
 
mergeSort(arr, 0, n-1)
print("\n\nSorted array is")
for i in range(n):
    print("%.1f" % arr[i],end=" ")
~~~


## Output:
![image](https://github.com/user-attachments/assets/6d7cb64b-9cf6-4495-b0e2-43de4f9ddd33)

## Result:
The program successfully sorts the first half of the given array using merge sort. where only the first half is sorted, and the second half remains unchanged.
