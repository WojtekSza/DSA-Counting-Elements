# DSA-Counting-Elements
Given an integer array arr, count how many elements x there are, such that x + 1 is also in arr. If there are duplicates in arr, count them separately.
```
Input: arr = [1,1,3,3,5,5,7,7]
Output: 0
Explanation: No numbers are counted, cause there is no 2, 4, 6, or 8 in arr.
```
```
class Solution:
    def countElements(self, arr: List[int]) -> int:
        ans=0
        #Creation of set will cost space complexity O(n) and time compleixty O(n). Withou that iteration thru list will cost O(1) for space complexity and O(n2) time complixity, due to cost of nested linear search thru list elements
        #Threfore better time complexity will be achived with HashSet approach
        has_set=set(arr)
        for i in arr:
            #iterration thur element will cost O(n) time compleixty, check if element is in HasSet cost O(1) time complexity. Threfore total O(n) + N*O(1) = O(N) +O(N) = O(N)
            if i+1 in has_set:
                ans+=1
        return ans
```
Time complexity O(n)
Space complexitu O(n)
