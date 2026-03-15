# Untitled

Notes

INTRO
it has 3 things 
1. client
2. user
3. interface
(where client is the browser / app that connects u with server, the user is the end consumer , the interface is the page layout u can also say that it is the frontend made with js .etc), (server is a computer that is designed to store and process data )
now the question is how does our client will connect with the server , the answer is first the client sends a request to the server then the server responds back with the same thing that the client has requested with. 

HTTP,DNS AND AI
https is a protocol which helps the language issue between the user and the computer , before we send the request to the server we need to first search the server that where the DNS comes around , the computer needs an special id for it to remember each server/computer thats where the IP address comes around, DNS is domain name server , it is like internets phone book it translates the main names to IP address 
(here is how it works , first when we type a domain like [google.com](http://google.com) it first search if it knows it or else it will will asks dns for the ip which responds back with the ip, then the computer uses that ip to connect to the domain we are needed with
how does it knows what to ask for thats when API come around

API
how does the app/application actually talks with the backend that where the API actually comes around (API which is application program interface is like an waiter in a hotel the customer will ask for something and waiter will make a note of it and will tell the chef , chef will prepare and the same waiter will deliever the customer what he had asked for it is like an mediator between two parties ) in technical terms when u reload the page in instagram api will gets the new data from the server or like if user wants to know the weather the api will get the temp from the server and provides the temp to the user
API’s uses CRUD to manipulate data 
1. it uses https methods such as post, get, put,connect, delete to define what kind of action to take on a resource
2. API also have endpoint, endpoint is an URL that represents a specific resource or action in the backend ,(its like telling the waiter actuallly what u want from the menu
3. API also have headers, headers contains extra information like metadata about an request 
REQUEST BODY
when u use POST or PUT request to send a data to the server the details go in the request body usually in a JSON format so when ur creating an user u need to pass the information from frontend through an FORM to the backend API in form of an JSON, 
Response body will contain the information that the server sends in after processing what user requests for 
STATUS CODE
every API will have status code which will be like 200, 400 which represents what just happened (200 (ok)indicates that the request is successfull ,201(create) indicates a new request has been created , 400 (bad request)represents there is an error and 404(not found) represents that its not found , 500(internal server error saying that something went wrong on the server

WHAT WILL THE REQUEST ACTUALLY CONTAINS
1. method
2. header
3. body
4. end point

WHAT WILL THE SERVER RESPONDS BACK
1.status code
2.body (JSON format)

TYPES OF API 
1. RESTFULL API(representational  state transfer api)
it follows a structural way 
 database ⇒ web server ⇒ restfull api ⇒ application/website
where clients interacts using resources such as URL’s , and standard HTTP method 
RESTFULL API are stateless which means that each requests are independent of each other , they are organing and easy to implement 
2. GRAPHQL API
this provides more flexibility than restfull api , this was created by facebook 
by providing a request for user that gets them exactly by what they need instead of multiple endpoints for different data, it only uses one endpoints , the client can specify exact field they want without the user previously defining them which is a good way for complex application 

BACKEND LANGUAGE
to build API’s you need to use languages like python, ruby, java , js
you dont need to write everything from scracth , instead u can use frameworks which will provide structural foundation for building servers and handling repetitive tasks 
ex: express, hono , nestjs  ( for js ) dj ( for python ) rails ( for ruby) springs( for java)
you cant put everything in a server cause it would be expensive and for this a dedicated storage is used like databases

DATABASES 
it is just a system that stores , manages and organizes the data , u can think database as an specialized software that lives on a computer whether the device is an laptop, server, or an powerful machine in a remote data center 
they are optimized for their speed, securit and scalability , they are used for fetch, update and store the data 
TYPES
they are two types
1. Relational - stores data in a structrual way , they use SQL (table)
2. Non Relational - they dont follow any strucural so they offer more flexibility , they handle semi structural and unstructural data , NOSQL, MONGODB (document type) , redis (key- value pair) , they are for complex large data, real time data or flexibile data models (socila media apps, ot devices , big data analytics )

HOW DO DATABASE INTERACT WITH BACKEND
first the client sends a requests to the server then server processes the request then determines what data is needed , then backend sends a query to the database, then databse will return the data to the server then the server formates that data in an JSON format thenn sends it back to the client 
we use ORM instead of raw quires , orm lets us to write the query in the programming languages (prizma, drizzle for SQL and mongus for nosql data )

BACKEND ARCHITECTURE 
HOW TO STRUCTURE THE BACKEND CODE 

the whole architecture is based upon the design and structure of the app we are desiging 
according to the needs they ae divided
1. Monolithic architecture 
 in a ml architecture all compoments are combinied into a single unifited code base
simple and easy 
but can get messy as the app grows
2. microservices architecture 
in a ms architecture the application is browken down into smaller independent services
each service have each specific bussiness function
they communicate with each other via API 
3. serverless architecture 
here there is no nede for managing the servers instead the clod will manage based upon the code triggers