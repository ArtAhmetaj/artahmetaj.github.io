# **Klasat**





## **Detyra 1**
### Krijoni nje klase me nje variabel private me emrin rrezja, dhe nje variabel publike me emer te cfaredoshem. Me funksione merni vleren private dhe perdoreni per te percaktuar vleren e syprines se rrethit.
```c++
#include <iostream>
using namespace std;

class rrethi{
    private:
    int rrezja;
    public :
    int a;
   void jepevleren(int k){
   rrezja = k ;
   }
    int ktheje(){
        return rrezja ;
    }

};

int main() {
    rrethi obj1;
   
   obj1.jepevleren(3);
   
    int r=obj1.ktheje();
   
    cout << 3.14 * r * r   << endl ;
   
    return 0;
    }
 ```


## **Detyra 2**
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

## ** Detyra 2 (pa funksione dhe me char ne vend te string) ** 

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




