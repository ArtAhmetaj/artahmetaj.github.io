# **Klasa dhe Konstruktori**

## Detyra 1

Te shkruhet programi qe ka klasen "Person" dhe kjo klase te kete kete keto variabla:


string emri


string mbiemri


string qyteti.


Ne funksionin main te krijohet nje vektor me objekte te tipit Person, i cili i merr te dhenat e perdoruesve(vektor) dhe pastaj i shfaqe ato.
```cpp
#include <iostream>
#include <string>
using namespace std;
class Person {
public:
    string emri, mbiemri, qyteti;
};
int main()
{
    const int n = 2;
    Person studentet[n];
    for (int i = 0; i < n; i++) {
        cout << "Emri:";
        cin >> studentet[i].emri;
        cout << "Mbiemri:";
        cin >> studentet[i].mbiemri;
        cout << "Qyteti:";
        cin >> studentet[i].qyteti;
    }
    for (int i = 0; i < n; i++)
    {
        cout << " Emri  ";
        cout << studentet[i].emri<< endl;
        cout << "Mbiemri";
        cout << studentet[i].mbiemri<< endl;
        cout << "Qyteti" ;
        cout << studentet[i].qyteti<< endl;
    }
    return 0;
} 
```
## Detyra 2
Te shkruhet programi i cili e permbane klasen omega, e kjo klase te kete variablat private n dhe k te tipit int, x dhe a te tipit double ndersa te kete variablen y te tipit double e cila eshte publike.

 Permes konstruktorit te llogaritet shprehja:  y = 3 * x + k * s.

```cpp
#include <iostream>
using namespace std;
class omega {
private:
    int n, k;
    double x, a;
public:
    double y;
    omega()
    {
        cout << "Jepni vleren e n:" << endl;
        cin >> n;
        cout << "Jepni vleren e k:" << endl;
        cin >> k;
        cout << "Jepni vleren e x:" << endl;
        cin >> x;
        cout << "Jepe vleren e a" << endl;
        cin >> a;
        double s = 0;
        for (int i = 1; i <= n + 1; i++) {
            s = s + (2*i+a);
        }
        y = 3 * x + k * s;

    }
};
int main() {
    omega a1;
    cout << "y=" << a1.y;
}
```
## Detyra 3 
Te shkruhet programi i cili permbane klasen kater, e kjo klase te kete kater variabla private te tipit double. 

Poashtu, le te krijohet metoda(funksioni) permes te cilit i japim vlera variablave a dhe b, metoda llogaritja permes te cilit e llogarisim syprinen dhe perimetrin e katerkendeshit dhe metoda shtypja e cila i shtype ato.

```cpp 
#include <iostream>
using namespace std;
class kater
{
private:
    double a, b, s, p;
public:
    kater(double _a, double _b)
    {
        a = _a;
        b = _b;
    }
    void llogaritja()
    {
        s = a * b;
        p = 2 * (a + b);
    }
    void shtypja()
    {
        cout << "Syprina e katerkendeshit:" << s << endl;
        cout << "Perimetri i katerkendeshit:" << p << endl;
    } 
};
int main()
{

    kater pes(3,4);
    pes.llogaritja();
    pes.shtypja();
    return 0;
}
```
## Detyra 4 
Te shkruhet programi i cili ka klasen rrethi, klase e cila i ka 4 variabla private te tipit double: Pi,r,s,p.

 Poashtu, te deklarohet konstruktori permes te cilit e caktojme vleren e Pi, metoda rrezja permes se ciles i japim vlere rrezes, metoda llogaritja e cila e llogarite syprinen dhe perimetrin e rrethit dhe ne fund metoda shtypja e cila i shtype ato.

```cpp
#include <iostream>
using namespace std;
class rrethi {
private:
    double Pi, r, s, p;
public:
    rrethi();
    void rrezja(double x);
    void llogaritja();
    void shtypja();
};
rrethi::rrethi()
{

        Pi = 3.1415;

}
void rrethi::rrezja(double x) {
    r = x;
}
void rrethi::llogaritja() {
    s = Pi * r * r;
    p = 2 * Pi * r;
}
void rrethi::shtypja() {
    cout << "Syprina=" << s << endl;
    cout << "Perimetri=" << p << endl;
}
int main()
{
    rrethi a;
    double x;
    cout << "Jepni vleren e rrezes:";
    cin >> x;
    a.rrezja(x);
    a.llogaritja();
    a.shtypja();
    return 0;
}
```
## Detyra 5 
Te krijohet nje klase me emrin beta, qe ka variablat publike:

*int n*


*double A[m]*

dhe nje funksion me double max() qe kalkulon vleren maksimale te vektorit ne fjale A[m]


m ka cleren konstante 10, kurse int n perdoret per te treguar se sa vlera te vektorit jane te mbushura dhe inicializohet ne vektorin main 
```cpp
#include <iostream>
#include <string>
using namespace std;
const int m=10;
class beta
{
public:
int n ;
double A[m];
double max()
{
 double max=A[0];
 for(int i=1;i<n;i++)
{    
    if(A[i]>max) max=A[i];
}
return max;
}
};

int main()
{
    beta objBeta ={5,2.1,-7.5,12.4,3.1,10.15};
    cout << "Vlera max:  " << objBeta.max() << endl ;
    return 0;
}