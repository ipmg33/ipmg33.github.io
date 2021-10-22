# Stage 2: User and Task Analysis

## Samevensa

- [Stage 2: User and Task Analysis](#stage-2-user-and-task-analysis)
  - [Samevensa](#samevensa)
    - [Problem](#problem)
  - [Users](#users)
    - [Final consumer/user](#final-consumeruser)
    - [Clerk](#clerk)
    - [Backend Office](#backend-office)
  - [Tasks](#tasks)
    - [Register](#register)
    - [Take a number](#take-a-number)
    - [Call the next costumer](#call-the-next-costumer)
    - [Setup a venue](#setup-a-venue)
  - [Scenarios](#scenarios)

### Problem
The problem we chose to handle focuses on when people take a number in a store.
    
This is almost always not a pleasant situation, due to the fact that people tend to wait long periods of time in a queue when they could be taking advantage of it going somewhere else, saving that precious time, without having to worry about their position in the queue.

---

## Users


### Final consumer/user

This user should be able to take up to 3 numbers in diferent stores or services.
When taking a number the user can choose from a number of stores, and then, if available, choose from a set of services or type of department.
<br>We might tackle this functionality with a QRCode reading, to automatically set the number for the user.

The user will also have a list of all the numbers currently in queue. 
<br>This will allow the user to monitor where in the queue he is, the current number that is being served and the average waiting time per hour, day, week, month and year.

The last store that the user visited should also be set to default, since the location of the store might be the best geographically placed store for that user.

As the current number approaches the number of a certain user, a pop-up notification shall appear in his phone, giving the information that the queue is 3 numbers away from is own, for example.

### Clerk

The clerk will have an interface where he can call the next number in line.

If a person doesn't show up, the clerk will be able to press a different button to call the next person in line, and also give the information that the previous one didn't came.
<br>This will be usefull to measure with more accuracy the average waiting time.

Adapt each clerk to its department, meaning their screen options could be diferent according to their function.

### Backend Office

The adminstrator will have an admin interface.
<br> In this page, the backend worker will be able to manage the stores, their services, databases. 
<br>It will also provide graphics of the statistics of the stores, such as, how many people took a number from each type of service, the average wait time, the average attending time.

--- 

## Tasks

### Register

For this action the user must enter a username, email and password. The objective is to register the new user in the system's database.
<br>The user might register to the application with Google as well.
<br>As pre-conditions:

> - The username and email should be unique, in order to clearly identify each user.
> - The email can't be associated with an already registered account.
> - Password should have a minimum of 6 characters and maximum of 16 characters.
> - The username should have a maximum of 16 characters.

The back-office will then send an email to the registering user to confirm the account and if it is confirmed, the user shall be added to the database.

As exceptions:

> - If the email or username is already registered, then the registration will fail.
> - If the password confirmation doesn't match the chosen password, the registration will fail.
> - If the password doesn't have a minimum of 6 characters, the registration will fail.
> - All fields should be filled, otherwise the registration fails.

This will be a rather frequent task, but each user will just go through it once.

### Take a number

In this task the user will have registered and logged in, done that they will be presented with a choice of venues, choosing one will bring them to a new screen where they can choose the service of the number they want to take. The objective is that the user takes the number corresponding to the service they need.
<br>As pre-conditions:

> - The user must be registered and logged in.
> - The user must be within range of the venue of which they choose to take a number from.
> - The user must not have an active number () for the service they are trying to take a number from.

After that the store clerk will know there is a new customer in the queue, and the timer for them to be served starts, so that the system can estimate the average waiting time.

As exceptions:

> - If the venue is closed, taking a number will fail.
> - If the user has 3 active numbers, this task will fail.

This will be one of the most frequent tasks.

### Call the next costumer

For this task the clerk must press the "call the next number" button. The objective is to call the next number.

As pre-conditions:
<span style="color:grey"> No pre-conditions yet

Next the timer for the user to be served stops.

As exceptions:

>- The next number has to be taken.

### Setup a venue

The admin will be configure the services available in the venue for the user to take a number.

As pre-condition:

>- Service names have to be different.
>- There has to be at least one service.

After this the admin can enable the view for the user to take a number from.

As exceptions:
<span style="color:grey"> No exceptions yet

<br>

## Scenarios

>- Mr. José Luís enters Vasco da Gama’s Continente, takes a number to the charcuterie because her daughter loves their cheese.
He also needs meat for lunch, so meanwhile waiting for it’s turn at the charcuterie, he sees through our interface that the current butcher shop number is 38, and if he takes a ticket he’ll be number 59, with an average time of 3 minutes per person, and thinks “Maybe I’ll just pass in the butcher shop at Pingo Doce Olivais…”, selects the referred shop and sees that are just 5 people in queue, “Alright! When I arrive there I’ll take a number, it saves me some time and I’m in such a rush right now”, as he starts thinking on everything he has to do today, receives a notification on his smartphone that his turn has arrived.

>- Damásio Bonifácio, software engineer at a finances shop in Lisbon, has to analyse some data, such as the number of people that were attended at the shop during this last month, to show to his superior with the goal to achieve some important statistics.
Damásio is a lucky guy, since the backend office of our application stores the averages and number of customers in one of the following periods of time: week, month and year, saving a lot of time for him. He can also have permissions to make some querys to the database, for more specific information.

>- Alfredo Pais is a clerk at Intermarché’s fishmonger, that has had a busy day at his job, serving customer after customer, passing from one to another using the "Call Next Number" button, sometimes due to his tiredness, he has clicked in the button when there was no active number at the moment, receiving a message to alert him from his mistake (he can always see the amount of active numbers).



