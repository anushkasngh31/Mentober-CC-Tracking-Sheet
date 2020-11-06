# Mentober-CC-Tracking-Sheet
/* question link: https://www.codechef.com/problems/CVDRUN */
#include <iostream>
using namespace std;

int main() {
	// your code goes here
int t; 
cin>>t; 
while(t--)
{
    int n,k,x,y,flag=0; 
    cin>>n>>k>>x>>y; 
    if(y>n)
    cout<<"NO"<<endl; 
    else
    {
        for(int i=0;i<n;i++)
        {
            if((x+k*i)%n== y)
            {
            cout<<"YES"<<endl;
            flag= 1; 
            break; 
            }
        }
        if(!flag)
        cout<<"NO"<<endl; 
    }
}
	    
	
	return 0;
}
