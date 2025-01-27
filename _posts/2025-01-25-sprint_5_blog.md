---
layout: post
title: Create Performance Task Blog
permalink: /sprint5
comments: true
---

## CPT Blog

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
<!-- ## Algorithmic Code

The API class defines methods for GET, POST, PUT, and DELETE requests. For example:


@app.route('/api/events', methods=['POST'])
def create_event():
    data = request.get_json()
    name = data['name']
    location = data['location']
    date = data['date']
    # Add event to database
    cursor.execute("INSERT INTO events (name, location, date) VALUES (?, ?, ?)", (name, location, date))
    db.commit()
    return jsonify({ "message": "Event created", "id": cursor.lastrowid })

Method with Sequencing, Selection, and Iteration

The create_event method uses:
1. Sequencing: Processes the incoming request data step-by-step.
2. Selection: Validates inputs and handles errors if fields are missing.
3. Iteration: Iterates over results when returning a list of events.

Parameters and Return Types
- Parameters: JSON body of the request (e.g., { "name": "Meeting" }).
- Return Type: JSON response using jsonify.

## Calling Algorithms
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
