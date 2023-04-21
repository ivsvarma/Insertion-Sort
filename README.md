# Insertion-Sort
The main idea behind insertion sort is that it inserts each item into its proper place in the final list. To save memory, most implementations of the insertion sort algorithm work by moving the current data element past the already sorted values and repeatedly interchanging it with the preceding value until it is in its correct place.
#include<iostream>
using namespace std;
int main(){
    int i,a,j,n,temp;
    cout<<"enter no. pf elements";
    cin>>n;
    int arr[n];
    cout<<"etert the elements ";
    for(i=0;i<n;i++){
        cin>>arr[i];
    }
    for(i=1;i<n;i++){
        temp=arr[i];
        j=i-1;
        while(j>=0&&arr[j]>temp)
        {
            arr[j+1]=arr[j];
            j=j-1;
        }
        arr[j+1]=temp;
    }



cout<<"print the sorted arr\n";
for(i=0;i<n;i++)
cout<<arr[i]<<"\n";
 return 0;
} 
