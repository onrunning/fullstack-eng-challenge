# Fullstack Engineer Use Case

## The Task:

Welcome to On's Fullstack Engineer coding challenge! To help us assess your coding skills, we'd like you to build a small application with a **Ruby backend and a Javascript framework on the frontend**.

We will provide you access to the Salesforce API with data related to On dealers. The app should:
  1. Synchronize all relevant dealers from Salesforce into its own database
   - Relevant dealers are all accounts with the field `E_Shop_Dealer__c == "Dealer and Point of Sale"`
   - Consider the case that dealers can be deleted from Salesforce
  2. Display all dealers from the local database in a list and on a map
   - The map and list should be linked: clicking on a dealer in the map should highlight it in the list and vice versa
   - The page should look acceptable on different devices

## Using the Salesforce API

Salesforce provides an API which you will use to retrieve the dealers.

For an introduction to the API: click [here](https://developer.salesforce.com/docs/atlas.en-us.api_rest.meta/api_rest/intro_what_is_rest_api.htm)

You can find the required credentials and snippet for how to connect to the api in `how_to_connect_to_sf.rb.enc`. You should have received the key to decrypt the file by email. To decrypt the file, download it locally and run the following command, replacing `ENCRYPTION_KEY` with the key. This should decrypt the file to `how_to_connect_to_sf.rb`.

```
openssl enc -k ENCRYPTION_KEY -aes256 -base64 -d -in how_to_connect_to_sf.rb.enc -out how_to_connect_to_sf.rb
```

You'll need to understand the resources in Salesforce and how they can be queried. You can find the necessary documentation [here](https://developer.salesforce.com/docs/atlas.en-us.api_rest.meta/api_rest/using_resources_working_with_searches_and_queries.htm)

The account has test data, which is ready for you to fetch.

## Salesforce Data Model

Dealers are stored as Accounts in Salesforce. The Account resource has many fields, but we're only interested in the following:
  - Id -> Unique id of the object in SF
  - E_Shop_Dealer__c -> this field is set to the value "Dealer and Point of
Sale" for all relevant dealers
  - Name -> name of the dealer
  - POS_Street__c
  - POS_City__c
  - POS_ZIP__c
  - POS_Country__c
  - POS_State__c
  - POS_Phone__c
  - Dealer_Latitude__c -> coordinate to use when displaying on map
  - Dealer_Longitude__c -> coordinate to use when displaying on map

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
