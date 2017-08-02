# analyticsSimulator
Simple realtime analytics simulator


 


Scenario:


Consider a website that receives 2 types of events (user login and user logout) and needs a realtime analytics system that can emit several statistics about the website traffic.



Task:

How would you design such a system, given that you need to output the following metrics about the website traffic in 10 seconds windows:

- number of unique users connected (unique user_id)

- average user session duration

At the end of the exercise, display the number of unique users since the beginnning of the simulation.

Consider offering a CLI dashboard that can emit these metrics each 10 seconds.



Notes:


  - a user can login and log out at any time

  - the order of the events is always logged in, logged out

  - the generated events have 4 fields and the following format: timestamp, event_type, user_id, session_id

  - the session_id identifies a specific user session on the site and is unique. A given user_id can generate one or more session_ids.
  
  - think of a simple implementation that should not take more than a couple of hours to complete, in the "production-ready" philosophy




Implementation details:


  - the system should be written as a simulation

  - only JDK 8 classes are allowed to be used in the implementation

  - the format of the output (dashboard) should be simple text
  
  - account for an optimal speed of ingestion from multiple sources of data
  - use the given simulation-input.csv input to test your simulation, considering that the test data has the following format: offset in seconds since start of simulation, event type, user_id, session_id
  - for receiving the website events, start the provided library that can be configured to output events in a given local directory. The simulation is successful if you can consume the events at the pace at which they are generated ( consider that you might also encounter spike periods ).




Deliverable:


  - a Java 8 command line application that simulates the website events and prints on the console the specified statistics

