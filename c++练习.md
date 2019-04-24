```
#include<iostream>
#include<cstring>
#include<map>
#include<deque>
using namespace std;
#define fori(a) for(int i=0;i<a;i++)
#define forj(a) for(int j=0;j<a;j++)
#define ifor(a,b) for(int i=a;i<=b;i++)
#define jfor(a,b) for(int j=a;j<=b;j++)
#define mem(a,b) memset(a,b,sizeof(a))
class Person
{
    public:
        Person (string name="李四",int age=15)
        {
            m_strName=name;
            m_iAge=age;
        }
        ~Person(){};
        void sayInfo()
        {
            cout<<"我是"<<m_strName<<endl;
            cout<<"我今年"<<m_iAge<<"岁"<<endl;
        }
        void sayLanguage()
        {
            cout<<"我会说话"<<endl;
        }
    protected:
        string m_strName;
        int m_iAge;
 };

 class Chinese : public Person
 {
    public:
        Chinese (string sex,string name,int money,int age):Person(name,age)
        {
            m_strSex=sex;
            m_iMoney=money;
        }
        ~Chinese(){};
        void sayLanguage()
        {
            cout<<"我会说汉语"<<endl;
        }
        void personallntrouduce()
        {
            sayInfo();
            sayLanguage();
        }
    protected:
        string m_strSex;
        int m_iMoney;
 };

 class American :public Person
 {
    public:
        American(string name,int age) :Person(name,age){}
        ~American(){};
        void sayLanguage()
        {
            cout<<"我会说英语"<<endl;
        }
 };

 int main()
 {
     Chinese *p=new Chinese("男","李四",1500,150);
     p->sayLanguage();
     p->sayInfo();
     p->personallntrouduce();
     delete p;
     p=NULL;
     American *q=new American("JIM",15);
     q->sayLanguage();
     q->sayInfo();
     delete p;
     q=NULL;
 }


```







