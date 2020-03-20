#include<iostream>
#include<cmath>
using namespace std;
float fun1(float a);
main()
{
	float power,base=0,x;
	float i,j;
	float store1,store2,store3,store4;
	cout<<"enter the value of x in (1+x) "<<endl;
	cin>>x;
	cout<<"Enter the upto to whihch term you want to find the binomial expension"<<endl;
	cin>>power;
	j=power;
	while(power>=base){
		
		float remainder;
		store1=fun1(power);
		i=pow(x,j);
float sum;
store2=fun1(base);
	store3=power-base;
	store4=fun1(store3);
	remainder=store1/(store2*store4);
	remainder=remainder*i;
	cout<<remainder;
	sum=sum+remainder;
	if(power>base)
	cout<<'+';
	else
	cout<<'='<<sum;
		base++;
		j--;
		}
		}
float fun1(float a)
{ 	 	
if(a>1)
return (a*fun1(a-1));
else if(a==1||a==0)
return 1;
}
