# test
#include<iostream>
using namespace std;
struct student
{
	char name[50];
	char num[15];
	int age;
	struct student * next;
};

int main()
{
	struct student *p,*q,*head;
	int s;
	int count=0;
	head=NULL;
	while(cout<<"live or die"<<endl,cin>>s,s==1)
	{
		p=new student;
		cin>>p->name;
		cin>>p->num;
		cin>>p->age;
		if(head==NULL)
		{
			head=p;
		}
		else
		{
			q->next=p;
		}
		q=p;
		p->next=NULL;
		count++;	 
	}
	p=head;
	while(p!=NULL)
	{
		cout<<p->name<<" "<<p->num<<" "<<p->age<<endl;
		p=p->next;
	}
	if(count)
	{
		p=head;
		do
		{
			q=p->next;
			delete p;
			p=q;
		}while(q);
	}
	return 0;
}	
