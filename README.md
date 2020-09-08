<h2> Shopify Data Science Challenge
<h3> Created by Mohammad Mushfequr Rahman
<h3> Email: mohammadmushfequr.rahman@ontariotechu.net



<h4> Answers to question are availble via the jupyter notebook and the pdf copy. 

        To run the notebook please ensure that you have jupyter and pandas. Completed using python 3. to start the jupyter server go to the terminal in the working directory and type 

            jupyter notebook 


<h4> Answers to question 2: 
Part a 

        SELECT S.ShipperName ,COUNT (OrderID)  Orders
        FROM Orders O, Shippers S
        WHERE O.ShipperID= S.ShipperID AND S.ShipperName="Speedy Express"

Answer: 


 | ShipperName | Orders |
 |------------ | ----------|
 | Speedy Express  |  54   |

 Part B: 

        SELECT LastName, COUNT(O.EmployeeID)
        FROM Employees E, Orders O
        WHERE O.EmployeeID == E.EmployeeID
        GROUP BY (O.EmployeeID)
        ORDER BY 2 DESC
        LIMIT 1;
Answer

| Last Name| Sales|
 |------------ | ----------|
 | Peacock  |  40  |

Part C: 

        SELECT P.ProductName, SUM(OD.Quantity) TotalOrders FROM Customers c
        JOIN Orders O
        ON c.CustomerID = O.CustomerID
        JOIN OrderDetails OD
        ON  O.OrderID = OD.OrderID
        JOIN Products P

Answer:

| ProductName| TotalOrders |
 |------------ | ----------|
 | Boston Crab Meat |  160  |

