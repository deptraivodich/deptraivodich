#include <iostream>
#include <cmath>
using namespace std;

int main()
{
	double sokm=0.0;
	cout<<"nhap vao so km da di: ";
	cin>>sokm;
	
	double tongtien=0.0, kmdau=5000;
	tongtien+=kmdau;
	
	double kmtu2_5=4500;
	if(sokm>1)
	{
		for(int i=2;i<=5 && i<=sokm ;++i)
		{
			tongtien+=kmtu2_5;
		}
	}
	
	double kmthu6trodi=3500;
	if(sokm>5)
	{
		for(int i=6; i<=sokm;++i)
		{
			tongtien+=kmthu6trodi;
		}
	}
	
	double mucgiam=0.1,giam=0.0;
	if(sokm>120)
	{
		for(int i=121; i<=sokm ;++i)
		{
			giam=mucgiam*tongtien;
			tongtien-=giam;
		}
	}
	cout<<"tong so tien di taxi la: "<<tongtien;
	return 0;
}
