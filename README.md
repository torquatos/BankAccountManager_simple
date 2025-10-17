# BankAccountManager_simple
A simple system for  managing bank accounts - POO, business logic and financial environment 

  This document perceive an initial guidance for the development of this project, and the technical specifications as well. This project has as main objective to create a solid system within its backend logics and allowing extensions in its future versions.

  1- Vision of the Project

      This System has as its focus the principles of POO (object oriented programming) and the basic rules for a financial business 

  2 - Scope and Features

      Development in phases achieve the essential funtionalities of the MVP(minimum viable product):

      | --- | --- | --- |  
      | Category | Functionality | Details |
      | --- | --- | --- |
      | Creating/Register | Register/Create an account | The creation of an account demands a id-number, name and opening balance |
      | --- | --- | --- |
      | type of account | current account | implementation of the class as base |
      | --- | --- | --- |
      | type of account | savings account | implementation of the class with an income logic (simple)/ method for applying income |
      | --- | --- | --- |
      | operations | deposit | add to the balance ammount |
      | --- | --- | --- |
      | operations | withdrawal | withdrawal from the balance amount. It needs to have a factor of verification/validaation for enough balance/source for the required amount in the operation |
      | --- | --- | --- |
      | operations | transfer | stablish movement of amounts between different accounts (send value to another account). It must have the validation/verification for the enough balance to proceed with the operation (factor implemented for the account of origin). It must have a factor of validation/verification for the existence of the account of destiny for the transfer.  |
      | --- | --- | --- |
      | account view | balance view | show the amount in the balance in real time |
      | --- | --- | --- |
      | account view | bank statement | show a timeline based list of the transactions (operations) |
      | --- | --- | --- |

  3. Architecture and Fundamentals

      Business Logic is the model and it's separeted of the persistence and the interface (MVC)

     3.1 POO - Object oriented programming

         Model of Classes:
     
           a - Client: storage the data of the client (name, id, etc)
           b - Account: parent class. base of the bank account - atributes and methods
           c - Current account / Savings Account : gets heritage from the Account (b)
                   - the savings account needs to implement  an income-application logic
           d - transactions: this object wll register each aspect of the operation

         Encapsulation:

            All critical attributes must to be PRIVATE and only being possible to be accessed or modified through getters, setter and/or business methods - integrity of the data

         Heritage/Polimorfism:

            Treatment and application on specific operations

     3.2 Data Structure
     3.3 Control of Flow and Validation

  4. Data Persistence
  5. User Interface
     


         
  
