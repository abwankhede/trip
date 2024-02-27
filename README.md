# trip
Application for Train ticket from London to France

For the Requested functionalities, we need to design the following APIs:

**Submit Ticket Purchase API:**

**Endpoint 1**: /purchase-ticket
Method: POST
Request Body:
text

{
"from": "London",
"to": "France",
"user": {
"firstName": "John",
"lastName": "Doe",
"email": "johndoe@example.com"
},
"pricePaid": 20
}

**Response**: Receipt details including the above information.
View Receipt Details API:

**Endpoint 2**: /receipt-details/{userId}
Method: GET
Request Parameters: userId (or unique ticket identifier)

**Response**: Detailed receipt information for the given user.
View Users and Allocated Seats by Section API:

**Endpoint 3**: /users-and-seats
Method: GET
Request Parameters:
Section: A or B

**Response**: List of users and their allocated seats in the requested section.
Remove User from the Train API:

**Endpoint 4**: /remove-user/{userId}
Method: DELETE
Request Parameters: userId (or unique ticket identifier)

**Response**: Confirmation of the user's removal from the train.
Modify User's Seat API:

**Endpoint 5**: /modify-seat/{userId}
Method: PUT
Request Parameters: userId (or unique ticket identifier)
Request Body:
text

{
"newSection": "A",
"newSeatNumber": 15
}

**Response**: Confirmation of the seat modification.
These APIs would handle the process of ticket purchase, retrieval of receipt details, viewing users and their allocated seats, removing users from the train, and modifying a user's seat. Each API should be designed to handle the respective operations securely and efficiently.