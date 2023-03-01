#include<iostream>
using namespace std;
struct student{
    string name;
    float grade[10];
    float avg;
};
student s;
float get_grade(int k)
{
        cout<<"grade("<<k<<")=";
        cin>>s.grade[k];
        return s.grade[k];
}
float clculate_avg()
{
      float avge=0;
    for(int k=0;k<10;k++)
    {
        avge=avge+s.grade[k];
    }
    return avge/10;
}
/*
void search_students()
{
    string na;
    cin>>na;
    for(int i=0;i<5;i++)
    {
        if(na==s[i].name)
        {
           cout<<"name : "<<s[i].name<<endl;
           cout<<"avg : "<<s[i].avg<<endl<<"grades : ";
           for(int j=0;j<10;j++)
           {
              cout<<s[i].grade[j]<<"\t";
           }
        }
    }
}
void find_top_student()
{
    cout<< "the best student : ";
    float max = s[0].avg;
    string fname = s[0].name;
    for(int i=1;i<5;i++)
    {
        if(s[i].avg>max)
        {
            max = s[i].avg;
            fname = s[i].name;
        }
    }
    cout<<fname<<"\t"<<"avg = "<<max<<endl;
}
*/
int get_student()
{
    student st[1];
 for(int i=0;i<1;i++)
{
    cout<<"enter a name : ";
    cin>> s.name;
    st[i].name = s.name;
    cout<<"enter 10 grades :"<<endl;
    for(int k=0;k<10;k++)
    {
    st[i].grade[k] = get_grade(k);
    }
    st[i].avg = clculate_avg();
}
return 0;
}
int main()
{
    student st[1];
    get_student();
    cout<<st[0].grade[5]<<endl;
    cout<<st[0].avg<<endl;
    return 0;
}
