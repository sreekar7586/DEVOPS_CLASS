\#include <iostream>

\#include <iomanip>

using namespace std;



// Class1

class Class1 {

&#x20;   double radius;

public:

&#x20;   void setRadius(double r) {

&#x20;       this->radius = r;

&#x20;   }

&#x20;   double circumference() {

&#x20;       return 2 \* 3.14 \* radius;

&#x20;   }

};



// Class2

class Class2 {

&#x20;   double radius;

public:

&#x20;   void setRadius(double r) {

&#x20;       this->radius = r;

&#x20;   }

&#x20;   double circumference() {

&#x20;       return 23.14 \* radius;

&#x20;   }

};



int main() {

&#x20;   double radius;

&#x20;   cin >> radius;



&#x20;   Class1 obj1;

&#x20;   obj1.setRadius(radius);

&#x20;   double c1 = obj1.circumference();



&#x20;   Class2 obj2;

&#x20;   obj2.setRadius(radius);

&#x20;   double c2 = obj2.circumference();



&#x20;   cout << fixed << setprecision(2);

&#x20;   cout << "Class1 Output: " << c1 << endl;

&#x20;   cout << "Class2 Output: " << c2 << endl;



&#x20;   return 0;

}

