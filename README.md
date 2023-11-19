This is my designed version of ATM Management System. 
Since the problem statement was to create classes which would have functionalities of an ATM bank , I have planned on using a map data structure for it. 
We can put the key as the username of that user and other details of that user i.e the object created,  can be the value of that key.

I have made the modifications in my code accordingly. I have taken user input in the main function.
Here is the description of some of the important parts of my code : 

(1) I have created three classes : ATM class, User class and BankAccount class.
    -> ATM class prints all the data (username, password and balance) of the user when he chooses the option . 
    -> BankAccount class has all the major functions , like deposit money , withdraw and checking balance .
    -> User class contains all the important details , eg. Creating an empty account for a user who has chosen to register, and setting up username and password for him/her. It uses the BankAccount object for working of deposit and withdraw functions. It also has function to authenticate the user of its the correct username and password or not.

(2) The int main function has user inputs in it. It gives the user 4 options : 
Register account, withdraw, deposit or check balance. 
