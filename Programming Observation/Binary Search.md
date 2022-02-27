# Q1 Peak Index In Mountain Array
- At least 3 elements are required to find out the peak in the mountain
- Again if i is the peak element then `0 < i < arr.length`
- As minimum 3 elements are required so mid + 1 always exist in the array but not mid - 1
```java
static int peak2(int[] arr) {  
    int start = 0;  
 int end = arr.length - 1;  
 while(start<end)  
    {  
        int mid = start + (end-start)/2;  
  
 if(arr[mid] > arr[mid + 1])  
        {  
            end = mid;  
 }  
        else  
 {  
            start = mid + 1;  
 }  
    }  
  
    return start;  
}
```
# Q2 Smallest Letter Greater Than Target
- Here we don't have to check that the mid is equal to the target or not, `why?` because we don't have to return the target element index that's why
- We have to just increase the start and decrease the end and when these two will cross each other then we have to just return the start
# Q3 First & Last Occurrences
- We just have to take two different variables to store first and last occurrences
- But the important thing is optimization of code, `how can we derive in less line of codes?` so the main thing is when we deriving the mid and if the mid is same as the target element then we just have to update the value of first and last , so if first we update the program and decrement the end to mid - 1 and if last then first = mid + 1, that's it