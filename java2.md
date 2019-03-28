# **Vazhdim i klasave** 

## Detyra 1 
LLogariteni funksionin ne foto .

[Funksioni](https://imgur.com/a/ur9njiF)

Ku variablat n , a dhe x jane private dhe te tipit double 
Per zgjedhjen e funksionit perdor  funksionet publike : 

vendosvleren() qe i jep vlerat variablave private,

 shuma() qe gjen shumen e (2*i+a) prej 1 deri ne n+1 

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
---
## Detyra 2 
LLogariteni funksionin z= (m+1)!+3*a


Variablat private jane **m** , **a**  , dhe funksioni **faktoriel()** qe cakton vleren e (m+1)!.

Variablat publike jane:

 funksioni **vlerat()** qe cakton vleren e  variables **m** dhe **a**

 dhe funksioni **zet()** qe kalkulon funksionin.



```cpp
#include <iostream>
using namespace std;
class alfa{
    private:
    double m;
    double a;
    double faktoriel() {
        double P=1;
        for(int i=1;i<=m+1;i++)
        {P=P*i;}
        return P ;
    }
    public:
    void vlerat(double k , double x ){
        m=k;
        a=x;
    }
void zet(){
    double z;
    z=faktoriel() + 3 *a ;
    cout << z << endl ;
}

};

int main () {
    alfa zgjidhja;
    zgjidhja.vlerat(1,2); 
    zgjidhja.zet();
    return 0 ;
}

```
---
## Detyra 3
Krijoini nje klase me emrin person qe ka 3 variable publike (emri,mbiemri , qyteti ) te llojit string.
Krijoni nje funksion qe i shtyp ato vlera 

 Vlerat e funksionit mund te jepen me nje funksion apo objektet e personit te inicializohen ne main.
 Ketu jane dy menyrat ku menyra e pare eshte me incializimin ne int main()
```cpp
#include <iostream>
#include <string>
using namespace std; 
class person       
{public: // ska variabla private 
string emri ;
string mbiemri ;
string qyteti ;
void shtypobjektin(){
    cout << "Emri:" << emri << endl ;
    cout << "Mbiemri:" << mbiemri << endl ;
    cout << "Qyteti:" << qyteti << endl ;
    cout << endl << endl ;  
}
};
int main () 
{
    person studenti1={"Art","Ahmetaj","Prishtine"};
    person studenti2={"Rinor","Ahmeti","Prishtine"};
    studenti1.shtypobjektin();
    studenti2.shtypobjektin();

return 0;

}
```
---

## Detyra 3 ( Metoda 2 )
```cpp
#include <iostream>
#include <string>
using namespace std; 
class person       
{public: // ska variabla private 
string emri ;
string mbiemri ;
string qyteti ;
void shtypobjektin(){
    cout << "Emri:" << emri << endl ;
    cout << "Mbiemri:" << mbiemri << endl ;
    cout << "Qyteti:" << qyteti << endl ;
    cout << endl << endl ;  
}
void caktovlerat()
{
    cout << "Cakto Emrin :" ; 
    cin >> emri ;
    cout <<"Cakto Mbiemrin:";
    cin >> mbiemri ;
    cout << "Cakto Qytetin:";
    cin >> qyteti ;
    cout << endl << endl ; 

}
};
int main () 
{
    person studenti1;
    person studenti2;
    studenti1.caktovlerat();
    studenti2.caktovlerat();
    studenti1.shtypobjektin();
    studenti2.shtypobjektin();

return 0;

}
```
