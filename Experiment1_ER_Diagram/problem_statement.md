# ER Diagram Workshop – Submission Template

## Objective
To understand and apply ER modeling concepts by creating ER diagrams for real-world applications.

## Purpose
Gain hands-on experience in designing ER diagrams that represent database structure including entities, relationships, attributes, and constraints.

---

# Scenario A: City Fitness Club Management

**Business Context:**  
FlexiFit Gym wants a database to manage its members, trainers, and fitness programs.

**Requirements:**  
- Members register with name, membership type, and start date.  
- Each member can join multiple programs (Yoga, Zumba, Weight Training).  
- Trainers assigned to programs; a program may have multiple trainers.  
- Members may book personal training sessions with trainers.  
- Attendance recorded for each session.  
- Payments tracked for memberships and sessions.

### ER Diagram:
<img width="1536" height="521" alt="club" src="https://github.com/user-attachments/assets/36fcf769-b01b-4e7e-b5d5-a4a3081c4066" />


### Entities and Attributes

| Entity | Attributes (PK, FK) | Notes |
|--------|--------------------|-------|
| MEMBER |MemberID (PK), Name, MembershipType, StartDate, Phone   | Stores details of fitness club members.      |
| PROGRAM       |  ProgramID (PK), ProgramName, Category                  |  Stores information about fitness programs offered.     |
|  TRAINER    | TrainerID (PK), Name, Specialization, Phone          |   Stores trainer information.     |
|SESSION        |SessionID (PK), Date, Time, TrainerID (FK)                    | Represents scheduled fitness sessions conducted by trainers.      |
|  ATTENDANCE   |    AttendanceID (PK), Status, CheckInTime, SessionID (FK)                |  Records attendance details for each session.     |
|   PAYMENT  |PaymentID (PK), Amount, PaymentDate, PaymentType, MemberID (FK)                    | Stores payment details made by members.      |

### Relationships and Constraints

| Relationship | Cardinality | Participation | Notes |
|--------------|------------|---------------|-------|
|MEMBER – JOINS – PROGRAM              |M:N            | Partial              |A member can join multiple programs, and each program can have many members       |
| PROGRAM – ASSIGNED_TO – TRAINER             |M:N            | Partial     |A trainer can handle multiple programs, and a program can have multiple trainers.|
|TRAINER – CONDUCTED_BY – SESSION | 1:N	|Total on Session	|One trainer conducts many sessions, but each session is conducted by only one trainer.|
|SESSION – HAS – ATTENDANCE|	1:N|	Total on Attendance|	One session has multiple attendance records. Each attendance record belongs to one session.|
|MEMBER – BOOKS – SESSION|	1:N|	Partial	|A member can book multiple sessions, but each booking belongs to one member.|
|MEMBER – MAKES – PAYMENT|	1:N|	Partial|	A member can make multiple payments, while each payment is made by only one member.       |

### Assumptions
- Each MemberID, ProgramID, TrainerID, SessionID, AttendanceID, and PaymentID is unique.
- A member may choose to join multiple fitness programs.
- Trainers can be assigned to more than one program based on their specialization.
- Every session is conducted by exactly one trainer.
- Attendance is recorded only for scheduled sessions.
- A member can make multiple payments (e.g., membership fee, session fee).
- PaymentType indicates whether the payment is for a Membership or a Session.
- Members are not required to join every available program or attend every session.

# Scenario B: City Library Event & Book Lending System

**Business Context:**  
The Central Library wants to manage book lending and cultural events.

**Requirements:**  
- Members borrow books, with loan and return dates tracked.  
- Each book has title, author, and category.  
- Library organizes events; members can register.  
- Each event has one or more speakers/authors.  
- Rooms are booked for events and study.  
- Overdue fines apply for late returns.

### ER Diagram:
<img width="685" height="506" alt="lib" src="https://github.com/user-attachments/assets/9a375b8e-cd20-406c-b418-fb6d21639cae" />


### Entities and Attributes

| Entity | Attributes (PK, FK) | Notes |
|--------|--------------------|-------|
|MEMBER|	MemberID (PK), Name, Email, Phone|	Stores details of library members.|
|BOOK	|BookID (PK), Title, Author, Category, ISBN|	Stores information about books available in the library.|
|EVENT	|EventID (PK), EventName, Description, EventDate, RoomID (FK)|	Stores details of library events.|
|SPEAKER	|SpeakerID (PK), Name, Profession, Contact	|Stores information about guest speakers for events.|
|ROOM|	RoomID (PK), RoomName, Capacity, Location|	Stores details of rooms where library events are held.|
### Relationships and Constraints

