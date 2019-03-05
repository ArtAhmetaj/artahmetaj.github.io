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