# ATM_project
#include <bits/stdc++.h>
using namespace std;

class User
{
private:
    std::string username;
    std::string password;

public:
    User(const std::string &username, const std::string &password)
        : username(username), password(password)
    {
    }

    const std::string &getUsername() const
    {
        return username;
    }

    const std::string &getPassword() const
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

    double getBalance() const
    {
        return balance;
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
};

class ATM
{
private:
    unordered_map<string, User> users;

public:
    void addUser(const User &user)
    {
        users[user.getUsername()] = user;
    }









};

    int main()
    {

        return 0;
    }
