# Data Cleaning and Visualization Challenge for Synapse

You have beend given some data in the _data.json_ file, clean the data if necessary and create a visualization to help determine what segment of users would be interested in a new bicycle project.

## Your task

A user has a new concept for a 3-speed bicycle made from recycled parts with a $20 price point. He wants to send a push notification to other interested people on the internet, prompting them to fund the project. However, he doesn't want to send a message to everyone, only those who they think would be interested.

That's where you come in. You're a resident data expert. You'd like to create a visualization that helps answer: what kinds of users would be interested in the bicycle project?

Luckily, you've been collecting analytics data on who would be interested to fund projects based on attributes like location, age range, gender, and mobile device.

## The Data

Your analytics software tracks the events: "View Project" and "Fund Project," for when a user views details about a project and for when they fund a project. The events also have the following attributes:
* `category`: what the project is about, e.g. "Sports", "Fashion", "Technology", etc.
* `client_time`: a UNIX timestamp of when the event occurred.
* `amount`: how much the user donated (for "Fund Project" only)

*Note:* The bicycle project belongs to two categories: "Sports" and "Environment."

Additionally, you know some information about each user on your site, that they supplied in a survey when they signed up. Specifically, you know:

* `session_id`: unique identifier for each user
* `age range`: one of ['18-24', '25-34', '35-44', '45-54', '55+']
* `gender`: one of ['M', 'F', 'U']
* `location`:
 * `city`: a city in the United States
 * `state`: a state in the United States
 * `latitude`
 * `longitude`
* `marital_status`: one of ['single', 'married']
* `device`: one of ['iOS', 'android']

From past experiments, you know that each user generally likes projects from the same category. For example, User A almost always views and funds projects from the "Technology" category. The bicycle project belongs to two categories: "Sports" and "Environment."

You have a sampled time series of 50,000 events from one month this year in a JSON blob. User data is added into every event.

Here's an example of two events by the same user:

    {
      "event_name": "View Project",
      "gender": "M",
      "marital_status": "single",
      "session_id": "98ccfbe8c29845c0a44f8e56213d1def",
      "device": "android",
      "category": "Technology",
      "age": "25-34",
      "client_time": 1393632024,
      "location": {
        "latitude": 33.786594,
        "city": "Covina",
        "state": "CA",
        "longitude": -118.298662,
        "zip_code": "91723"
      }
    }

    {
      "event_name": "Fund Project",
      "gender": "M",
      "marital_status": "single",
      "session_id": "98ccfbe8c29845c0a44f8e56213d1def",
      "device": "android",
      "amount": 20,
      "category": "Technology",
      "age": "25-34",
      "client_time": 1393632301,
      "location": {
        "latitude": 33.786594,
        "city": "Covina",
        "state": "CA",
        "longitude": -118.298662,
        "zip_code": "91723"
      }
    }

## Your submission

Once again, you want to create a visualization after cleaning the data, that answers: what segments of users would be interested in the bicycle project? Based on your visualization.

You can create any kind of visualization that you think best answers the question. e.g. static or interactive, using python. Feel free to use any tools you're familiar with, or try out that new data viz library you heard about.
