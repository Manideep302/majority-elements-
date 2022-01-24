# majority-elements-
//Finding majority elements of an array using c++ code(static coding).
#include<iostream>
using namespace std;
int main(){
//    Method 1
    int n;
    cout<<"enter the size of the array ";
    cin>>n;
    int arr[n];
    cout<<"provide the elements of the array"<<endl;
    for(int i=0;i<n;i++)
    cin>>arr[i];
    int t=0;
    for(int i=0;i<n;i++){
        int count=0;
        for(int j=0;j<n;j++){
            if(arr[i]==arr[j])
            count++;
        }
        if(count>(n/2)){
            cout<<"the majority element preasent in the given array is ";
            t=1;
            cout<<arr[i]<<endl;
            break;
        }
    }
    if(t==0)
    cout<<"There is no majority element preasent in the provided array"<<endl;
   return 0;
}
