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

