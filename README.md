# Fullstack Engineer Use Case

## The Task:

Welcome to On's Fullstack Engineer coding challenge! To help us assess your coding skills, we'd like you to build a small application with a **Ruby backend and a Javascript framework on the frontend**. The app should fetch retailer data from an API, store it locally, and display the retailers on a map.

Breaking down the task the app should:

1. Synchronize all records from a remote system via the provided API into its own database

- Consider the case that records can be deleted in the remote system

2. Display all dealers from the local database in a list and on a map

- The map and list should be linked: clicking on a dealer in the map should highlight it in the list and vice versa
- The page should look acceptable on different devices

## The API

The fakerapi.it API is used for this challenge. It provides fake/randomized company data that can be used to simulate our retailers. To access the data use the following endpoint:

https://fakerapi.it/api/v1/companies?_seed=1&_quantity=200

A company resource has many fields, but we're only interested in the following ones:

- `name` -> name of the retailer
- `phone` -> phone number
- `addresses[0].street` -> the first address record should be used as address data
- `addresses[0].city`
- `addresses[0].zipcode`
- `addresses[0].country`
- `addresses[0].latitude` -> the first address record should be consulted for coordinates
- `addresses[0].longitude`

_Note:_ The data is completely random and does not "make sense", so it's perfectly possible that the coordinates mark a place in Europe while the country reads "Taiwan". Do not freak out about this :)

## Implementation Notes

You're free to use any Ruby framework of your choice, whether it's Rails, Sinatra, or Grape ... or no framework at all. On the frontend, please use a modern JS framework. Also good to keep in mind:

- We'll be looking more closely at the backend, so please start with that and then progress to the frontend.
- We expect you to be prepared to explain your rationale behind the decisions taken. We also expect you to provide us with your assumptions. This will help us contextualise your solution when assessing the task.
- We don't expect you to model users or handle any user authentication in this task. Do not solve this!
- We believe in open source. You're free to make use of any open source library with caution.
- We don't expect you to spend a lot of time on this task. No need to spend more than 8 hrs. Provide us with your solution even if it's incomplete. We will review it and discuss your progress with you.
- Use this task as an opportunity to show your skills ;)
- We are an open-minded team and value questions and ideas. Don’t hesitate to write us if you have any questions or remarks. We’re happy to answer all of them :)

Have fun and good luck!