| Relationship | Cardinality | Participation | Notes |
|--------------|------------|---------------|-------|
|MEMBER – BORROWS – BOOK|	1:N|	Partial|	A member can borrow multiple books, while each borrowed book record belongs to one member.The relationship stores LoanDate, ReturnDate, and FineAmount.|
|MEMBER – REGISTERS – EVENT|	M:N|	Partial|	A member can register for multiple events, and each event can have many registered members.|
|EVENT – HAS – SPEAKER	|M:N	|Partial	|An event may have multiple speakers, and a speaker can participate in multiple events.|
|EVENT – HELD_IN – ROOM|	N:1|	Total on Event	Each event is conducted in one room, while a room can host multiple events over time.|

### Assumptions
- Each MemberID, BookID, EventID, SpeakerID, and RoomID is unique.
- A member can borrow multiple books, but each borrowing record is associated with one member.
- LoanDate, ReturnDate, and FineAmount are attributes of the BORROWS relationship.
- Members can register for multiple library events.
- A library event can feature one or more speakers.
- A speaker may participate in multiple events.
- Every event is held in exactly one room, while a room may host many events on different dates.
- Books are uniquely identified by BookID, while ISBN uniquely identifies the publication edition.
---

# Scenario C: Restaurant Table Reservation & Ordering

**Business Context:**  
A popular restaurant wants to manage reservations, orders, and billing.

**Requirements:**  
- Customers can reserve tables or walk in.  
- Each reservation includes date, time, and number of guests.  
- Customers place food orders linked to reservations.  
- Each order contains multiple dishes; dishes belong to categories (starter, main, dessert).  
- Bills generated per reservation, including food and service charges.  
- Waiters assigned to serve reservations.

### ER Diagram:
<img width="862" height="512" alt="restrau" src="https://github.com/user-attachments/assets/86a3813c-a1f3-4c21-a3cb-26d624004ece" />

### Entities and Attributes

| Entity | Attributes (PK, FK) | Notes |
|--------|--------------------|-------|
|CUSTOMER|	CustomerID (PK), Name, Phone, Email|	Stores customer information.|
|RESERVATION|	ReservationID (PK), ResDate, ResTime, NoOfGuests, CustomerID (FK), WaiterID (FK)|	Stores table reservation details made by customers.|
|WAITER|	WaiterID (PK), Name, Phone, Section	|Stores waiter details.|
|ORDER|	OrderID (PK), OrderDate, OrderTime, ReservationID (FK)	|Stores customer orders linked to reservations.|
|ORDER_ITEM	|OrderItemID (PK), Quantity, UnitPrice, OrderID (FK), DishID (FK)	|Stores individual items included in an order.|
|DISH|	DishID (PK), DishName, Price, CategoryID (FK)|	Stores menu dish details.|
|CATEGORY|	CategoryID (PK), CategoryName, Description	|Stores categories of dishes (e.g., Starters, Main Course, Desserts).|
|BILL	|BillID (PK), BillDate, FoodCharge, ServiceCharge, TotalAmount, OrderID (FK)|	Stores billing details generated for each order.|

### Relationships and Constraints

| Relationship | Cardinality | Participation | Notes |
|--------------|------------|---------------|-------|
| CUSTOMER – MAKES – RESERVATION|	1:N|	Partial|	A customer can make multiple reservations, while each reservation belongs to one customer.|
|RESERVATION – ASSIGNED_TO – WAITER|	N:1|	Total on Reservation	|Each reservation is assigned to one waiter, while a waiter can handle multiple reservations.|
|RESERVATION – HAS – ORDER|	1:N|	Partial|	A reservation may include multiple orders, while each order belongs to one reservation.|
|ORDER – CONTAINS – ORDER_ITEM|	1:N|	Total on Order| Item	One order contains multiple order items, and each order item belongs to one order.|
|ORDER_ITEM – REFERS_TO – DISH|	N:1|	Total on Order Item	Each order item refers to one dish, while a dish can appear in many order items.|
|DISH – BELONGS_TO – CATEGORY|	N:1|	Total on Dish	Each dish belongs to one category, while each category can contain many dishes.|
|ORDER – GENERATES – BILL|	1:1	|Total	|Each order generates exactly one bill, and each bill corresponds to one order. |            

### Assumptions
- Each CustomerID, ReservationID, WaiterID, OrderID, OrderItemID, DishID, CategoryID, and BillID is unique.
- A customer can make multiple reservations on different dates and times.
- Every reservation is assigned to exactly one waiter.
- A reservation may include one or more food orders.
- Every order contains at least one order item.
- Each order item refers to only one dish, but the same dish may appear in multiple orders.
- Every dish belongs to exactly one category.
- Each completed order generates exactly one bill containing food charges, service charges, and the total amount.
---
