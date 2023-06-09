# Listed_Assignment

**Video link to the demo:-** - https://drive.google.com/file/d/1IC85qQ0oOZV9iXpZ9AImqArcDD8ZxtIN/view?usp=sharing

This project is a Node application that sends an automated reply to new #UNREAD and #PERSONAL tagged emails. It is built using NodeJS, Express, Google OAUTH, Nodemon.

Tech Stack and Packages Used
----------
The following packages were used during the development of the Node App
1. express
2. @google-cloud/local-auth (Authentication purpose)
3. googleapis (Authentication purpose)
4. nodemon (Running the server continously).

Methodology
----------

The main methodology that has been used can be divided into 2 parts :-

1. **Authentication** - First of all we need to authenticate the user and get access to the users email to proceed.
2. **Reading User emails** - To get all the emails that the authenticated user has recieved in the previous **1 Hour**.
3. **Checking for new emails** - We need to check if the email is off type **no-reply** then we dont need to send any reply.
4. **Checking if the user has already replied** - We need to check if the user has already replied if they have we dont need to send the reply to the same email again.
5. **Constructing the message and sending** - We need to construct the message that we want to send and then proceed to send the email and then return.

Note on improvements
----------
I think there are a lot of improvements that could have been made some of them are:-
1. The app doesn't has a solid way to diffrentiate between different kinds of **do not send reply**.
2. The app can only reply to emails that were sent with **PERSONAL** tag this is because we don't have a way of diffrentiating between **do not send reply** and **professional** emails cause there may be a lot of emails which are **professional** but at the same time of **do not send reply**.

Installation
----------

1. Clone this repository using
   ```
   git clone https://github.com/pnaskardev/Listed_Assignment
   ```

2. Navigate to the Listed_Assignment folder, install the required dependencies and start the webserver on port 8000

   ```
   cd Listed_Assignment
   npm install
   ```
3. Please do add credentials.json file in order to run the app for more information please follow :- https://developers.google.com/gmail/api/quickstart/js

4. Run the Node App

   ```
    node .
   ```