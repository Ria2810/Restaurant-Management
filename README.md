# Restaurant-Management
## Introduction:

This Restaurant Management is designed to overcome the entire problem which we are facing currently, and to make complete atomization of manual system to computerized system. Since the current restaurant management is implemented in Manual, so the response is very slow. The restaurant management eliminates this limitation of the existing software.  It has the following objectives:

- Enhancement:
The main objective of Restaurant Management is to enhance and upgrade the existing system by increasing its efficiency and effectiveness. The software improves the working methods by replacing the existing manual system with the computer-based system.

- Automation:
The Restaurant Management automates each and every activity of the manual system and increases its throughput. Thus the response time of the system is very less and it works very fast.
- Accuracy:
The Restaurant Management provides the uses a quick response with very accurate information regarding the users etc. Any details or system in an accurate manner, as and when required.
- User-Friendly:
The Restaurant Management has a very user-friendly interface. Thus the users will feel very easy to work on it. The software provides accuracy along with a pleasant interface.

- Maintenance Cost:
The Restaurant Management reduces the cost of maintenance.

 
## System Description:

The main objective of this project is to develop a client/server model. The system has two parts first for the customers and the other for the management side. The customer side allows the customer to view menu list according to their desires and order meal , and at the management side the staff is allowed to edit information regarding menu list, price, billing, etc.
The advantage of the program is that there is no need to hire a person for the same only a system is required to execute it. The customer can work  on the program and select the items which he/she wants to order and accordingly can delete the items if required .It is user friendly, as it works as a calculator, a user can simply add or delete some item if required and accordingly a new bill will be generated.
In short, the program is easily executable and can be easily accessed by a user. It is a great software for the future generation as it saves time and decrease the work of the owner of the restaurant and the waiter too. It will help the owners to handle their customers in a better and a comfortable way.
Requirements definition and management is recognized as a necessary step in the delivery of successful system and software projects, discipline is also required by standards , regulations, and quality improvement initiatives. Creating and managing requirements is a challenge of IT, systems and product development projects or indeed for any activity where you have to manage a contractual relationship. Organization need to effectively define and manage requirements to ensure they are meeting needs of the customer.



 
## Requirement Analysis

The requirement of our system is to be able to store the information about the menu list, ordering and billing.
SOFTWARE REQUIREMENTS:
- Turbo C++

