# CP3407 Project - Major Components Explanation

## Overview

FeedMe's architecture was designed with scalability, maintainability, and user experience as core principles. Our design choices reflect modern web development practices while ensuring robust functionality.

## Architectural Design

<img width="602" height="939" alt="architecturaldesign" src="https://github.com/user-attachments/assets/4d9909d1-c7a7-4869-947d-07c8d24a7fba" />

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

## Interface Design

[Interface Design NinjaMock](https://ninjamock.com/s/558WWZx)
