# FirstRepository
What happend?!
#include <iostream>
#include <math.h>
using namespace std;
double func(double c);
double X_Dich(double a, double b, double eps){
double x;
if (func(a)*func(b)>0.0) cout<<"error";
else x = 0.5 * (a+b);
if (abs(func(x)) > eps){
if(func(a)*func(x)<0.0)
return X_Dich(a,x,eps);
} 
}
double func(double c){
return pow(c,3)-(2*c)-5;
}
int main(){
int a,b,eps;
cin>>a>>b>>eps;
cout<<X_Dich(a,b,eps);
return 0;
}
