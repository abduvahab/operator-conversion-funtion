# operator-conversion-funtion
another usage of operator key word in c++. 

You can define a member function of a class, called a conversion function, that converts from the type of its class to another specified type.
Conversion function syntax

>>-+-----------+--operator--conversion_type--------------------->
   '-class--::-'                              

>--+----------------------+--(--)--+----------+----------------->
   | .------------------. |        +-const----+   
   | V                  | |        '-volatile-'   
   '---pointer_operator-+-'                       

>--+---------------------+-------------------------------------><
   '-{--function_body--}-'   

A conversion function that belongs to a class X specifies a conversion from the class type X to the type specified by the conversion_type. The following code fragment shows a conversion function called operator int():

operator className(){}

classNmae::operator typeName(){}

# example 
using namespace std;
- class X{

    private:
        int age;
        string name;
        
        
     public:
     
      X(int _age=0, string _name="person"):age(_age),name(_name){}
      
      operator int()const{return age;}
      
      operator char*()const{return name.c_str();}
      
  }
  
  int main(){
  
  
    X x;
    
    int a=x;
    
    char* s= x;
    
  
    return ;
  }

