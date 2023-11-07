# ATM_project
#include <bits/stdc++.h>
using namespace std;


// I have used class User to define the two major variables : username and pswd
class User
{
private:
    std::string username;
    std::string password;

public:
    User(const std::string &username, const std::string &password)
        : username(username), password(password)  // setting the provided username and pswd
    {
    }

    const std::string &showUsername() const
    {
        return username;
    }

    const std::string &showPassword() const
    {
        return password;
    }
};

class BankAccount
{
private:
    double balance;

public:
    BankAccount(double initialBalance = 0.0)
        : balance(initialBalance)
    {
    }

 
    void deposit(double amount)
    {
        balance += amount;
    }

    void withdraw(double amount)
    {
        if (amount <= balance)
        {
            balance -= amount;
            cout<<"Amount withdrawn : "<<amount;
        }else{
            cout<<"Not enough balance";
        }
    }
       double getBalance() const
    {
        return balance;
    }

};

class ATM
{
private:
    unordered_map<string, User> users;

public:
    void addUser(const User &user)
    {
        users[user.showUsername()] = user;
    }
    bool authenticateUser(const std::string& username, const std::string& password) {
        auto it = users.find(username);
        if (it != users.end() && it->second.showPassword() == password) {
            return true;
        }
        return false;
    }









};

    int main()
    {
    

        return 0;
    }
