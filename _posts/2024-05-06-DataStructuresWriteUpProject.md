---
comments: True
layout: post
title: Data Structures Write Up 
description: Data Structures Write Up 
type: tangibles
courses: {'compsci': {'week': 30}}
---

# Collections
### Blog Python Model code and SQLite Database.

Model:
![Image](../../../images/image.png)

This is the model created for the reviews feature. This feature will allow for users to leave a review with a rating and comment. Using post and get requests, this review system can be functional. The model code above is for defining read and create methods, establishing the SQL database, and initialization of the database with two example reviews under the variables r1 and r2. The list of reviews is iterated through and added to the established database.

### From VSCode using SQLite3 Editor, show your unique collection/table in database, display rows and columns in the table of the SQLite database.

![alt text](../../../images/image1.png)

This is what the SQL database looks like. The SQL database has 31 entries, and we can see the rating and comment parameters. This database can help us, as website developers, see what can be improved in our website and go through the ratings we recieved.


### From VSCode model, show your unique code that was created to initialize table and create test data.

![alt text](../../../images/image-2.png)

This screenshot just focuses on the initialization code. The two initial reviews were ones with a rating of 5 and 4 with unique comments. These reviews were added to a list and iterated through and get added to the database as the initial reviews. This is an important step, since this is the stage of actually setting up the database and its parameters.

**APIs and JSON**
### In VSCode, show Python API code definition for request and response using GET, POST, UPDATE methods. Discuss algorithmic condition used to direct request to appropriate Python method based on request method.

![alt text](../../../images/image-3.png)

In this file the post and get requests are defined. Get requests are sent to the frontend. To break it down, a get request is a request sent to load the contents of a page when a user first opens it up. A post method is also defined, which is a request sent to the backend to add something to the data collection type set up.  In Flask, the _CRUD class defines methods for handling POST and GET requests, with each method corresponding to the respective HTTP method. Flask's routing mechanism directs requests to the appropriate method based on the HTTP method used, allowing for clear separation of logic for creating and retrieving reviews at the specified endpoint.


### In VSCode, show algorithmic conditions used to validate data on a POST condition
![alt text](../../../images/image-4.png)

Rating and comment information is extracted. If this is done correctly, data is jsonified and created in backend. If not done correctly the message: "error processing request" is sent, as there is a error 400.

### In Postman, show URL request and Body requirements for GET, POST, and UPDATE methods.
![image](https://github.com/AnvayYadav/student/assets/142522800/c1f2f103-33c4-4ec0-9661-2657bbf85c5a)
![image](https://github.com/AnvayYadav/student/assets/142522800/d2b5a5df-3b76-4a87-8da3-3a5bdac800c4)

In postman we can see how the endpoint is good for Get and Post methods.

# Lists and Dictionaries
### Blog Python API code and use of List and Dictionaries.

![alt text](../../../images/image-7.png)

The list here is used to getting all the reviews json ready.


### In VSCode using Debugger, show a list as extracted from database as Python objects.

![alt text](../../../images/imag-9.png)

Breakpoint is set up where list of objects would be extracted from the database.

# Frontend 
### Blog JavaScript API fetch code and formatting code to display JSON.

![alt text](../../../images/fertch1.png)

![alt text](../../../images/fetch2.png)

Here we can see the fetch present, which is how the frontend backend communication works. Fetching allows the frontend to send a get request to load page's contents, and send post requests when activity on the page is wanted to be added to the backend data collection. Here we can see the backend url present, which has already been tested in postman.


### In Chrome inspect, show response of JSON objects from fetch of GET, POST, and UPDATE methods.

![alt text](../../../images/image-8.png)

We can see the response of JSON objects from fetch. Fetching allows the frontend to send a get request to load page's contents, and send post requests when activity on the page is wanted to be added to the backend data collection. Here we can see the backend url present, which has already been tested in postman.

### In the Chrome browser, show a demo (GET) of obtaining an Array of JSON objects that are formatted into the browsers screen.

![alt text](../../../images/image-14.png)

Image of browser with all reviews nicely formatted inside a box created.

### In JavaScript code, show code that performs iteration and formatting of data into HTML.

![alt text](../../../images/image-12.png)

### In the Chrome browser, show a demo (POST or UPDATE) gathering and sending input and receiving a response that show update. Repeat this demo showing both success and failure.

![alt text](../../../images/image-13.png)

We can see the errors present in console. The post request isn't working when the user clicks the submit button in this screenshot, and the user is informed.

![alt text](../../../images/image-8.png)

Sucess case, everything worked gracefully in this screenshot example.

### In JavaScript code, show and describe code that handles success. Describe how code shows success to the user in the Chrome Browser screen.

![alt text](../../../images/image-15.png)

When a user submits a review through the provided form, the JavaScript function SubmitApplication() is triggered. This function gathers the review data (comment and rating) from the form, sends it to the local API endpoint via a POST request, and logs any errors or the success status of the request to the console. In a successfull case the review will be sent to the backend and a success message will be in console.

### In JavaScript code, show and describe code that handles failure. Describe how the code shows failure to the user in the Chrome Browser screen.


![alt text](../../../images/image-10.png)

![image](https://github.com/AnvayYadav/student/assets/142522800/9bd926a6-42f9-4ea1-9157-a5462aae6553)

Console will inform the user that there was an error submitting their review.


This write-up provides anoverview of the development process for a review feature within our group's Jobly website. I covered frontend and backend concepts, including Api's and modelling the database itself. The writeup includes details on setting up the SQLite database, defining API endpoints for handling GET and POST requests in Python using Flask, and demonstrating communication between frontend and backend through JavaScript fetch API. The documentation also illustrates debugging techniques, such as inspecting JSON responses and handling success and failure scenarios. This write-up was a good experience for me to get prepared for the close by AP exam.