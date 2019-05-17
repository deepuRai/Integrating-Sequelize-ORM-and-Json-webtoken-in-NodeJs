# Integrating-Sequelize-ORM-and-Json-webtoken-in-NodeJs
Download zip file and extract it. To test please follow below steps :- 


Step 1:- Register test user using below url 

http://localhost:3000/api/users and pass below paramters in body(x-www-form-urlencoded)

firstname :- test
lastname :- test
email :- test@test.com
password :- 1234
role :- 1


Step 2:- Hit login api using http://localhost:3000/api/signin to generate json token. you will see below response 

{
    "auth": true,
    "accessToken": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6MSwiaWF0IjoxNTU4MTEwMTk1LCJleHAiOjE1NTgxOTY1OTV9.jDtvXgBOdtoOHrQxHxFDpMTlhW8vkMq1yWde_hJz1VM"
}

Step 3 :- Now create a sample post using http://localhost:3000/api/post. Please send above token in header request(x-access-token -- eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6MSwiaWF0IjoxNTU4MTEwMTk1LCJleHAiOjE1NTgxOTY1OTV9.jDtvXgBOdtoOHrQxHxFDpMTlhW8vkMq1yWde_hJz1VM) and sample post data in body(x-www-form-urlencoded) with below parameter

title :- sample post title
description :- sample post description
