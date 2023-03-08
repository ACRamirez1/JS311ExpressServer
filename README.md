# JS311ExpressServer

JS 311 Notes

Back-End
- always running
- listening to requests

Request 
*** verb (GET, PUT, POST, DELETE)
- URL or domain - google.com or amazon.com
*** route - what comes after /      /features/actions
- query (sometimes) the stuff after the ?        https://iamprogrammer!!:2021,hereicome!!@js211-8week-ebook.herokuapp.com/module-4/class-14/
- body (sometimes)
- header (sometimes for extra options or paramaters) we wont do much with this. 

Response
*** body
*** response code 
- header (usually don't care about this)

Status codes
- 100's are INFORMATIONAL RESPONSES. This is just information given to you for the project you are working on. 
- we are looking for something in the 200's. 
- 100's and 200's are good
- 300's are okay, it is just telling you if something has been moved. It is a REDIRECTION MESSAGE. 
- 400's are CLIENT ERROR RESPONSE. This means that this is our fault, not the customers fault.
- 500's are SERVER ERROR RESPONSES. This is the servers fault, and therefore could be the customers fault. Back end issue. 
-- Sometimes it could be your fault. 



When we are working on the computer, we are the SERVER. 


Class 3 

thruthy and falsey

false values
    0
    undefined
    NaN
    flase
    empty strings '' ""
    null

    everything else is true
    *************************

    We're going to build our own todo app with our own api interface and our own data.

    We're building a todo back end and here is what we want to support:

    We want 5 routes
        - we want a route that returs all of the todos in our list
            GET /todos
                return an array of all todo objects

        - we want a route that returns a single todo based on the id provided
            GET /todo/:id
                :id is the id of the todo to return if it exists.
                if else, return message("ID not found")

        - we want a route that will delete a single todo based on the id provided
            DELETE /todos/:id
                :id is the id of the todo that was deleted.
                return message("Item was deleted")

        - we want a route that adds a single todo to the list
            POST /new/todos
                body should include an object that has at least a description
                we're going to make a function that generates a random id that's added
                    when the new todo is created.
                ex: body: {"description": "feed the dog",
                            "completed": false}

        - we want a route that updates an existing todo based on the id provided
            PUT /todos/:id
                ex: /todos/10, body= {"description": "buy groceries", "completed": true}

        POST and PUT use the body.

        todo objects should have:
            - id: id of the todo items 
            - description: what the do is
            - completed: true or false

********************************

How we're going to generate a random id

Math.random()  //generate a random number between 0 and 1
// it will NEVER return 1.

math.floor() rounds down to the whole number
math.ceil() rounds up to the whole number

