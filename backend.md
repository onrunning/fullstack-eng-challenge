# Backend Engineer Use Case
#### Welcome to On's Backend Engineer coding challenge!

## The Task:


To help us assess your coding skills, we'd like you to build a small **Ruby API backend** application (as in backend for frontend).
The app should fetch the dealer data from the API, store it locally and expose it via an endpoint.

Breaking down the task the app should:

- Authenticate the clients
  - Follow the standard best practices
  - Consider rate limiting

- Provide an API endpoint to return the dealer data
  - Consider performance impacts and improvements

- Synchronize all records from a remote system via the provided API into its own database
  - Consider the case that records can be deleted or updated in the remote system

## The API

The fakerapi.it API is used for this challenge. It provides fake/randomized company data that can be used to simulate our dealers. To access the data use the following endpoint:

https://fakerapi.it/api/v1/companies?_seed=1&_quantity=200

A company resource has many fields, but we're only interested in the following ones:

- `name` -> name of the dealer
- `phone` -> phone number
- `addresses[0].street` -> the first address record should be used as address data
- `addresses[0].city`
- `addresses[0].zipcode`
- `addresses[0].country`
- `addresses[0].latitude` -> the first address record should be consulted for coordinates
- `addresses[0].longitude`

_Note:_ The data is completely random and does not "make sense", so it's perfectly possible that the coordinates mark a place in Europe while the country reads "Taiwan". Do not freak out about this :)

## Implementation Notes

You're free to use any Ruby framework of your choice, whether it's Rails, Sinatra, or Grape ... or no framework at all. Also good to keep in mind:

- Sufficient test coverage
- We expect you to be prepared to explain your rationale behind the decisions taken. We also expect you to provide us with your assumptions. This will help us contextualise your solution when assessing the task.
- We believe in open source. You're free to make use of any open source library with caution.
- We don't expect you to spend a lot of time on this task. No need to spend more than 5 hrs. Provide us with your solution even if it's incomplete. We will review it and discuss your progress with you.
- Use this task as an opportunity to show your skills ;)
- We are an open-minded team and value questions and ideas. Don’t hesitate to write us if you have any questions or remarks. We’re happy to answer all of them :)

Have fun and good luck!
