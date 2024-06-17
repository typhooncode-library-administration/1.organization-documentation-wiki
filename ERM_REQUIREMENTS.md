# ERM Requirements

The following are the key requirements that describe the relationships and rules in the ERM of the library management software system:

## Database structure

![Database Structure](ERM_Bibliotheksverwaltung.drawio.png)


### Tables and Relathionships

#### 1. Customer
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
