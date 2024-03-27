# Group 3 Project 1

# Team Name:
47114 Group 3


# Team Members:
1. Danielle Baptiste: [@dbaptiste08](https://github.com/dbaptiste08)
2. Connor Miller: [@ConnorMiller64](https://github.com/ConnorMiller64)
3. Jack Miller: [@Jackhmiller31](https://github.com/jackhmiller31)
4. Hayden Martin: [@haydentMartin](https://github.com/haydentMartin)
5. Timofei Begun: [@Conscientisehandball](https://github.com/conscientisehandball)

# Problem Description:
The task at hand is to create and model a database for a membership based tennis club. In order to use this club, members must purchase a membership and in return get access to the club’s courts which include indoor and outdoor courts, access to a variety of tournaments, lessons with a tennis coach, and orders.

# Data Model:
Explanation of data model:

Our model is used to represent a hypothetical tennis club that is membership based that is focused on the management operations, and the several services members can choose from.

Members are the heart of this tennis club, and at the tennis club they can reserve one on one lessons with the staff, which is represented with coach reservations. Since coaches are employees, we created a many to many relationship to demonstrate that members can have many different coaches and coaches can provide lessons to many different employees. These training sessions have set attributes including location and length of session.

Members can also reserve numerous different services at the tennis club. We created a facility table to demonstrate the physical spaces the tennis club has. The tennis club houses courts, restaurants, gift shops, and spas representing the attribute facility type. There is also a description attribute that describes the facility. There is a 1 to many relationship between facility and amenities because of the specific numerous services at each facility. We created two separate entities, so we could create an associative identity between members and amenities named Amenity_Reservation. Since, it is highly uncommon for a member to say reserve a whole restaurant or spa we created a many to many between amenities and members, to specify what one particular service at a particular facility.

Members have numerous payments they make to the club thus we created a one-to-many relationship specifying amount, method, and date. Since, there are items a member wishes to order from the tennis club including clothing and racquets, represented by inventorytype, we created an additional associative identity between inventory and order. We named this entity Order_Details which describes the priceEach and quantityOrdered.

Lastly, this tennis club has numerous employees. Like any good business the manager of the tennis club has details on the employees, including names and phone numbers. We created a one to many relationship between employees and employee type to expand on the attributes of said employees. EmployeeType includes information such as part-time or full-time status, the specific facility the employee works at and the pay type based on the employee’s later specifications. Since employees work at the facilities and tournaments we demonstrated this relationship by creating a one to many relationship between employees and the above two entities.


<img width="851" alt="New Model" src="https://github.com/dbaptiste08/GroupProject1/assets/149968815/6cb4a082-5280-4591-a84f-bc719ab0e3ce">




# Data Dictionary:

<img width="678" alt="Screenshot 2024-03-26 at 1 11 31 PM" src="https://github.com/dbaptiste08/GroupProject1/assets/149968815/edf0f986-fcc1-4d43-8d38-aacfea2be8c4">

<img width="681" alt="Screenshot 2024-03-26 at 1 13 06 PM" src="https://github.com/dbaptiste08/GroupProject1/assets/149968815/abe20325-b211-4f72-9012-25cad74b800f">

<img width="643" alt="Screenshot 2024-03-26 at 1 26 46 PM" src="https://github.com/dbaptiste08/GroupProject1/assets/149968815/59b65007-7275-44db-a71d-58a089a9731d">


<img width="653" alt="Screenshot 2024-03-26 at 1 17 17 PM" src="https://github.com/dbaptiste08/GroupProject1/assets/149968815/fdcd54aa-66a4-4452-a39e-9cbfe1f4fe7a">

<img width="621" alt="Screenshot 2024-03-26 at 1 19 05 PM" src="https://github.com/dbaptiste08/GroupProject1/assets/149968815/e1945be2-ca35-4e50-aedf-5e9cc0553475">

<img width="630" alt="Screenshot 2024-03-26 at 1 23 36 PM" src="https://github.com/dbaptiste08/GroupProject1/assets/149968815/aad17b20-3d80-49bf-86d0-4f6d744e5443">


<img width="646" alt="Screenshot 2024-03-26 at 1 22 57 PM" src="https://github.com/dbaptiste08/GroupProject1/assets/149968815/d7384e92-5c65-4ffa-b6fb-7329262de4ca">

<img width="674" alt="Screenshot 2024-03-26 at 1 25 43 PM" src="https://github.com/dbaptiste08/GroupProject1/assets/149968815/a3a41bef-1e30-4373-8cfd-db394dd801b4">

<img width="602" alt="Screenshot 2024-03-26 at 1 29 20 PM" src="https://github.com/dbaptiste08/GroupProject1/assets/149968815/79dd46d7-1e5b-4b2d-8f5e-99d282f967f7">


<img width="598" alt="Screenshot 2024-03-26 at 1 30 16 PM" src="https://github.com/dbaptiste08/GroupProject1/assets/149968815/353ddaf3-cf61-4e39-be79-5e3f546f8a9c">

<img width="627" alt="Screenshot 2024-03-26 at 1 30 58 PM" src="https://github.com/dbaptiste08/GroupProject1/assets/149968815/ebc749fa-fb5b-47eb-af04-d89140e44000">

<img width="600" alt="Screenshot 2024-03-26 at 1 33 21 PM" src="https://github.com/dbaptiste08/GroupProject1/assets/149968815/ef2ec6d0-0989-408c-9c6b-c737d379b23a">


# Queries:

<img width="756" alt="Screenshot 2024-03-26 at 6 04 45 PM" src="https://github.com/dbaptiste08/GroupProject1/assets/149968815/43d155da-07bb-4022-b929-c6fb679a952d">

Query 1 lists the count of employees and the type of employment that the club currently has. This query will help identify the distribution of employees across different employment types.

<img width="1269" alt="Screenshot 2024-03-26 at 6 07 19 PM" src="https://github.com/dbaptiste08/GroupProject1/assets/149968815/5ec167e5-1798-4a3d-85da-6efe8a81cb0c">

Query 1 allows managers to see how many of each type of employee they currently have. It is useful to know how many part time employees a manager has because typically they are paid less and help the organization to stay within budget. It is also useful to track the full-time employees, as they have a more steady commitment to the club, and have a more diverse skill set. 


Query 2 lists the total revenue generated for the tennis club. This number is rounded to the nearest whole number.

<img width="1270" alt="Screenshot 2024-03-26 at 6 08 19 PM" src="https://github.com/dbaptiste08/GroupProject1/assets/149968815/86fbbf9d-07f4-495b-b0bc-5eb51581a84e">

Query 2 gives the manager a more holistic view of the status of their tennis club. This allows the manager to communicate to stakeholders the performance of the club. Also, it gives a performance evaluation for the manager’s current employees.


Query 3 lists the order identification number, the status of the order, and the member receiving said order.

<img width="1269" alt="Screenshot 2024-03-26 at 6 13 37 PM" src="https://github.com/dbaptiste08/GroupProject1/assets/149968815/2ab9edcf-a13b-44e2-a4f5-df94d799ad90">

Query 3 is importatn because for a successful company to run, it is key for the customers to be satisfied. Regular communications about a shipment indicate that the company goes to lengths to ensure a customer gets their product. Which could lead to a customer, ordering another product from the tennis club in the future.


Query 4 lists out the facility type, the description of the facility, the amenity offered, and how many reservations a member has made at a particular facility.

<img width="1269" alt="Screenshot 2024-03-26 at 6 15 55 PM" src="https://github.com/dbaptiste08/GroupProject1/assets/149968815/aefcb44b-0bb8-4f4b-b62a-ada6882b27e2">

From a managerial standpoint, it is important to know which services are the most profitable in their company. The most popular services are making a reservation at a restaurant, and booking services at the spa. With this knowledge, a manger can turn a higher profit by making sure the staff are high performing, and potentially open more restaurants.


Query 5 provides the information on amount of reservations each employee is handling.

<img width="1272" alt="Screenshot 2024-03-26 at 6 17 55 PM" src="https://github.com/dbaptiste08/GroupProject1/assets/149968815/3a851988-bc15-43cc-b74b-e01e013ff97a">

This is important because the club would like to see the performance of each employee. Some employees may not be working to the standard of our club, and some may be exceeding it. The amount of reservations they are handling shows which employees are doing their share.


Query 6 helps sort our clubs most popular orders and provides how much money is spent on them by the customer.

<img width="1270" alt="Screenshot 2024-03-26 at 6 19 38 PM" src="https://github.com/dbaptiste08/GroupProject1/assets/149968815/700b3afe-c8a7-47c9-b1ab-7dd62cc9a739">

It is important to know what products are selling at higher than average rates. This will tell our club which items need to be purchased more often to keep in stock. The amount spent tells us how much money is coming in from selling these products.


Query 7 tells how many orders come from members under 30 years old.

<img width="1257" alt="Screenshot 2024-03-26 at 6 20 39 PM" src="https://github.com/dbaptiste08/GroupProject1/assets/149968815/eecf5050-1b3b-4f1f-ab3f-3b4790d1333e">

It is important for the club to look at who is ordering more items. Age is a good indicator of spending habits, and the club may be interested in pushing their advertising toward groups that are more likely to buy more from the club to increase profits.


Query 8: Gives members who participate in tournaments with an age requirement of 27 years old.

<img width="1242" alt="Screenshot 2024-03-26 at 6 22 50 PM" src="https://github.com/dbaptiste08/GroupProject1/assets/149968815/ba04b197-0699-4722-a0d0-7f9754afafc4">

Our tennis club may want to know this information, because if there are tournaments that aren't being participated in by a decent number of members, they may want to scrap the tournaments or lower the age requirement so they aren’t wasting money and reserved courts.

Query 9 lists the members name, age, phone number, and total spent.

<img width="1270" alt="Screenshot 2024-03-26 at 6 28 35 PM" src="https://github.com/dbaptiste08/GroupProject1/assets/149968815/50130a9c-4e25-4d7d-9e29-4598847783df">

This query provides management with a list of their most profitable clients. With this information, management can identify specific customers who spend the most at the club using the metric of total spent greater than $1,000 This could be useful for a manager to maximize revenue by offering rewards to said customers, and encourage their spending habits.


Query 10 lists the total raquet revenue during specific months.

<img width="1269" alt="Screenshot 2024-03-26 at 6 32 52 PM" src="https://github.com/dbaptiste08/GroupProject1/assets/149968815/0f8d3e7a-6f0e-4402-8514-787d91bd345e">

This query shows the total revenue made on the sale of tennis racquets by date. This information can be used to show the most profitable days for racquet sales and could be used to identify possible seasonality. Ideally, the CSV file from these results could be used in Microsoft Excel to visualize the information in a chart or graph. This would likely give managers the clearest idea of when racquet sales are most/least profitable. Which can aid the manager, when deciding on prices for the racquets to generate the most revenue.


# Database Information: 
Name of the database: ns_Sp24_47114_Group3

Additional information: Each query listed above is marked in the database using stored procedures which can be called using the following format (for each query replace number sequentially up to 10): CALL TP_Q1();






























