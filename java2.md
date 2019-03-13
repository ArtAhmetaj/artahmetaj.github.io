# **Vazhdim i klasave** 
## Detyra 1 
LLogariteni funksionin ne foto .

[Funksioni](https://imgur.com/a/ur9njiF)

Ku variablat n , a dhe x jane private dhe te tipit double 
Per zgjedhjen e funksionit perdor  funksionet publike : 

vendosvleren() qe i jep vlerat variablave private,

 shuma() qe gjen shumene e (2*i+a) prej 1 deri ne n+1 

 dhe funksionig() qe e gjen dhe kthen vleren.
 
 ```cpp
#include <iostream>
using namespace std;

class llogaritja
{
    private:
    double n ,a , x; 
    public:
    double shuma() 
    {
        double shuma =0;
        for(int i=1;i<n+1;i++)
        {shuma=shuma+(2*i+a);
        }
        return shuma ;
    }
void vendosvleren(double c,double d, double e)
{  n=c;
    a=d;
    x=e;
}
void funksionig() {
    int g ;
    g=3*x+4*shuma();
    cout << g << endl ;
}
};
int main() { 
    llogaritja funksioni;
    funksioni.vendosvleren(1,2,3);
    funksioni.funksionig();
}
```
## Detyra 2 


