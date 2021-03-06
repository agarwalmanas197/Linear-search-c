# Linear Search
## Problem: Given an array arr[] of n elements, write a function to search a given element x in arr[].

### Examples :
```
Input : arr[] = {10, 20, 80, 30, 60, 50, 
                     110, 100, 130, 170}
          x = 110;
```

### Output : 
```
6
```
Element x is present at index 6
```
Input : arr[] = {10, 20, 80, 30, 60, 50, 
                     110, 100, 130, 170}
           x = 175;
           
 ```
### Output :
```
-1
```
Element x is not present in arr[].

A simple approach is to do linear search, i.e

Start from the leftmost element of arr[] and one by one compare x with each element of arr[]
If x matches with an element, return the index.
If x doesn’t match with any of elements, return -1.

// C code to linearly search x in arr[]. If x 
// is present then return its location, otherwise 
// return -1 

```  
#include <stdio.h> 

  

int search(int arr[], int n, int x) 
{ 

    int i; 

    for (i = 0; i < n; i++) 

        if (arr[i] == x) 

            return i; 

    return -1; 
} 

  

int main(void) 
{ 

    int arr[] = { 2, 3, 4, 10, 40 }; 

    int x = 10; 

    int n = sizeof(arr) / sizeof(arr[0]); 

    int result = search(arr, n, x); 

    (result == -1) ? printf("Element is not present in array") 

                   : printf("Element is present at index %d", 

                            result); 

    return 0; 
}
```

### Output:
```
Element is present at index 3
The time complexity of above algorithm is O(n).
```

Linear search is rarely used practically because other search algorithms such as the binary search algorithm and hash tables allow significantly faster searching comparison to Linear search.
