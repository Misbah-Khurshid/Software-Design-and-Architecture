# Class Activity: Food Delivery System and Bank Management System

From Real World Concept to Software Object
Course: Software Design & Architecture (SEC-532)
University: The University of Azad Jammu and Kashmir, Muzaffarabad

**Student:** Misbah Khurshid|
**Roll No:** 2025-SE-10|
**Semester:** 3rd | **Session:** 2025-29

---

## Contents

1. [Food Delivery System](#1-food-delivery-system)
2. [Bank Management System](#2-bank-management-system)

---

## 1. Food Delivery System

### Overview

This part models a Food Delivery System as a set of conceptual classes. A food delivery service handles customers, restaurants, menus, orders, payments, delivery riders, promotions and reviews at the same time. The goal is to organize these real world ideas into clear classes with attributes and methods, before thinking about any implementation.

### Conceptual Classes

1. **Customer:** A person who orders food through the service.
2. **Restaurant:** A business that prepares and sells food.
3. **MenuItem:** A single dish or drink offered by a restaurant.
4. **Order:** A request placed by a customer for one or more menu items.
5. **OrderItem:** One line within an order, linking a menu item with its quantity.
6. **DeliveryRider:** A person who collects the order and delivers it to the customer.
7. **DeliveryAddress:** The location where an order must be delivered.
8. **Payment:** Money paid by the customer for an order.
9. **Promotion:** A discount or offer, such as a voucher code.
10. **Review:** Feedback given by a customer about a restaurant or delivery.

### Detailed Classes

**Customer**
- Attributes: customerId, fullName, email, phoneNumber, defaultAddress
- Methods: updateProfile(), browseRestaurants(), placeOrder(), viewOrderHistory()

**Order**
- Attributes: orderId, customerId, restaurantId, orderDate, totalAmount, status
- Methods: createOrder(), updateStatus(), assignRider(), calculateTotal()

**Restaurant**
- Attributes: restaurantId, restaurantName, location, cuisineType, openingHours, rating
- Methods: addMenuItem(), updateMenuItem(), acceptOrder(), generateSalesSummary()

### Abstraction Decisions

Customer, Order and Restaurant were chosen for detailed modeling because they are central to daily operations. Real-time GPS tracking, route optimization, rider salary calculation, inventory management and detailed accounting were left out as beyond the scope of this small model. Screens, database tables and programming language details were also excluded.

### Invented Software Object

**Order Validation Checker:** Checks an order before it is sent to the restaurant. It confirms the cart has at least one item, the restaurant is open, every item is available, a valid delivery address is given and a payment method is selected. It returns whether the order can proceed or what is missing.

---

## 2. Bank Management System

### Overview

This part models a Bank Management System as a set of conceptual classes. A bank handles customers, accounts, transactions, loans, cards and branches at the same time. The same approach is used: identify classes, define attributes and methods, and make clear abstraction decisions.

### Conceptual Classes

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

### Detailed Classes

**Customer**
- Attributes: customerId, fullName, email, phoneNumber, address
- Methods: updateProfile(), openAccount(), viewAccounts(), applyForLoan()

**Account**
- Attributes: accountNumber, accountType, balance, openDate, status
- Methods: deposit(), withdraw(), transfer(), checkBalance()

**Transaction**
- Attributes: transactionId, accountNumber, type, amount, date, status
- Methods: record(), verify(), reverse(), generateReceipt()

### Abstraction Decisions

Customer, Account and Transaction were chosen for detailed modeling because they are central to everyday banking. Interest rate calculation, tax handling, fraud detection and detailed accounting were left out as beyond the scope of this small model. Screens, database tables and programming language details were also excluded.

### Invented Software Object

**Transaction Validator:** Checks a transaction before it is processed. It confirms the account is active, the amount is valid, the balance is sufficient and the beneficiary exists. It returns whether the transaction can proceed or what is missing.

---

## Conclusion

Both systems show how real world ideas can be turned into software objects by identifying classes, defining attributes and methods, and making clear abstraction decisions before any implementation.
