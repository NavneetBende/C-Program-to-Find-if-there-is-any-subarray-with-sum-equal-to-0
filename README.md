Subarray with sum equal to 0 in C
Here, in this page we will discuss the program to find if there is any subarray with sum equal to 0 in C programming language. If such subarray is present then print true otherwise print false.

Subarray with sum equal to 0 in C
Algorithm:
Run a outer loop for index 0 to n.
Run a nested loop from index i+1 to n,
Find sum, if it is equal to 0, then print true.
Otherwise, print false.
Time and Space Complexity
Time Complexity : O(n2)
Space Complexity : O(1)
Example :
Input : [ 4, 2, -3, 1, 6 ]
Output : true
Explanation : There is a subarray with zero sum from index 1 to 3, {2+(-3)+1 = 0}
Run
#include<stdio.h>

int main(){
    int arr[] = {-3, 2, 3, 1, 6};
    int n = sizeof(arr)/sizeof(arr[0]);
    
    int flag = 0, sum;
    
    for(int i=0; i<n; i++){
      
        for(int j=i; j<n; j++){
            sum += arr[j];
            
            if(sum==0){
                flag =1;
                break;
            }
        }
    }
    
    if(flag==1)
    printf("true");
    
    else printf("false");
    
}
Output
false
