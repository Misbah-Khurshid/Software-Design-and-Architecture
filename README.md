# Software-Design-and-Architecture
# Bank Management System

Class Activity: From Real World Concept to Software Object
Course: Software Design & Architecture (SEC-532)
University: The University of Azad Jammu and Kashmir, Muzaffarabad

**Student:** Misbah Khurshid
**Roll No:** 2025-SE-10
**Semester:** 3rd | **Session:** 2025-29

---

## Overview

This project models a Bank Management System as a set of conceptual classes. A bank handles many things at the same time, such as customers, accounts, transactions, loans, cards and branches. The goal of this activity is to organize these real world ideas into clear classes with attributes and methods, before thinking about any implementation.

## Conceptual Classes

1. **Customer:** A person who holds one or more accounts in the bank.
2. **Account:** A bank account that stores a balance and belongs to a customer.
3. **Transaction:** A deposit, withdrawal or transfer made on an account.
4. **Branch:** A physical bank location that serves customers.
5. **Employee:** A bank staff member such as a cashier or manager.
6. **Loan:** Money lent to a customer, with an amount, duration and repayment status.
7. **Card:** A debit or credit card linked to an account.
8. **Statement:** A summary of an account's transactions over a period.
9. **Beneficiary:** A saved recipient for transfers.
10. **Notification:** An alert sent to a customer about account activity.

## Detailed Classes

### Customer
- **Attributes:** customerId, fullName, email, phoneNumber, address
- **Methods:** updateProfile(), openAccount(), viewAccounts(), applyForLoan()

### Account
- **Attributes:** accountNumber, accountType, balance, openDate, status
- **Methods:** deposit(), withdraw(), transfer(), checkBalance()

### Transaction
- **Attributes:** transactionId, accountNumber, type, amount, date, status
- **Methods:** record(), verify(), reverse(), generateReceipt()

## Abstraction Decisions

Customer, Account and Transaction were chosen for detailed modeling because they are central to everyday banking. The other classes support them. Interest rate calculation, tax handling, fraud detection and detailed accounting were left out because they are beyond the scope of this small model. Screens, database tables and programming language details were also excluded, since conceptual modeling focuses on the real world domain.

## Invented Software Object

**Transaction Validator:** Checks a transaction before it is processed. It confirms that the account is active, the amount is valid, the balance is sufficient and the beneficiary exists. It returns whether the transaction can proceed or what is missing. It has no direct real world counterpart, but it keeps the business rules consistent.

## Conclusion

The Bank Management System shows how real world banking ideas can be turned into software objects by identifying classes, defining attributes and methods, and making clear abstraction decisions.
