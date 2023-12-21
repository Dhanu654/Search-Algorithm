# Linear Search and Binary search
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
### Program:
i)	#Use a linear search method to match the item in a list.
```
Program for linear search method to match the item in a list
Developed by:DHANUSYA.K
RegisterNumber: 23006651
'''
def linearSearch(array,n,k):
    for i in range(0,n):
        if(array[i]==k):
            return i
    return -1
    
array = eval(input())
k = eval(input()) 
n=len(array)
array.sort()
result = linearSearch(array,n,k)
if(result == -1):
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)


```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```
Program to find the element in a list using Binary Search(Iterative Method)..
Developed by: DHANUSYA.K
RegisterNumber: 23006651
'''
def binarySearchIter(array, k, low, high):
    while low<=high:
        mid = low+(high-low)//2
        if array[mid]==k:
            return mid
        elif array[mid] <k:
            low = mid+1
        else:
            high = mid-1
    return-1
    
    
array = eval(input())
array.sort()
k = eval(input())
result = binarySearchIter(array,k,0,len(array)-1)
if (result==-1):
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)





```
iii)	# Find the element in a list using Binary Search (recursive Method).
```
Program to find the element in a list using Binary Search (recursive Method).
Developed by: DHANUSYA.K
RegisterNumber: 23006651
'''
def binarysearch(array, k, low, high):
    while low<=high:
        mid=(low+high)//2
        if array [mid]==k:
            return mid
        elif array [mid]<k:
            low=mid+1
        else:
            high=mid-1
    return -1
    
array = eval(input())
array.sort()
k = eval(input()) 
result=binarysearch(array,k,0,len(array)-1)
print(array)
if result!=-1:
    print(f"Element found at index:  {result}")
else:
    print(f"Element not found ")




```
## Sample Input and Output

![Screenshot 2023-12-21 105852](https://github.com/Dhanu654/Search-Algorithm/assets/148514965/14ec65bb-abbb-4d34-a703-37a1f76d89ae)
![Screenshot 2023-12-21 110026](https://github.com/Dhanu654/Search-Algorithm/assets/148514965/a02d7996-fe95-42f4-a7a6-b2771e82283f)
![Screenshot 2023-12-21 110250](https://github.com/Dhanu654/Search-Algorithm/assets/148514965/c33aaac3-ec4c-4b94-b704-21b7b09db272)







## Result
Thus the linear search and binary search algorithm is implemented using python programming.
