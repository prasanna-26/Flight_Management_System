# ✈️ Flight Management System

## 📌 Introduction

The **Flight Management System** is a mobile-friendly application designed to streamline flight-related tasks for passengers. Users can:

- Easily **book**, **modify**, or **cancel** flights  
- Complete **web check-ins** and obtain **boarding passes** from home  
- Receive timely **notifications** about upcoming flights and tasks  
- Track baggage in **real-time** using the **"Baggage Track"** feature

Each bag is tagged with a unique barcode during airport check-in, enabling passengers to monitor its status and ensure it's en route to the correct destination—similar to a delivery tracking app. Currently, the system supports flight information from a single airline (e.g., Emirates).

## 📊 Business Analysis

There are **two types of users** in this system:

### 👤 Customer

- Registers using **name**, **email**, **phone number**, **password**, and **nationality**
- Searches for flights by providing:
  - Departure and arrival cities  
  - Date of travel  
  - Passenger count  
  - Trip type (one-way or round-trip)
- Views and selects available flights based on search criteria
- Makes payments using selected payment methods
- Manages bookings (view, modify, or cancel)
- Performs **web check-in** and downloads the boarding pass (up to 48 hours before departure)
- Activates **baggage tracking** by entering the special **bar code number** after airport check-in

### 🛠️ Administrator

- Logs in using admin credentials
- Can **add**, **update**, and **delete**:
  - Flight details  
  - Passenger luggage information  
- Has **full access** to payment-related operations
- Can update the **baggage location**

## 📏 Business Rules

- The system includes two users: **Customer/User** and **Administrator/Admin**
- **Customer** registers with personal information and logs in using a username and password
- The **Customer Account** contains:
  - Profile information  
  - Booking history  
  - Payment methods  
- **Flight search** is conducted based on flight parameters (cities, dates, etc.)
- **Payments** can be made for:
  - First Class  
  - Business Class  
  - Economy Class tickets
- **Admin** logs into the system and manages flight and customer data
- **Admin** has unrestricted access to **payment** and **baggage** information
- The **Baggage Track** option is accessible until the flight takes off:
  - Admin can **update** baggage location  
  - Customer can **monitor** baggage movement

## 🧱 Table Design and Analysis

The system contains **six main entities** with defined primary and foreign keys:

### 1. `User`
| Field Name     | Data Type     | Description           |
|----------------|----------------|------------------------|
| `User_ID`      | `INT(50)`      | **Primary Key**        |
| `User_Name`    | `VARCHAR(20)`  |                        |
| `User_Email`   | `VARCHAR(20)`  |                        |
| `First_Name`   | `VARCHAR(20)`  |                        |
| `Last_Name`    | `VARCHAR(20)`  |                        |
| `User_Mobile`  | `VARCHAR(20)`  |                        |
| `User_Country` | `VARCHAR(20)`  |                        |
| `Username`     | `VARCHAR(20)`  | Login credential       |
| `Password`     | `VARCHAR(20)`  | Login credential       |

### 2. `Flight_Details`
| Field Name        | Data Type     | Description           |
|--------------------|----------------|------------------------|
| `Flight_ID`        | `INT(50)`      | **Primary Key**        |
| `Departure_City`   | `VARCHAR(30)`  |                        |
| `Arrival_City`     | `VARCHAR(30)`  |                        |
| `Date`             | `INT(50)`      |                        |
| `Trip_Type`        | `VARCHAR(20)`  |                        |
| `Passengers_Count` | `INT(50)`      |                        |

### 3. `Ticket_Type`
| Field Name       | Data Type     | Description            |
|-------------------|----------------|-------------------------|
| `Flight_ID`       | `INT(50)`      | **Primary & Foreign Key** |
| `Ticket_Class`    | `VARCHAR(20)`  |                        |
| `Ticket_Price`    | `INT(50)`      |                        |

### 4. `Payment`
| Field Name         | Data Type     | Description           |
|----------------------|----------------|------------------------|
| `Transaction_ID`     | `INT(50)`      | **Primary Key**        |
| `Flight_ID`          | `INT(50)`      | **Foreign Key**        |
| `Booking_ID`         | `INT(50)`      | **Foreign Key**        |
| `Transaction_Date`   | `INT(50)`      |                        |
| `Transaction_Time`   | `INT(50)`      |                        |

### 5. `Bookings`
| Field Name       | Data Type     | Description           |
|-------------------|----------------|------------------------|
| `Booking_ID`      | `INT(50)`      | **Primary Key**        |
| `Flight_ID`       | `INT(50)`      | **Foreign Key**        |
| `User_ID`         | `INT(50)`      | **Foreign Key**        |
| `Booking_Date`    | `INT(50)`      |                        |
| `Booking_Time`    | `INT(50)`      |                        |

### 6. `Baggage_Track`
| Field Name        | Data Type     | Description           |
|---------------------|----------------|------------------------|
| `Baggage_ID`        | `INT(50)`      | **Primary Key**        |
| `Flight_ID`         | `INT(50)`      | **Foreign Key**        |
| `User_ID`           | `INT(50)`      | **Foreign Key**        |
| `Booking_ID`        | `INT(50)`      | **Foreign Key**        |
| `Baggage_Location`  | `VARCHAR(20)`  |                        |
