# **Klasat**





## **Detyra 1**
 Krijoni nje klase me nje variabel private me emrin rrezja, dy funksione publike ku nje funksion percakton vleren e rrezes dhe tjetri funksion llogarit siperfaqen.
 Funksionet duhet te inicializohen jashte klases .
```c++
#include <iostream>
using namespace std;
#define PI 3.14
class Rrethi
{
private:
	int rrezja;
public:
	void vendos_rrezen(double r);
	double siperfaqja()

};
void Rrethi::vendos_rrezen(double r)
{
	rrezja = r;
}
double Rrethi::siperfaqja()
{
	return PI * rrezja * rrezja;

}
int main()
{
	Rrethi objRrethi;
	objRrethi.vendos_rrezen(4.5);
	cout << "siperfaqja e rrethit: "
		<< objRrethi.siperfaqja();

	return 0;

}

 ```

---
## **Detyra 2**
 Krijoni nje klase me emrin Person e cila permbane variablat publike: emri,mbiemri,qyteti dhe VitiLindjes. Poashtu, kjo klase le te permbaje edhe dy funksione te llojit void, te cilat marrin te dhenat permes tastieres dhe pastaj i shfaqin ato.
```c++
#include <iostream>
using namespace std;
#include string
class Person
{
public:
	string emri;
	string mbiemri;
	string qyteti;
	int VitiLindjes;
    void MerrTeDhenat()
    {
	cout << "jepni emrin e studentit:";
	cin >> emri;
	cout << "jepni mbiemrin e studentit:";
	cin >> mbiemri;
	cout << "jepni qytetin e studentit:";
	cin >> qyteti;
	cout << "jepni vitin e lindjes se studentit:";
	cin >> VitiLindjes;
	cout << endl << endl;
    }
    void ShfaqTeDhenat()
    {
	cout << "Te dhenat e lexuara" << endl;
	cout << emri << endl;
	cout << mbiemri << endl;
	cout << qyteti << endl;
	cout << VitiLindjes << endl;
    }
};
int main()
{
	Person studenti;
    	studenti.MerrTeDhenat();
    	studenti.ShfaqTeDhenat();
	return 0;

}
```
---
##  **Detyra 2 - menyra tjeter**
```c++

#include <iostream>
using namespace std;
class Person
{
public:
	char emri[20];
	char mbiemri[20];
	char qyteti[20];
	int VitiLindjes;
};
int main()
{
	Person studenti;
	cout << "jepni emrin e studentit:";
	cin >> studenti.emri;
	cout << "jepni mbiemrin e studentit:";
	cin >> studenti.mbiemri;
	cout << "jepni qytetin e studentit:";
	cin >> studenti.qyteti;
	cout << "jepni vitin e lindjes se studentit:";
	cin >> studenti.VitiLindjes;
	cout << endl << endl;

	cout << "Te dhenat e lexuara" << endl;
	cout << studenti.emri << endl;
	cout << studenti.mbiemri << endl;
	cout << studenti.qyteti << endl;
	cout << studenti.VitiLindjes << endl;
	return 0;

}
```
---
## Detyra 3 
 Te shkruhet Seria Fibonacci permes klasave !
```c++
#include <iostream>
using namespace std;
class Fibonacci
{
  public:
    int a, b, c;
    void Fibo(int n)
    {
        int a = 0, b = 1;
        for (int i = 0; i < n; i++)
        {
            if (i == 0)
            {
                cout << a;
                continue;
            }
            if (i == 1)
            {
                cout << " " << b;
                continue;
            }
            c = a + b;
            cout << " " << c;
            a = b;
            b = c;
        }
    }
};
int main()
{
    cout << "Jepni numrin e termave ne serine Fibonacci: ";
    int r;
    cin >> r;
    cout << r << " termat e serise Fibonacci jane:" << endl;
    Fibonacci fibonacci;
    fibonacci.Fibo(r);
    return 0;
}
```
---
## Detyra 4
Krijoni nje klase me emrin inicimi  me nje variabel private krijoni 2 funksione ku njeri percakton vleren e variables me ane te **cin** dhe funksioni tjeter e jep vleren e variables ne funksionin main me **cout**
```cpp
#include <iostream>
using namespace std;
class inicimi
{
private: int a;
public:
	void leximi();
	void shtypja();

};
void inicimi::leximi()
{
	cout << "jepni vleren e var. a= ";
	cin >> a;
}
void inicimi::shtypja()
{
	cout << endl << "vlera e var. private a = "
		<< a;


}
int main()
{
	inicimi objInicimi;
	objInicimi.leximi();
	objInicimi.shtypja();
	cout << endl << endl;
	return 0;
}





















```

---
## Detyra 5
Krijoni nje klase katrori me nje variabel ( *int a* ) dhe nje variabel publike (*int b*) , me funksione publike vendosni vleren dhe paraqiteni ate ne funksionin int main 
```cpp
#include <iostream>
using namespace std;
class Katrori
{
private:
	int a;

public:
	int b;
	void vendos_vleren(int k)
	{
		a = k;
	}

	int lexo_vleren()
	{
		return a;
	}

};
int main()
{
	Katrori objKatrori;
	int x;
	cout << "jepni vleren e variables a =";
	cin >> x;
	cout << "jepni vleren e variables b =";
	cin >> objKatrori.b;
	cout << endl << endl;
	cout << "te dhenat e lexuara:" << endl;
	cout << "vlera e variables a = " << objKatrori.lexo_vleren()<<endl;
	cout << "vlera e variables b = " << objKatrori.b << endl;

	return 0;

}






























```
---
## Detyra 6
Detyra le te jete e ngjashme me detyren e 4 por inicimi i vlerave te mos behet me **cin** por direkt te funksioni int main 
Kuptohet qe per kete rast te gjitha variablat jane publike
Per kete detyre kemi variablet x,y,z ku z eshte variabel double.
```cpp
#include <iostream>
using namespace std;
class inicimi_direkt
{

public:
	int x;
	double y, z;
	void shtypja()
	{
		cout << "x= " << x << endl;
		cout << "y= " << y << endl;
		cout << "z= " << z << endl;
	}
	

};
int main()
{
	inicimi_direkt objID = { 3,1.4,5.6 };
	objID.shtypja();
	return 0;
}
































```