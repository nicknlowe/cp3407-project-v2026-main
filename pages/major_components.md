# CP3407 Project - Major Components Explanation

## Overview

FeedMe's architecture was designed with scalability, maintainability, and user experience as core principles. Our design choices reflect modern web development practices while ensuring robust functionality.

## Architectural Design

<img width="602" height="939" alt="architecturaldesign" src="https://github.com/user-attachments/assets/4d9909d1-c7a7-4869-947d-07c8d24a7fba" />

This architecture shows a simple, cloud-based setup for our FeedMe food app. The frontend (user’s device) communicates securely through Amazon CloudFront, which handles caching and protection before routing requests to the backend. Payments are processed via Stripe, while core application data (orders, users, restaurants) is stored in an Amazon RDS instance, with phpMyAdmin used for database administration.

## Database Design

```mermaid
erDiagram
    USER {
        int user_id PK
        string name
        string email
        string password_hash
        string role "user | admin"
        date date_created
    }
    RESTAURANT {
        int restaurant_id PK
        string name
        string description
        string address
        string contact_number
        float rating
    }
    MENUITEM {
        int item_id PK
        int restaurant_id FK "RESTAURANT.restaurant_id"
        string name
        string description
        float price
        string image_url
        boolean availability_status
    }
    ORDER {
        int order_id PK
        int user_id FK "USER.user_id"
        int restaurant_id FK "RESTAURANT.restaurant_id"
        float total_amount
        string payment_status
        string order_status
        date created_at
    }
    ORDERITEM {
        int order_item_id PK
        int order_id FK "ORDER.order_id"
        int item_id FK "MENUITEM.item_id"
        int quantity
        float subtotal
    }
    DELIVERYTRACKING {
        int tracking_id PK
        int order_id FK "ORDER.order_id"
        string status "Placed | Preparing | Out for Delivery | Delivered"
        date last_updated
    }
    PAYMENT {
        int payment_id PK
        int order_id FK "ORDER.order_id"
        string stripe_transaction_id
        float amount
        string payment_method
        string payment_status
        date timestamp
    }
    USER ||--o{ ORDER : "places"
    RESTAURANT ||--o{ MENUITEM : "offers"
    ORDER ||--o{ ORDERITEM : "contains"
    MENUITEM ||--o{ ORDERITEM : "referenced in"
    ORDER ||--|| DELIVERYTRACKING : "has"
    ORDER ||--|| PAYMENT : "has"
```

The ER diagram above defines how data flows through our FeedMe app at a relational level. A user creates an order tied to a specific restaurant, and each order is broken down into multiple order items, which link back to individual menu items (resolving the many-to-many relationship between orders and menu items). Restaurants manage their own menu items, including pricing and availability, while each order stores totals and status information.
Payments are handled in a separate table, allowing each order to have a tracked transaction (e.g., via Stripe), including payment status and method. Delivery tracking is also separated, enabling real-time updates (placed, preparing, out for delivery, delivered) without modifying the main order record. Overall, the design keeps data modular, scalable, and easy to query for key features like order history, live tracking, and restaurant management.

## Interface Design

[Interface Design NinjaMock](https://ninjamock.com/s/558WWZx)

### Home Page

<img width="1926" height="1196" alt="image" src="https://github.com/user-attachments/assets/773752c3-4b53-4b59-85bc-1478dede1379" />

### Order Page

<img width="1930" height="1196" alt="image" src="https://github.com/user-attachments/assets/69289e36-2d88-4e99-8f9a-033bd07b5de8" />

### Category Page

<img width="1927" height="1196" alt="image" src="https://github.com/user-attachments/assets/21d7cdfe-1793-4b16-a3c8-5560c2117bbb" />

### The Story Page

<img width="1927" height="1195" alt="image" src="https://github.com/user-attachments/assets/5fd33cca-249c-4ad0-8790-09dc68d3e70d" />

### Support Page

<img width="1928" height="1199" alt="image" src="https://github.com/user-attachments/assets/f5478273-501a-41cd-ad61-39ce6ac8dd3b" />