The services provided by the system will be : -
-	Add a new items
-	Show list of items
-	Edit details of a  menu list
-	Search a particular item
-	Delete a particular item
-	Customer's ordering
-	Details of all the bookings
-	
### Add a new items
The staff members can add a new items  as per new menu list launched by the restaurant . They have to provide information such as item no., item name, discount,price of the package.
### Show list of all the items
In this option, the staff member can check the list of all the items offered by the restaurant. 
### Edit details of a menu list
Using this option, one can edit the details of the menu list ; it means, the item no., item name and price and other details of the menu list can be changed. 
### Search a particular item
The restaurant's operating personnel can have a look at each items individually. 
### Delete a particular  item
Using this option, the member of the restaurant can delete the record of a particular item. 
### Ordering
Under this option, the user can see all details of the items available and select an item. Ordering is by entering the item no., item name and quantity required .
### See details of all the order
Using this, one can see all the information about a customer's ordering such as item no., item name , quantity and price. The total cost is calculated by adding the item prices and the discount.






 
## Architectural Design
![image](https://user-images.githubusercontent.com/67699993/121335386-291c3c80-c938-11eb-9ba9-8cfa0b6b03bf.png)
## File Design Structure                
•	Rest.dat

| Name	 | Type	        | Width         |	Description  |
|-------|--------------|---------------|--------------|
| ino   |	int	         | 2 bytes       | Order number | 
| name	 | char(string) | 50 characters | Item name    |
| price	| float	       | 4 bytes       | Item price   |
| qty	  | float	       | 4 bytes       | quantity     |
| dis	  | float	       | 4 bytes	      | discount     |  



 
## List of Header Files
Header files provide function prototype declarations for library functions. 

| HEADER FILE |	DESCRIPTION / FUNCTIONS USED                                  |
|-------------|---------------------------------------------------------------|
| iostream.h	 | provides console input/output                                 |
| conio.h	    | getch, delay, clrscr, gotoxy, kbhit                           |
| stdio.h	    | gets, puts                                                    |
| string.h	   | manipulates strings and arrays                                |
| fstream.h	  | provides definitions for stream classes ifstream and ofstream |
| process.h	  | exit                                                          |

 
## Class/Function 
### Description

Class restaurant

| Name  |	Type         | Description               |
|-------|--------------|---------------------------|
| ino   |	int          |	Stores the order number   |
| name  |	char(string) |	Stores the name of item   |
| price |	float        |	Stores the price of item  | 
| qty   |	float        |	Stores the quantity       |
| dis   |	float        |	Stores the discount       |

| Name                    | Description                                  |
|-------------------------|----------------------------------------------|
| void create_item();     |	Function to create an item              		   |
| void show_item();       | Function to display the details of item 		   |
| int retino();           | Function to return order number         		   |
| float retprice();       | Function to return price of the item    		   |
| char* retname();        |	Function to return the item name        		   |
| float retdis(); 	       | Function to return discount             		   |
| void write_item();	     | Function to write an item on the file  		    |
| void display_all();	    | Function to display details of all items     |
| void display_sp(int n); |	Function to display details of searched item |
| void modify_item();	    | Function to modify the details of an item    |
| void delete_item();	    | Function to delete an item                   |
| void menu();	           | Function to display the menu                 |
| void place_order();	    | Function to place an order and billing       |
| void admin_menu();	     | Function to display the admin menu           |
| void intro();	          | Function to display the introduction         |

## Code

#include<iostream.h>
#include<conio.h>
#include<stdio.h>
#include<process.h>
#include<fstream.h>
#include<string.h>

class restaurant
{
	int ino;
	char name[50];
	float price,qty,dis;
	public:
	void create_item()
	{
		cout<<"\nPlease Enter The Order No. of The Food Item:-";
		cin>>ino;
		cout<<"\n\nPlease Enter The Name of The Food Item:-";
		gets(name);
		cout<<"\nPlease Enter The Price of The Food Item:-";
		cin>>price;
		cout<<"\nPlease Enter The Discount(%):-";
		cin>>dis;
		cout<<"\n__________________________________________________";
	 }
	void show_item()
	{
		cout<<"\nThe Order No. of The Food Item:-"<<ino;
		cout<<"\nThe Name of The Food Item:-";
		puts(name);
		cout<<"\nThe Price of The Food Item:-"<<price;
		cout<<"\nDiscount:-"<<dis;
	}
	int  retino()
	{
		return ino;
	}
	float retprice()
	{
		return price;
	}
	char* retname()
	{
		return name;
	}
	int retdis()
	{
		return dis;
	}
};
fstream fp;
restaurant pr;

void write_item()
{
	fp.open("Rest.dat",ios::out|ios::app);
	pr.create_item();
	fp.write((char*)&pr,sizeof(pr));
	fp.close();
	cout<<"\n\nThe item Has Been Created ";
	getch();
}

void display_all()
{
	clrscr();
	cout<<"\n\n\n\t\tDISPLAY ALL ITEMS\n\n";
	fp.open("Rest.dat",ios::in);
	while(fp.read((char*)&pr,sizeof(pr)))
	{
		pr.show_item();
		cout<<"\n\n========================================\n";
	}
	fp.close();
	getch();
}

void display_sp(int n)
{
	int flag=0;
	fp.open("Rest.dat",ios::in);
	while(fp.read((char*)&pr,sizeof(pr)))
	{
		if(pr.retino()==n)
		{
			clrscr();
			pr.show_item();
			flag=1;
		}
	}
	fp.close();
	if(flag==0)
	cout<<"\n\nrecord not exist";
	cout<<"\n\n====================================================";
	getch();
}

void modify_item()
{
	int no,found=0;
	clrscr();
	cout<<"\n\n\tTo Modify ";
	cout<<"\n\n\tPlease Enter The Order No. of The Food Item:-";
	cin>>no;
	fp.open("Rest.dat",ios::in|ios::out);
	while(fp.read((char*)&pr,sizeof(pr)) && found==0)
	{
		if(pr.retino()==no)
		{
			pr.show_item();
			cout<<"\nPlease Enter The New Details of Food Item:-"<<endl;
			pr.create_item();
			int pos=-1;
			fp.seekp(pos,ios::cur);
			fp.write((char*)&pr,sizeof(pr));
			cout<<"\n\n\t Record Updated";
			found=1;
		}
	}
	fp.close();
	if(found==0)
	cout<<"\n\n Record Not Found ";
	cout<<"\n__________________________________________________";
	getch();
}

void delete_item()
{
	int no;
	clrscr();
	cout<<"\n\n\n\tDelete Record";
	cout<<"\n\nPlease Enter The Order No. Of The Food Item You Want To Delete:-";
	cin>>no;
	fp.open("Rest.dat",ios::in|ios::out);
	fstream fp2;
	fp2.open("Temp.dat",ios::out);
	fp.seekg(0,ios::beg);  
	while(fp.read((char*)&pr,sizeof(pr)))
	{
		if(pr.retino()!=no)
		{
			fp2.write((char*)&pr,sizeof(pr));
		}
	}
	fp2.close();
	fp.close();
	remove("Rest.dat");
	rename("Temp.dat","Rest.dat");
	cout<<"\n\n\tRecord Deleted ..";
	cout<<"\n\n___________________________________________";
	getch();
}

void menu()
{
	clrscr();
	fp.open("Rest.dat",ios::in);
	if(!fp)
	{
		cout<<"EMPTY FILE!”;
		getch();
		exit(0);
	}
	cout<<"\n\n\t\tFOOD MENU\n\n";
	cout<<"====================================================\n";
	cout<<"O.NO.\t\t\tNAME\t\t\tPRICE\n";
	cout<<"====================================================\n";
	while(fp.read((char*)&pr,sizeof(pr)))
	{
		cout<<pr.retino()<<"\t\t\t"<<pr.retname()<<"\t\t\t"<<pr.retprice()<<endl;
	}
	fp.close();
}
void place_order()
{
	int  order_arr[50],quan[50],c=0;
	float amt,damt,total=0;
	char ch='Y';
	menu();
	cout<<"\n============================";
	cout<<"\n  PLACE YOUR ORDER";
	cout<<"\n============================\n";
	do{
		cout<<"\n\nEnter The Order No. Of The Food Item : ";
		cin>>order_arr[c];
		cout<<"\nQuantity in number : ";
		cin>>quan[c];
		c++;
		cout<<"\nDo You Want To Order Another Food Item ? (y/n)";
		cin>>ch;
	}while(ch=='y' ||ch=='Y');
	cout<<"\n\nThank You For Placing The Order";
             getch();
             clrscr();
	cout<<"\n\n*****************************INVOICE******************************\n";
	cout<<"\nOr No.\tOr Name\tQuantity \tPrice \tAmount \tAmount after discount\n";
	for(int x=0;x<=c;x++)
	{
		fp.open("Rest.dat",ios::in);
		fp.read((char*)&pr,sizeof(pr));
		while(!fp.eof())
		{
			if(pr.retino()==order_arr[x])
			{
				 amt=pr.retprice()*quan[x];
				 damt=amt-(amt*pr.retdis()/100);
				 cout<<"\n"<<order_arr[x]<<"\t"<<pr.retname()<<"\t"<<quan[x]<<"\t\t"<<pr.retprice()<<"\t"<<amt<<"\t\t"<<damt;
				 total+=damt;
			}
			fp.read((char*)&pr,sizeof(pr));
		}
		fp.close();
	}
	cout<<"\n\n\t\t\t\t\tTOTAL = "<<total;
	getch();
}

void intro()
{
	clrscr();
	cout<<"\t\t\t\t\tRESTAURANT MANAGEMENT SYSTEM";
	cout<<"\n\n\t\t\t___________________________________\n";
	getch();
}

void admin_menu()
{
	clrscr();
	char ch2;
	cout<<"\n\n\n\tADMIN MENU";
	cout<<"\n\n\t1.CREATE ITEM";
	cout<<"\n\n\t2.DISPLAY ALL FOOD ITEMS";
	cout<<"\n\n\t3.SEARCH ";
	cout<<"\n\n\t4.MODIFY ITEM";
	cout<<"\n\n\t5.DELETE ITEM";
	cout<<"\n\n\t6.VIEW ORDER MENU";
	cout<<"\n\n\t7.BACK TO MAIN MENU";
	cout<<"\n\n\tPlease Enter Your Choice (1-7):-";
	ch2=getch();
	switch(ch2)
	{
		case '1': clrscr();
			  write_item();
			  break;
		case '2': display_all();
			  break;
		case '3': int num;
			  clrscr();
			  cout<<"\n\n\tPlease Enter The Order No:-";
			  cin>>num;
			  display_sp(num);
			  break;
		case '4': modify_item();
			  break;
		case '5': delete_item();
			  break;
		case '6': menu();
			  getch();
		case '7': break;
			  default:cout<<"\a";
			  admin_menu();
	}
}

void main()
{
	char ch;
	intro();
	do
	{
		clrscr();
		cout<<"\n\n\n\tMAIN MENU";
		cout<<"\n\n\t01. CUSTOMER";
		cout<<"\n\n\t02. ADMINISTRATOR";
		cout<<"\n\n\t03. EXIT";
		cout<<"\n\n\tPlease Select Your Option (1-3):-";
		ch=getch();
		switch(ch)
		{
			case '1': clrscr();
				  place_order();
				  getch();
				  break;
			case '2': admin_menu();
				  break;
			case '3': exit(0);
			default : cout<<"\a";
		}
	}while(ch!='3');
getch();
}

