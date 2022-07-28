# Binary-Search-C-
#include<iostream>
using namespace std;

int BinarySer(int arr[],int n,int key)
{
	int s=0;
	int e=n;
	while(s<=e){
		int mid=(s+e)/2;
		if(arr[mid]==key)
		{
			return mid;
		}
		else if(mid>key)
		{
			e=mid-1;
		}
		else
		{
			s=mid+1;
		}
		
	}
	
}


int main()
{
	
	int n;
	cout<<"enter n"<<endl;
	cin>>n;
	int arr[n];
	for(int i=0;i<n;i++)
	{
		cin>>arr[i];
	}
	int key;
	cout<<"enter search key"<<endl;
	cin>>key;
	cout<<BinarySer(arr,n,key);
//	cout<<BinarySer(arr,n,key);
}
