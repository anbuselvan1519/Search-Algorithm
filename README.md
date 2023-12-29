# Linear Search and Binary search
### Name: Anbuselvan.S
### Reference No: 23005959
## Aim:
To write a program to perform linear search and binary search using python programming.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
## Linear Search:
1.	Start from the leftmost element of array[] and compare k with each element of array[] one by one.
2.	If k matches with an element in array[] , return the index.
3.	If k doesn’t match with any of elements in array[], return -1 or element not found.
## Binary Search:
1.	Set two pointers low and high at the lowest and the highest positions respectively.
2.	Find the middle element mid of the array ie. arr[(low + high)/2]
3.	If x == mid, then return mid.Else, compare the element to be searched with m.
4.	If x > mid, compare x with the middle element of the elements on the right side of mid. This is done by setting low to low = mid + 1.
5.	Else, compare x with the middle element of the elements on the left side of mid. This is done by setting high to high = mid - 1.
6.	Repeat steps 2 to 5 until low meets high
## Program:
i)	#Use a linear search method to match the item in a list.
```
#Program for linear search method to match the item in a list
#Developed by:Anbuselvan.S
#RegisterNumber: 23005959
def linearSearch(array,n,k):
    s=array.sort()
    for i in range(0,n):
        if k==array[i]:
            return i
             
array = eval(input())
k = eval(input())
n=len(array)
result = linearSearch(array,n,k)
print(sorted(array))
if result==None:
    print("Element not found")
else:    
    print("Element found at index: ",result)
```
ii)	# Find the element in a list using Binary Search(Iterative Method).
``` 
Program to find the element in a list using Binary Search(Iterative Method)..
Developed by:Anbuselvan.S
RegisterNumber: 23005959

def binarySearchIter(array, k, low, high):
    while low<=high:
        mid = low +(high-low)//2
        if array[mid] ==k:
            return mid
        elif array[mid]<k:
            low=mid+1
        else:
            high=mid-1
    return -1           
    
array = eval(input())
array.sort()
k = eval(input()) 
result=binarySearchIter(array, k, 0, len(array)-1)
if result==-1:
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)
```
iii)	# Find the element in a list using Binary Search (recursive Method).
```
Program to find the element in a list using Binary Search(Iterative Method)..
Developed by:Anbuselvan.S
RegisterNumber: 23005959

def binarySearch(array, k, low, high):
    if high>=low:
        mid = low +(high-low)//2
        if array[mid] ==k:
            return mid
        elif array[mid]>k:
            return binarySearch(array, k, low, mid-1) 
        else:
            return binarySearch(array, k, mid+1, high) 
    else:        
        return -1           
    
array = eval(input())
array.sort()
k = eval(input()) 
result=binarySearch(array, k, 0, len(array)-1)
if result==-1:
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)
```
## Sample Input and Output
![image](https://github.com/anbuselvan1519/Search-Algorithm/assets/139841744/47cd779d-cfa3-48ea-b62d-456bb0480acd)
![image](https://github.com/anbuselvan1519/Search-Algorithm/assets/139841744/e2804068-ded4-4fb9-97d6-d168afa883d8)
![image](https://github.com/anbuselvan1519/Search-Algorithm/assets/139841744/59f74643-eea3-4bec-afcb-4a9a95eff095)
![image](https://github.com/anbuselvan1519/Search-Algorithm/assets/139841744/a90ff281-27d1-4c2b-905c-340a442239f3)
![image](https://github.com/anbuselvan1519/Search-Algorithm/assets/139841744/b262292a-5578-4a03-97a2-1d5e26a939b7)
![image](https://github.com/anbuselvan1519/Search-Algorithm/assets/139841744/6f644b19-cc73-4bf2-b343-c31204379c5f)

## Result
Thus the linear search and binary search algorithm is implemented using python programming.
