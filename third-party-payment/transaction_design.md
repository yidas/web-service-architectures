Transaction Design
==================

Transaction Flow
----------------

1. [SQL] SELECT {Points} FROM {User_Credit} (WHERE) FOR UPDATE

2. [SQL] UPDATE {User_Credit} SET {Points} - {Used_Points} (WHERE)

3. [SQL] INSERT INTO {Orders}

4. (If it need to use credit card) Add a credit card transaction with {$total_Amount - $Used_Points} amount by API.

