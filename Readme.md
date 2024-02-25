# Airline Booking System
## Objective
 We need to build a backend system that can support different features for an airline company.
 Our end  user is going to be someone who wants to book flights and query about flights so we need a robust
 system to actually help them give the best experience possible. This doc is solely going to focus on the 
 backend part of the the system. We want to prepare the whole backend keeping the fact in mind that the code base
 should be as maintainable as possible.

## Functional Requirements
  - A user should be able to search for flights from one place to another.
      - User should be able to select the data of the journey.
      - Able to mention the source and destination details.
      - [v2] Roundway, Multicity booking functionality.
      - Able to select the class of the flights [Not mandatory].
      - Able to select number of seats to book.
      - Show the best flights based on  minimum time and cost.
      - Pagination and filters based on price, time etc. 
  - A user should be able to book a flight considering that user is registered.
      - User should be able to cancel a booking and then based on some criteria we can intiate a refund for them.
      - Avle to request and book excess luggage for every flight.
  - For making a booking, the user has to make a payment [dummy].
  - User should be able to list there previous and upcomming flights.
  - Should be able to download Doarding pass if they have done online checkin.
  - Notifications via email for completing online checkin before 3 hours of departure.
  - Notification to users about delay in booked flights.
  - Users should be abel to review the flights journey if and only if they have booked a flight.
    - Rating along with comment.
    - while listing also show the review of the flight.     
  - Tracking flight prices should be possible, the user should be notified about any changes in price, time delay etc.
  - Listing FAQs
      - [v2] Prepare seat selections
  - Coupons for discounta and offers.
  - While making a bookin a person can reserve more than one seat.

## Non Functional Requirements
  - we can expect that we are getting more searches than bookings.
  - The system needs to be accurate in terms of booking.
  - Expect that we will be having approx 1,00,000 total users and 5,00,000 bookings might come up in one quater.
  - So in one day we can expect 10000 bookings.
  - - System should be capable to scaling up to at least 3x the current estimated traffic.
  - The system should handle real time updates to flight prices, before the user makes the final booking.
  - Concurrency should be handled using RDBMS should be the good solution.

### Capacity Estimation
- Storage extimates
  - for upcoming 5 years, 80,00,000 bookings, 2,00,000 Users, Considering  all the users records and booking take 10 MB of data then overall 10 TB of memory should be fine for our pilot run.
- Traffic extimatses -if we consider 30:1 as the search:booking ratio, then at max we expect 150000 search queries a day. 2 query/s


    # High level system design
  (there are many things but this is just to get the gist of it)
<div style=" margin: 10px; position: relative;"><img allowfullscreen frameborder="0" style="width:640px; height:480px" src="https://lucid.app/publicSegments/view/585a058f-f58d-4a97-91b3-a4727b3b2392/image.png" id="J~.dWY.sDlVO"></img></div>

### Search and Flights Service
 - Create Flights
 - Delete Flights
 - Update Flights
 - Search for Flights
     - Based on multiple criteria we can search for flights
     - pagination








***This doc is required so that you have clear view of what will be the project and its features (needed in good companies).***
