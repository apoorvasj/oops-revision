<h1>Abstraction (Data hiding) </h1>
<p>Abstraction can be understood as a separation of implementation and interface. We only need to know, how to interact with this interface.</p>


```cpp
#include <iostream>
using namespace std;

class Student{
    string name;
    int roll_num;
    
    public:
    void getName(string n,int rn){
        name=n;
        roll_num=rn;

    }

    void printDetails(){
        cout<<"Welcome, student "<<name;
        cout<<"\nYour roll number is"<<roll_num;
    }

};

int main(){
    Student stu1;
    stu1.getName("Ram",22);
    stu1.printDetails();
    stu1.name="Ram" //ERROR

}
```
<p>We only need to understand what member functions are available, what parameters they can take and what values they are capable of returning. In this student class, trying to directly access the name variable would throw an error.</p>
<blockquote>Encapsulated classes implement data hiding.</blockquote>

```java
abstract class Teacher{
public abstract void name();
public void greeting(){
System.out.println("Hi, I am a Teacher.");
}
}

//derived class needs to inherit the base class. An abstract class cant be used directly, its objects cannot be created directly.

class Student extends Teacher{
public void name(){
System.out.println("Hi, I am a student.");
}
}

//method is declared in the abstract class above but definition is only in the derived class.

public class Main{
public static void main(String[]args){
Student stu= new Student();
stu.name();
stu.greeting();
}
}
```
<a href="https://www.w3schools.com/java/java_abstract.asp">Source</a>
