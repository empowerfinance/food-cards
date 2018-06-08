# food-cards

### Introduction
For this project, you are implementing a simple food card system called food me.
The product is simple:  The user is initially show a list of 4 food cards.  

* The user is shown a list of 4 cards
* Each card has a picture of the food on the front, and has the title and description on the back. Each food item also has a collection of tags.
* When a card first loads, it displays the "front" with an image. Tapping on the card flips it to it's back.
* The user can tap the "Get More" button to get additional cards in their feed.
* At the top of the feed, there are are a collection of filters. Tapping one one of these filters will show only the cards that match.

You can use any tools or frameworks you are comfortable with to complete this task.
The end result should be a working app + source, that can be built and run on the interviewer's machine.

### Design
Your team has provided you with a UI mock, seen below:

![mock](/mock/iphone_mock.png "mock")

### API Resources
You are provided with 3 endpoints:

  - [GET /food](#get-food)
  - [GET /more](#get-more)
  - [GET /filters](#get-filters)

### GET /food

Example: http://foodcards.getsandbox.com/food

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

Example: http://foodcards.getsandbox.com/more

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

Example: http://foodcards.getsandbox.com/filters

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
