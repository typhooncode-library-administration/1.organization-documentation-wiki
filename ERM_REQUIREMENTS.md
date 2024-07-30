# ERM Requirements

The following are the key requirements that describe the relationships and rules in the ERM of the library management software system:

## Entity-Relationship-Model (ERM)

![Database Structure](ERM_Bibliotheksverwaltung.drawio.png)

## Entities

#### Customer
- **Description**: Represents a library customer who borrows media and participates in events.
- **Attributes**:
  - `Customer_ID`: Unique identifier of the customer.
  - `Name`: Name of the customer.
  - `Location_ID`: Reference to the customer's location.

#### Location
- **Description**: Represents a physical location with address information for customers and libraries.
- **Attributes**:
  - `Location_ID`: Unique identifier of the location.
  - `Street`: Street name and number.
  - `City`: City name.
  - `Postal_Code`: Postal code.
  - `Country`: Country name.

#### Library
- **Description**: Represents a library that offers various media and organizes events.
- **Attributes**:
  - `Library_ID`: Unique identifier of the library.
  - `Library_Name`: Name of the library.
  - `Location_ID`: Reference to the library's location.

#### Loan
- **Description**: Represents a loan containing media items borrowed by a customer.
- **Attributes**:
  - `Loan_ID`: Unique identifier of the loan.
  - `Customer_ID`: Reference to the customer making the loan.

#### Medium
- **Description**: Represents a medium (e.g., book, DVD) that can be borrowed from the library.
- **Attributes**:
  - `Medium_ID`: Unique identifier of the medium.
  - `Title`: Title of the medium.
  - `MediaType_ID`: Reference to the media type.
  - `Inventory_ID`: Reference to the inventory of the medium.

#### Inventory
- **Description**: Represents the inventory unit of a medium in the library.
- **Attributes**:
  - `Inventory_ID`: Unique identifier of the inventory.
  - `Medium_ID`: Reference to the medium.

#### Fee
- **Description**: Represents fees that a customer must pay for various services.
- **Attributes**:
  - `Fee_ID`: Unique identifier of the fee.
  - `Customer_ID`: Reference to the customer who pays the fee.
  - `Amount`: Amount of the fee.
  - `FeeType_ID`: Reference to the fee type.

#### Payment
- **Description**: Represents a payment that settles a fee.
- **Attributes**:
  - `Payment_ID`: Unique identifier of the payment.
  - `Fee_ID`: Reference to the fee.
  - `Amount`: Amount of the payment.










### Tables and Relationships

#### 1.Customer
- **customer_id**: int (Primary Key)
- **first_name**: varchar(25)
- **last_name**: varchar(35)
- **birthdate**: date
- **street**: varchar(50)
- **house_number**: int
- **city**: varchar(25)
- **postal_code**: varchar(5)
- **area_code**: varchar(5)
- **phone_number**: varchar(20)
- **email_address**: varchar(100) (Unique)

#### 2.Library_card
- **library_card_id**: int (Primary Key)
- **fk_customer**: int (Foreign Key)
- **fk_extended_location**: int (Foreign Key) 
- **valid**: boolean
- **expiration_date**: date

#### 3.Events
- **event_id**: int (Primary Key)
- **fk_location**: int (Foreign Key)
- **title**: varchar(100) NOT NULL
- **descriptio**: text NOT NULL
- **datetime_begin**: date
- **datetime_end**: int (Primary Key)
- **number_max_participants** smallint NOT NULL
- **number_subscribed_participants** smallint
