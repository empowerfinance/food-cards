# Food Me

### Introduction
For this project, you are implementing a simple card system called Food Me.
The product is simple:

* The user is shown a list of 4 cards
* Each card has a picture of food on its front, and has a title and description on its back. Each card also has a collection of tags.
* When a card is first loaded, it should display the "front" with an image. Tapping on the card flips it to its back.
* The user can tap the "Get More" button to get additional cards in their feed.
* At the top of the feed, there is a collection of filters. Tapping on one of these filters will show only the cards that match.

### Requirements

* You can use any tools or frameworks you are comfortable with to complete this task.
* The end result should be a working app + source, that can be built and run on the interviewer's machine.
* Submissions should be fully native, written in Swift.

### Design
Your team has provided you with a UI mock, seen below:

![mock](/mock/iphone_mock.png "mock")

### API Resources
You are provided with 3 endpoints:

  - [GET /cards](#get-food)
  - [GET /more](#get-more)
  - [GET /filters](#get-filters)

### GET /food

Example: https://foodcards.getsandbox.com/cards

Response body:

      [
        {
          "name": "Grilled Chicken",
          "image": "https://images.pexels.com/photos/262945/pexels-photo-262945.jpeg?auto=compress&cs=tinysrgb&h=650&w=940",
          "description": "A protein staple in many modern diets.  Healthier than the fried variety.",
          "tags": [
            "meal",
            "healthy"
          ]
        },
        {
          "name": "Fried Chicken",
          "image": "https://images.pexels.com/photos/5619/plate-white-fish-chilli.jpg?auto=compress&cs=tinysrgb&h=650&w=940",
          "description": "Chicken with a delicious crispy crust. A fan favorite.",
          "tags": [
            "meal"
          ]
        },
        ...
      ]

### GET /more

Example: https://foodcards.getsandbox.com/more

Response body:

      [
        {
          "name": "Grilled Chicken",
          "image": "https://images.pexels.com/photos/262945/pexels-photo-262945.jpeg?auto=compress&cs=tinysrgb&h=650&w=940",
          "description": "A protein staple in many modern diets.  Healthier than the fried variety.",
          "tags": [
            "meal",
            "healthy"
          ]
        },
        {
          "name": "Fried Chicken",
          "image": "https://images.pexels.com/photos/5619/plate-white-fish-chilli.jpg?auto=compress&cs=tinysrgb&h=650&w=940",
          "description": "Chicken with a delicious crispy crust. A fan favorite.",
          "tags": [
            "meal"
          ]
        },
        ...
      ]

### GET /filters

Example: https://foodcards.getsandbox.com/filters

Response body:

      [
        "meal",
        "snack",
        ...
      ]

### Extra Considerations
Here are a few things to consider as you work on this project.

* When getting "More" cards, you may get duplicates already in your set.
* Your set might not contain anything that matches a filter. How will you handle this?
* Flipping the cards will require some kind of transition or animation.
* Feel free to do some extra polishing if you want to flex your UI muscles, but don't spend too much time here.
