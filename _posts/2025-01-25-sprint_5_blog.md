---
layout: post
title: Create Performance Task Blog
permalink: /sprint5
comments: true
---

### Individual Feature: Event Calendar

My feature focuses on an event calendar where users can:
1. **Add events** by specifying details such as name, location, and date.
2. **View upcoming events** displayed in an organized and user-friendly calendar interface. 

This feature provides users with a visual and interactive way to keep track of their schedules.

---
### Lists, Dictionaries, and Database

- **Lists (Rows)**: Queries from the database retrieve rows of event data as Python objects. These rows are used to populate the calendar. We use a third-party library, SQLAlchemy, to perform the queries.
![ 1]({{ site.baseurl }}/images/1.png)


- **Dictionaries (Columns)**: Each row (event) is converted into a dictionary with keys matching database column names usingr read ():
    ![ 2]({{ site.baseurl }}/images/2.png)

- **Formatting Response Data (JSON) from API into DOM**

  - **The API returns event data in JSON format. After receiving the JSON data, it is formatted and displayed in the DOM using JavaScript.**
     ![ 3]({{ site.baseurl }}/images/3.png)


- **Methods in the "Class" to Work with Columns (CRUD Operations)**

  - **Create**: Add a new event to the database.
     ![ 4]({{ site.baseurl }}/images/4.png)

  - **Read**: Retrieve event data from the database (already covered above with the query).

  - **Update**: Modify event data in the database.
     ![ 5]({{ site.baseurl }}/images/5.png)

  - **Delete**: Remove an event from the database.
     ![ 6]({{ site.baseurl }}/images/6.png)



---
## Algorithmic Code

### API Class for CRUD Operations

The API class in the code defines the necessary HTTP methods (POST, GET, PUT, DELETE) to handle requests for the events data. Here’s how each method is defined:

![7]({{ site.baseurl }}/images/7.png)

- **POST**: Creates a new event and saves it to the database. It uses the request body data (event name, location, and date) to generate the event and store it in the database.
- **GET**: Retrieves a single event by its ID, returning the event data as a JSON response.
- **PUT**: Updates an existing event's details. The request data specifies which fields (e.g., name, location, date) should be updated.
- **DELETE**: Deletes an event by its ID.

### Method/Procedure with Sequencing, Selection, and Iteration

The `post()` method handles event creation, which involves **sequencing**, **selection**, and **iteration**:

#### Sequencing
The steps are executed in a specific order:

1. **Check for Required Fields**: The method first checks if the required fields (`name`, `location`, `date`) are present in the incoming request. If any are missing, it returns an error response.
2. **Validate Date Format**: The method validates the date format using the `datetime.strptime()` function. If the date format is invalid, it returns an error message specifying the correct format.
3. **Create Event Object**: If all fields are valid, an `Event` object is instantiated using the data from the request.
4. **Save Event to Database**: The `create()` method is then called on the `Event` object to store it in the database.

#### Selection
Selection is used to determine what action to take based on the input:

- If any required fields are missing or invalid, the method returns an error message.
- If all data is valid, it proceeds to create and store the event.

#### Iteration
The `get()` method for retrieving all events by user ID demonstrates iteration. It fetches all the events from the database and iterates over them to generate a list of their JSON representations:

- The `Event.query.all()` fetches all events from the database.
- The method then iterates through the fetched events, using a list comprehension, to generate a JSON response containing the data for each event.

![8]({{ site.baseurl }}/images/8.png)

In this case, the method iterates over the events to create a list of their JSON representations, which is then returned as the response.

### Parameters (Request Body) and Return Type (JSONify)

#### Parameters
The parameters for the **POST**, **PUT**, and **DELETE** methods are obtained from the request body. This is done using `request.get_json()`. 

For example, in the **POST** method, the expected parameters are:

- **name**: The name of the event.
- **location**: The location of the event.
- **date**: The date of the event.

#### Return Type
The methods return a **JSON** response using `jsonify()`:

- **POST**: After creating an event, the `post()` method returns the newly created event's data as JSON:
  ![9]({{ site.baseurl }}/images/9.png)

- **GET**: The `get()` method returns the event data as JSON.

- **PUT**: After updating the event, the `put()` method returns the updated event data as JSON.

- **DELETE**: The `delete()` method returns a JSON message confirming the deletion of the event.


<!-- ## Calling Algorithms
 document.addEventListener('DOMContentLoaded', function() {
      getUserId(pythonURI)  // Get user ID first
          .then(userId => {
              if (userId) {
                  getUserEvents(userId)  // Fetch events based on user ID
                      .then(fetchedEvents => {
                          events = fetchedEvents;  // Store events globally
                          renderCalendar(events);  // Pass events to the calendar
                          renderSidebar(events);   // Pass events to the sidebar
                      })
                      .catch(err => console.error("Error fetching events: ", err));
              }
          })
          .catch(err => {
              console.error("Error fetching user ID: ", err);
          });

          Handling Responses: The frontend updates the calendar or displays error messages based on the response.
 -->
