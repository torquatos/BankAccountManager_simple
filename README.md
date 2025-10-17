# BankAccountManager_simple
A simple system for  managing bank accounts - POO, business logic and financial environment 

  This document perceive an initial guidance for the development of this project, and the technical specifications as well. This project has as main objective to create a solid system within its backend logics and allowing extensions in its future versions.

  1- Vision of the Project

      This System has as its focus the principles of POO (object oriented programming) and the basic rules for a financial business 

  2 - Technological Stack and Initial Requirements 

    | --- | --- | --- |
    | Component | Technology | Detail |
    | --- | --- | --- |
    | Language | JAVA | POO - Core of the application |
    | --- | --- | --- |
    | Framework | SpringBoot | Spring appllications |
    | --- | --- | --- |
    | Persistence | SpringData JPA/Hibernate | ORM - object relation mapping - persistence of the Java objects in the SQL |
    | --- | --- | --- |
    | DataBank | MySQL | Relational Dadabank |
    | --- | --- | --- |
    | API | SpringWeb - REST Controllers | RESTful endpoints |
    | --- | --- | --- |
    | Tests | JUnit5-Mockito | Assures the service layer and the integrity of the API |
    | --- | --- | --- |
    
  3 - Scope and Features

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

  4. Architecture and Fundamentals

      Business Logic is the model and it's separeted of the persistence and the interface (MVC)

     4.1 POO - Object oriented programming

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

     4.2 Data Structure

      Check within the item 4, work better on the aspects of the dara structure and data persistence
     
     4.3 Control of Flow and Validation

          All the operations must to include a entry validation and a status validation

               a - Business Validation: implementation of logic of conditions to assure the rules are rightly followed. Once the logic "fails" throw the exception
               b - Exception treatment: try-catch blocks to deal with unexpected errors - makes the "code" not break and returns a feedback to the user

  5. Data Persistence
  6. User Interface

     Priority is on the backend, so it will follow two phases for interface:

         - Initial: MVP - Console: interface using command line (make sure it's working properly, validation and test of the backend)
         - Final User: A graphic interface, still a simple one - GUI (separation between the view/presenting logic and the business logic) - decide later on the technology / tool for the frontend development 


  7. Phases

           a - Initial configuration: configure the project using springboot - Spring Initializr - with the dependencies : web, jpa, mySqlDriver
           b - modeling and repo: create the classes Account, CurrentAccount, SavingsAccount and Transactions (or operations, verify what is the better naming), create the repository interfaces
           c - service: implementation of the AccountService as the POO logic, together with the validations of balance and the exception treatments for the service
     


         
  
