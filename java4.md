# **Pointeret**

Cdo variabel ne c++ ka 1 adrese te caktuar ku ruhet .
Per mi perdor ato adresa ne perdorim variablat e quajtura pointer qe jepin adresen e variables

*Shembull:* 
```cpp
#include <iostream>
using namespace std;
int main()
{
	int a = 5;
	int *p; // pointerat e kane shenjen yll te lloji i tipit(int* p) ose emri (int *p)
	 p = &a; // me shenjen & marim adresen e a dhe ja japim pointerit.
	cout << " Vlera e a:" << a << endl;
	cout << "Adresa e a:" << p << endl;


 return 0 ;
}
```
Shenja yll perveq qe perdoret per te treguar pointer perdoret edhe per te mare vleren ne ate adrese specifike (dereferencim )
 
 *Shembull:*
 ```cpp
 #include <iostream>
 using namespace std;
 int main() {

     int a=2 ;
     int *p;
     p=&a;
     cout << " vlera e a:" << *p << endl; // do te jep rezultatin a=2
     return 0;
 }
``` 

## Detyra 1 

Te deklarohet nje variabel me nje vlere te cfaredoshme dhe nje pointer. Permes pointerit, ta marrim adresen
e variables dhe permes pointerit, duke e ditur adresen e variables, t'ia ndryshojme vleren.

```cpp
#include <iostream>
using namespace std;
int main()
{
    int r = 10;
    cout << "Vlera e variables r eshte:" << r << endl;
    int *a;
    a = &r;
    cout << "Adresa e variables r eshte:" << a << endl;
    *a = 50;
    cout << "Vlera e variables r pas caktimit te vleres:" << *a << endl;
    cout << "Vlera e variables r pas caktimit te vleres:" << r << endl;
    //sic po e shohim *a=r 
    return 0;
}
```
## Detyra 2

Te shkruhet programi permes te cilit jepim vlera per dy variabla (x dhe y). Nese x > y, te njesohet shuma e tyre
kurse per kushte tjera le te njesohet ndryshimi i tyre.

```cpp
#include <iostream>
using namespace std;
int main()
{
    int x, y, z;
    cout << "Jep vleren per variablen x:";
    cin >> x;
    cout << "Jep vleren per variablen y:";
    cin >> y;
    if (x > y)
    {
        z = x + y;
        cout << x << "+" << y << "=" << z << endl;
    }
    else
    {
        z = x - y;
        cout << x << "-" << y << "=" << z << endl;
    }
    return 0;
}
```

## Detyra 3
Ngjashem sikur detyra e dyte, por programi te shkruhet permes pointereve.
```cpp
#include <iostream>
using namespace std;
int main()
{
    int x, y, z;
    int *a, *b;
    cout << "Jep vleren per variablen x:";
    cin >> x;
    cout << "Jep vleren per variablen y:";
    cin >> y;
    a = &x;
    b = &y;
    if (x > y)
    {
        z = *a + *b;
        cout << *a << "+" << *b << "=" << z << endl;
    }
    else
    {
        z = x - y;
        cout << *a << "-" << *b << "=" << z << endl;
    }
    return 0;
}
```

## Detyra 4 
Te shkruhet programi i cili tregon se a jane dy pointere te barabarte apo jo.
 
 
 Te dy pointeret te marrin te njejten adrese
```cpp
#include <iostream>
using namespace std;
int main()
{
 int r=10;
 int *a,*b;
 a=&r;
 b=a;
if (a==b)
cout << "Pointeret jane te barabarte." << endl;
else 
cout << "Pointeret nuk jane te barabarte." << endl;

}
```

## Detyra 5 

Te shkruhet programi i cili ka funksionin *llogaritja()* i cili merr nje pointer te tipit int dhe kthen rezultatin ne double
Te llogaritet : y=*a+3

```cpp
#include <iostream>
using namespace std;

double llogaritja (int *a)
{
    double y=0;
    y=*a+3;
    return y;
}
int main ()
{
    int r;
    cout << "Te jepet vlera per var. r:";
    cin >> r;
    cout << "Vlera e y=" << llogaritja(&r) << endl;
}
```
## Detyra 6
Kerkesa e ngjashme me detyren paraprake, por tani funksioni merr nje variabel te tipit double, ndersa ne main 
te deklarohet nje variabel dhe t'i jepet vlere e cfaredoshme, pastaj nje pointer i cili merr adresen e saj dhe perdoret
ne funksionin llogaritja.

```cpp
#include <iostream>
using namespace std;

double llogaritja (int a)
{
    double y=0;
    y=a+3;
    return y;
}
int main ()
{
    int r;
    int *z;
    cout << "Te jepet vlera per var. r:";
    cin >> r;
    z=&r;
    cout << "Vlera e y=" << llogaritja(*z) << endl;
}
```
## Detyra 7 

Detyre e ngjashme me detyren 6 por me sintakse te cpp te ndryshme. 

```cpp
#include <iostream>
using namespace std;

void llogaritja (double *a)
{
    double y=0;
    y=*a+3;
    cout << "y=" << y << endl;
}
int main ()
{
    void(*r)(double *a);
    r=llogaritja;
    double x;
    cout << "Jepni vleren e variables x:";
    cin >> x;
    (*r)(&x);
    cout << endl;
    return 0;
}
```
