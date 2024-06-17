# ERM Requirements

The following are the key requirements that describe the relationships and rules in the ERM of the library management software system:

## Database structure

![Database Structure](ERM_Bibliotheksverwaltung.drawio.png)


### Tables and Relathionships

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
