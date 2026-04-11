# User story title: Order History & Reordering 

## Priority: Medium
This feature is important for improving user convenience and encouraging repeat purchases, but it is not required for the initial system launch. Priority may increase in later iterations once core ordering functionality is stable.

## Estimation: e.g. 3 days
Planning poker estimates.
* Dean: 2 day 
* Gurjas: 2 days
* Nick: 3 days
* Nikodem: 3 days
* Dylan: 2 days

## Assumptions (if any):
* Users must be logged in to view their order history.
* Order data is already stored in the database from previous completed purchases.
* Reordering will duplicate a previous order and allow minor edits before checkout.
* Payment processing is handled by the existing checkout system.

## Description: 

Description-v1: The web application will allow users to view a list of their previous orders, including order date, items purchased, total price, and order status.

## Tasks, see chapter 4.

1. Task 1 - Design order history page: 1 day  
2. Task 2 - Retrieve and display past orders from database: 1 day  
3. Task 3 - Restrict access to logged-in users: 0.5 day  
4. Task 4 - Implement reorder functionality: 1 day  
5. Task 5 - Allow editing before checkout: 0.5 day  
6. Task 6 - Test order history and reorder flow: 0.5 day  

# UI Design:
<img width="1536" height="1024" alt="userstory8" src="https://github.com/user-attachments/assets/0307c2f8-fbf4-4eb2-8ade-20c9968b95fc" />


# Completed:
<img width="1243" height="378" alt="orderhistory" src="https://github.com/user-attachments/assets/93737ed4-28ce-4fa7-b918-c59f78e7e722" />
