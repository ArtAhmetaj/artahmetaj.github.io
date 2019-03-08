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



