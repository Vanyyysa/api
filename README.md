"# api" 

JSON POST with Database Integration

Clients can use this JSON POST API endpoint to provide structured data to a server in order to create or change records. The request body sends JSON data, which makes it versatile and simple to work with. After processing, the server delivers an HTTP status code and any required JSON. It can be used for secure user registration, data changes, and bespoke workflows. Endpoint requirements and error-handling processes should be documented properly.

 


## API
API simplifies operations by providing real-time communication, easy data management, and secure connectivity with third-party services. It enables developers to create adaptable and efficient applications by providing strong authentication, scalable architecture, and extensive documentation. API provides expanded functionality and increased user interaction.

PURPOSE: 
API is designed to simplify difficult operations and improve the functionality of your apps. Our API provides a broad collection of tools to expedite operations, improve user experience, and promote productivity whether you are constructing a website, mobile app, or any other program.

Key Features:

Data Administration:

- Use our API to easily store, retrieve, and manage data. It supports a wide range of data kinds and formats, ensuring compatibility with many systems.
- Protocols for secure data transfer and storage to protect sensitive information.

Authorization and authentication:

- Protect your API endpoints by implementing secure user authentication and permission processes.
-Fine-grained access control based on roles and permissions to limit user activity.

Communication in Real Time:

- Allow users to communicate in real time with features such as instant messaging, notifications, and live updates.
- WebSockets and other real-time data exchange protocols.

Third-party Service Integration:

- Integrate seamlessly with popular third-party services, allowing you to access external functionality without leaving your application.
- Social networking, payment gateways, mapping services, and other related services.

Reporting and analytics:

- Create comprehensive analytics and reports to acquire useful insights into user behavior, system performance, and other critical data.
- Reporting tools that can be customized to visualize data based on your individual needs.

Scalability and dependability

- Highly scalable architecture to meet expanding user demands while maintaining performance.
-Redundancy and failover methods to provide continuous service even when servers fail.

Documentation and assistance:

- Extensive API documentation, including endpoints, request methods, and response formats in detail.
-Professional customer service to assist you with API integration, issue resolution, and upgrades.

Security:

- Use industry-standard security protocols like HTTPS, OAuth, and API keys.
- Security audits and updates on a regular basis to protect against emerging threats.

Customization:

- Tailor API endpoints and functionalities to your individual use case and business needs.
- Flexible configuration options for tailoring the API to the specific requirements of your application.

Handling Errors:

- Error messages that are clear and succinct to aid in debugging and troubleshooting.
- Predictive error handling to resolve anticipated difficulties ahead of time.

API is intended to help developers, businesses, and entrepreneurs by providing a solid foundation for their apps. Our API is the key to unlocking endless possibilities whether you are developing a social networking platform, an e-commerce website, or a productivity software. With our API, you can now enjoy better functionality, increased user engagement, and unprecedented efficiency.


## API
Endpoints


AVAILABLE ENDPOINTS, THEIR FUNCTIONS, AND THE REQUIRED INPUTS.

http://127.0.0.1/api/public/postName

The purpose of this endpoint is to add new information to the database.
Required Parameters: First name (fname), Last name (lname).

http://127.0.0.1/api/public/postUpdate

The purpose of this endpoint is to alter existing data in the database.
Required Parameters: ID, First name (fname), Last name (lname).

http://127.0.0.1/api/public/postPrint

The purpose of this endpoint is to display the data saved in the database.
Required Parameters: None.

http://127.0.0.1/api/public/postDelete

The purpose of this endpoint is to remove specified data from the database.
Required Parameters: ID.


## Request
Payload


Explain the
structure of the request payload, including any required or optional fields.
You can use JSON examples to illustrate.


 


## Response


Describe the
structure of the API response, including possible status codes and JSON
examples.

Request payload:
 {
"lname":"hortizuela",
"fname":"manny"
 }

This payload is used to add a new name record to the database. It requires both the person's surname name ("lname") and first name ("fname").

## JSON Payload printName:
 
Request payload:

There are no special fields in this payload. It might be used to retrieve or print a name from the system, but there are no necessary or optional fields specified in the payload.

## JSON Payload name change:

 Request payload:
 {
"id":1, 
"lname":"wick", 
"fname":"john" 
}

This payload is used to update an existing name entry identified by the "id" parameter. It requires the person's most recent last name ("lname") and first name ("fname").

## JSON Payload deleteName:
Request payload:
{
  "id":1
}


This payload is used to delete a name record based on the "id" value given. It simply takes the deletion of the name entry's unique identifier.

## Response

## JSON Payload postName:

- Response payload:
{
         "status":"success","data":null
}
"status": This property indicates the status of the API call. It's "success" in this case, indicating that the request was successful.
"data": This parameter is present but set to null, indicating that for successful postName requests, no specific data is returned.

## JSON Payload printName:

- Response payload:
{
         "status":"success","data":["lname":"hortizuela","fname":"manny","lname":"licayan","fname":"arnold"]
}

"status": This property indicates the status of the API call. The word "success" indicates that the request was granted.
"data": An array of objects, each of which represents a name entry. Each object has equivalent "lname" (last name) and "fname" (first name) fields. The response has several name entries.


## JSON Payload updateName:

Response payload:
{
         "status":"success","data":null
}

"status": This property indicates the status of the API call. The word "success" indicates that the request was granted.
"data": This field is available but set to null, indicating that for successful updateName requests, no specific data is returned.


## JSON Payload deleteName:

- Response payload:
{
         "status":"success","data":null
}


"status": This property indicates the status of the API call. The word "success" indicates that the request was granted.
"data": This parameter is available but set to null, indicating that for successful deleteName requests, no specific data is returned.


## Usage

To alter database information using Postman and the API endpoints, follow these steps:



1. Start Postman:

Check that Postman is installed and running on your system.



2. Insert data by sending a POST request:

To insert data into the database using the /api/public/postName endpoint, do the following:



Choose the HTTP method as POST.

Enter the following URL: http://127.0.0.1/api/public/postName.

Within the request body, include the parameters fname and lname, as well as the values to be inserted.

To send the request, press the "Send" button.



3. Make a POST request to update the data:

Using the /api/public/postUpdate endpoint, you can update existing database entries:



POST is the HTTP method to use.

Enter the following address: http://127.0.0.1/api/public/postUpdate.

Include the revised values for the parameters id, fname, and lname in the request body.

To submit the request, press the "Send" button.



4. Send a POST Request to Print Data:

Using the /api/public/postPrint endpoint to display database data:



Opt for the HTTP method as POST.

Enter the following URL: http://127.0.0.1/api/public/postPrint.

Because no extra parameters are required, leave the request body empty.

To send the request, press the "Send" button.



5. Delete Data with a POST Request:

Using the /api/public/postDelete endpoint, you can erase data from the database:



Set the HTTP method to POST.

Enter the following address: http://127.0.0.1/api/public/postDelete.

Include the parameter id with the ID of the data you want to delete in the request body.



To start the request, use the "Send" button.




## License


No License 


## Contributors

Sir Manny Hortizuela
provided:

- some codes
- database structure
- payloads
- etc.


## Contact
Include contact
information for inquiries or support.

Vanesa May S. Salvador
- vanesasalvador2705@gmail.com
- vanessa.salvador@student.dmmmsu.edu.ph
- 09619940099


