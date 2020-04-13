# fos
**Online Food Ordering System** 


Table Name

+--------------------------------------+

- User accounts [User]
- Profile       [For extra fields]
- Restaurant    [For Resaurant]
- Category      [Categories of food]
- Food          [Food items]
- Cart          [Cart]
- Order         [Order]
- Orderitem     [OrderItem]

+----------------------------------------------+

**No of Django Concept use in this system**

+----------------------------------------------+
- User registartion      [all auth]
- Sending email          [signals and celery]
- Checking Permissions   [Decorators]

+----------------------------------------------+

+-----------------------------------------------------------------------+

**No of Javascripta and css Concept use in this system**

+-----------------------------------------------------------------------+
 - Simple javascript     [for some dynamically change]
 - Jquery                [for some dynamically change]
 - AJAX                  [for send request on perticuler events occured]
 - CSS                   [Some Basic design]    
 - Bootstrap4            [Use advance Models, cart, Alert etc design ]

+-----------------------------------------------------------------------+

**Model Description**

+-----------------------------------------------------------------------+

+----------------------+

1. **User**

+----------------------+

   - id
   - username
   - password
   - firstname
   - lastname
   - email
   - active
   - staff
   - super
   ....
   
+----------------------+

2. **City**

+----------------------+

   - id
   - name
   - description
   
+----------------------+

3. **Profile**

+----------------------+

   - id
   - user          [OneToOne with User]
   - address 
   - contact
   - city          [OneToOne with City]
  
+----------------------+

4. **Restaurant**

+----------------------+

   - id
   - user          [OneToOne with User]
   - name
   - address 
   - contact
   - city          [OneToOne with City]
   - open

+----------------------+

5. **Category**

+----------------------+

 - id
 - name
 - description

+----------------------+

6. **Food**

+----------------------+

 - id
 - category       [ForeignKey with category]
 - name
 - qunatity
 - price  
 - description

+----------------------+

7. **Cart**

+----------------------+

 - id
 - user      
 - food           [OneToOneField with food]
 - restaurant     [OneToOne with restaurant]
 - qunatity       [Quantity of user want to buy]
 - price          

+----------------------+

8. **Order**

+----------------------+

 - id
 - user    
 - restaurant     [OneToOne with restaurant]
 - date           [Date  and time of order]
 - total_price 

+----------------------+

9. **Orderitem**

+----------------------+

 - id
 - order          [ForeigKey with Order]
 - food           [OneToOne with food]
 - qunatity       [Quantity of user want to buy]
 - price
 
+----------------------+
