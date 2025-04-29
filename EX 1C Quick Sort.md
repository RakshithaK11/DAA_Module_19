# EX 1C Quick Sort
## DATE:
## AIM:
To write a python program to implement quick sort using tha last element as pivot on the list of float values.

## Algorithm
1.Choose a pivot (typically the last element of the array).
2.Partition the array around the pivot, placing elements smaller than the pivot on the left and larger on the right.
3.Recursively apply QuickSort to the left and right subarrays created by the partition.
4.Repeat partitioning until the subarrays have only one element (sorted).
5.Combine the sorted subarrays to get the final sorted array.
## Program:
~~~
Program to implement implement quick sort using the last element as pivot on the list of float values.
Developed by: RAKSHITHA K 
Register Number:212223110039

def partition(arr,low,high):
    i = ( low-1 )
    pivot = arr[high]
    for j in range(low , high):
        if arr[j] <= pivot:
            i = i+1
            arr[i],arr[j] = arr[j],arr[i]
    arr[i+1],arr[high] = arr[high],arr[i+1]
    return ( i+1 )
def quickSort(arr,low,high):
    if low < high:
        pi = partition(arr,low,high)
        quickSort(arr, low, pi-1)
        quickSort(arr, pi+1, high)
 # Driver code to test above 
arr = []
n = int(input())
for i in range(n):
    arr.append(input())
quickSort(arr,0,n-1)
print ("Sorted array is:")
for i in range(n):
    print ("%c" %arr[i])
~~~

## Output:
![image](https://github.com/user-attachments/assets/db56a68e-39c6-4d87-831a-75c2c4d8984c)

## Result:
The program successfully sorts the input array using the QuickSort algorithm, arranging the elements in ascending order.
