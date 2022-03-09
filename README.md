# Codeforcescpp-160A
#include<bits/stdc++.h>
 
using namespace std;
 
int main(){
  int n;
  cin >> n;
  int arr[101];
  for(int i=0;i<n;i++){
    cin >> arr[i];
  }
 
  sort(arr,arr+n, greater<int>());
 
  int sum = 0;
 
  for(int i=0;i<n;i++){
    sum+=arr[i];
  }
 
  int add = 0;
  int count = 0;
 
  for(int i=0;i<n;i++){
    add+=arr[i];
    count++;
    if(add>sum/2){
      break;
    }
  }
  cout << count;
  return 0;
}
