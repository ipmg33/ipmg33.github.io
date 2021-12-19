# Stage 4: Functional prototype 

- [Stage 4: Functional prototype](#stage-4-functional-prototype)
  - [**URL**](#url)
  - [**Startup instructions**](#startup-instructions)
  - [**Briefing**](#briefing)
  - [**Scenarios**](#scenarios)
    - [*1st Scenario*](#1st-scenario)
    - [*2nd Scenario*](#2nd-scenario)
    - [*3rd Scenario*](#3rd-scenario)
    - [*4th Scenario*](#4th-scenario)
  - [**Incomplete Parts**](#incomplete-parts)
  - [**Tools**](#tools)

<br>

## **URL**
<br>

**Mobile App** : https://drive.google.com/file/d/1gRkxTj2Toksts-6WCo5WUm4shTdjzFj/view?usp=sharing <br>
**Back-office** : http://casaventura.asuscomm.com:4200/

<br>
<br>

## **Startup instructions**
<br>
Our system is built in two different platforms with different goals, the mobile app
(developed using android 5.4) for final users and a web app (developed using
angular) for the business manager. <br><br>
Download the apk, only works in android phones with android 5.4 or higher, if for
some reason you don’t have an android phone available we recommend using blue
stacks. It is an android emulator that works just like a tablet for instance. <br>(https://www.bluestacks.com/download.html) <br><br>
The back-office is a simple browser application. <br>
For both you need internet. 

<br>
<br>

## **Briefing**
<br>
Our system has the goal to manage the number taken in stores, by giving clients
the information of what number is currently being seen and the estimated time to
be seen, which will help people to do anything in the meantime. <br> <br> It also will provide
statistics that the store manager can use to better help the venue, statistics such as
the average waiting time by department and number of tickets seen by
department. 

<br>
<br>

## **Scenarios**
<br>

### *1st Scenario*
You need bread, and you are near Sintra. <br> The objective is for you to take a ticket for
"Peixaria" in the "Loja Sintra".

<br><br>

### *2nd Scenario*
You are now the manager of all the stores in samevensa’s system go to the backoffice and call the ticket of “Peixaria” in “Loja Sintra”. 

<br><br>

### *3rd Scenario*
You want to see if you have enough time to go to some store before your upcoming
ticket. <br> The objective is to check how much estimated time you have to wait for
your "Peixaria" in "Loja de Sintra" ticket.

<br><br>

### *4th Scenario*
You want to retrace your steps from a previous day when you went to a certain
shop. <br> Check how much time you spent waiting for your "Peixaria" in "Loja de
Sintra" ticket.

<br><br>

## **Incomplete Parts**
<br>
Our computational prototype isn't fully functional considering its purpose. <br><br> Don't
expect the waiting times to add up, nor the ticket (senha) numbers to be
sequential. <br><br> The numbers that show up in the dropdown panels are totally
representative, however our database returns true values. But they’re not
consistent with what is shown. 

<br>

<img src="./img/Stage4/InconsistentPart.PNG" alt="app" width="400"/>

<br>

As you can see, the number of the ticket is '0', and the current ticket being attended
is 8 which is absurd. <br><br> Also, we previously mentioned a QR code ticket management,
however we haven't implemented that yet. <br><br> **The prototype is meant to give the user
a feel of what a real situation would look like.**

<br><br>

## **Tools**

<br>

>- Android studio, using Java as the main language to manipulate the data and 
construct the program logic and using our own mobile phones (we also used the
emulator on the pc) to test the app.

<br>

>- For the management site, we used Visual Studio Code as our IDE, and Angular for
the front-end back-end manipulation.

<br>

>- For the database we used MongoDB to store all the data in our application (tickets,
departments, user info).

<br>

>- We also used python to make a websocket.


