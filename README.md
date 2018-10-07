# StructExc1
Да се напише програма, която създава структура Automobile с полета brand, model, date, и price, указващи марка, модел, дата на производство и цена на автомобилите в автосалон. Да се въведе цяло число n и след него n на брой данни от тип Automobile. Да се въведе реално число P и да се намери колко автомобила има в наличност с тази цена. 

#include<iostream>
using namespace std;
struct Automobile
{
       char brand [20];
       char model [20];
       char date [12];
       double price;
};
int main()
{
    int n;
    cout<<"Number of cars: ";
    cin>>n;
    Automobile cars[n];
    for(int i=0;i<n;i++)
    {
            cout<<"Brand: ";
            cin>>cars[i].brand;
            cout<<"Model: ";
            cin>>cars[i].model;
            cout<<"Date: ";
            cin>>cars[i].date;
            cout<<"Price: ";
            cin>>cars[i].price;
    }
     double p;
     int count=0;
     cout<<"Enter price: ";
     cin>>p;
     cout<<"Number of cars with this price: "<<endl;
     for (int i=0;i<n;i++)
     {
         if(cars[i].price==p) 
         {
          count=count+1;
         }
     }
          cout<<count<<endl;;
     system("pause");
     return 0;
    }
                             
 // Същата задача решена с указател към структура
#include<iostream>
using namespace std;
struct Automobile
{
       char brand [20];
       char model [20];
       char date [12];
       double price;
};
int main()
{
    int n;
    cout<<"Number of cars:";
    cin>>n;
    Automobile cars[n];
    Automobile *q;
    q=cars;
    for(int i=0;i<n;i++)
    {
            cout<<"Brand: ";
            cin>>q->brand;
            cout<<"Model: ";
            cin>>q->model;
            cout<<"Date: ";
            cin>>q->date;
            cout<<"Price: ";
            cin>>q->price;
            q++;
    }
     double p;
     int count=0;
     cout<<"Enter price: ";
     cin>>p;
     cout<<"Number of cars with this price: "<<endl;
     for (int i=0;i<n;i++)
     {
         if(cars[i].price==p) 
         {
          count=count+1;
         }
     }
          cout<<count<<endl;;
     system("pause");
     return 0;
    }
