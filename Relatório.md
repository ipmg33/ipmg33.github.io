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
    - [Setup a store](#setup-a-store)

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

For this action the user must enter a username, email and password. The objective is register the new user in the system's database.
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

### Call the next costumer

### Setup a store