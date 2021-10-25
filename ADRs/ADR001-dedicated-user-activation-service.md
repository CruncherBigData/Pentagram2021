# ADR_01: A dedicated user activation service subscribing to purchase events from Farmacy Foods

# Status: 
Proposed

# Rationale:
A primary goal of the project is converting transactational customers to Farmacy Family engaged customers. Farmacy Foods publishes all purchase transactions to a kafka stream. We need to use these events to reach out to potential candidates for Farmacy Family. There isn't a lot of processing we need to do on this event other than store the user information and forward the information to a notification service to send emails to users who complete a transaction. The benefit of a dedicated service comes from the extensibility that it will provide for the following functionality

1. Keep track of who has already been activated 

2. When we reached out to the customer last time to avoid being too pushy 

3. Also to keep track of how active a customer is

4. It could also provide additional API. For example, to find most active users 


Alternatives that can be considered are

1. A batch job that is schedule to run every night or twice a day reading from the same kafka stream and extracting the email and user info and forwarding that to a notification service to send out emails like the service would do

2. We could also have a serverless function (AWS lambda or Azure function) listen on the Kafka Stream and do a store and forward. This would work well for this scenario as well 


# Decision



# Consequences:

