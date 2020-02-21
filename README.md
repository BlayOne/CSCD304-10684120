# CSCD304-Assginment

//LINEAR SEARCH USING DIVIDE AND CONQUER

#include <bits/stdc++.h> 
using namespace std; 
  
// Linearly search x in arr[].  If x is present then return its 
// location,  otherwise return -1 
int search(int arr[], int n, int x) 
{ 
    int i; 
    for (i = 0; i < n; i++) 
        if (arr[i] == x) 
            return i; 
    return -1; 
} 
  
// Driver code 
int main() 
{ 
    int arr[] = { 3, 4, 1, 7, 5 }; 
    int n = sizeof(arr) / sizeof(arr[0]); 
    int x = 4; 
  
    int index = search(arr, n, x); 
    if (index == -1) 
        cout << "Element is not present in the array"; 
    else
        cout << "Element found at position " << index; 
  
    return 0; 
} 



//BINARY SEARCH USING DIVIDE AND CONQUER
    #include<bits/stdc++.h>
      using namespace std;
       int Binary_search(int arr[],int l,int r, int key)
     
      {
           if(l<=r)
         {
             int mid = l+((r-l)/2);
             
             if(arr[mid]==key)
              return 1;
              
              else if(arr[mid]>key)
               return Binary_search(arr,l,mid-1,key);
               
               else
                 return Binary_search(arr,mid+1,r,key);
         }
         
         return 0;
     }
       int main()
     {
       int arr[]={3,4,5,6,7,8,4,5,2,8,9,13,14,17,19};
       
       int n=sizeof(arr)/sizeof(arr[0]);
       
        int key=79;
       
       sort(arr,arr+n);
       
        if(Binary_search(arr,0,n-1,key))
         cout<<"key is found in given array"<<endl;
         
         else
          cout<<"key is not found in given array"<<endl;
     }
