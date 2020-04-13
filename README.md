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
+--------------------------------------+

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

+----------------------+
2. **Profile**
+----------------------+
   - id
   - user          [OneToOne with User]
   - address 
   - contact
   - city 
+----------------------+

+----------------------+
3. **Restaurant**
+----------------------+
   - id
   - user          [OneToOne with User]
   - name
   - address 
   - contact
   - city 
   - open
+----------------------+

+----------------------+
4. **Category**
+----------------------+
 - id
 - name
 - description
+----------------------+

+----------------------+
5. **Food**
+----------------------+
 - id
 - category       [ForeignKey with category]
 - name
 - qunatity
 - price  
 - description
+----------------------+

+----------------------+
6. **Cart**
+----------------------+
 - id
 - user      
 - food           [OneToOneField with food]
 - qunatity       [Quantity of user want to buy]
 - price          
+----------------------+

+----------------------+
7. **Order**
+----------------------+
 - id
 - user    
 - restaurant     [OneToOne with restaurant]
 - date           [Date  and time of order]
 - total_price 
+----------------------+

+----------------------+
8. **Orderitem**
+----------------------+
 - id
 - order          [ForeigKey with Order]
 - food           [OneToOne with food]
 - qunatity       [Quantity of user want to buy]
 - price
+----------------------+
