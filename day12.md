# Day 12
## Handbook review
### Module description
#### Total time of contact hours:
> 60 (40 included in class-room exercises)". 
- Last week, this week, final day.

#### Module examination
> Written project report and oral presentation
##### Final report
  - Quality Plan: testing
  - Automatic: "Unit test": test scenarios [control data], expected result

>> [From Wikipedia]
>> Unit tests are typically automated tests written 
>> and run by software developers to ensure that a section of an application 
>> (known as the "unit") meets its design and behaves as intended.

>> In procedural programming, a unit could be an entire module, 
>> but it is more commonly an individual function or procedure. 

>> In object-oriented programming, a unit is often an entire interface, 
>> such as a class, but could be an individual method.

>> By writing tests first for the smallest testable units, 
>> then the compound behaviors between those, one can build up 
>> comprehensive tests for complex applications.

#### Type and form of assessment:
>> Successful implementation of task including presentation
##### Final project/task
(see below)

## Today's class-room exercise
### Problem:
The Consortium (client) has decided the following:
1. Cities can fix their own holidays. On holidays
the sport center are closed.
2. Sport centers can fix their own opening hours,
for each day of the week. The "default" opening
hours are still 7am to 9pm, everyday of the week.
E.g., "Hanoi#001" opens on Mondays at 7am and closes at 9pm, 
but on Saturdays it opens at 9am and closes at 11pm.
"Hanoi#002", on the other hand, 
opens on Mondays at 6am and close at 8pm, and 
on Saturdays it follows the "default" schedule:
that is, from 7am to 9pm.
3. Sport centers can also fix their own "minimum length-of-playing"
(i.e, the shortest length of time a player can book).
E.g., "Hanoi#001" sets as 45 minutes the "minimum length-of-playing",
while "Hanoi#002" sets as 60 minutes the "minimum length-of-playing".
4. The "maximum length-of-playing" for all sport centres is
90 minutes. 

Moreover,
4. Clients should be able to quickly check/browse:
- For each sport center, the **applicable holidays**.
- For each sport center, for each day of the week, the **opening hours**.
- For each sport center, the "minimum length-of-playing" and the
"maximum length-of-playing".

### Task:
- Adapt your application to the new requirements.
- However, for today's exercise, 
  - **do not** develop the "holidays management module"
  - **do not** develop the "opening hours management module"
  - **do not** develop the "minimum length-of-playing management module"
  
### Submission
- Create a new branch "flexmng" in your private repository.
- Push the new code into "flexmng".

### Deadline:
- Tuesday, 28 April 2020, at 2pm.



## Final project
### Basic Description

A mobile app (for Android <del>and iOS</del>) 
for booking online badminton courts

### Initial requirements

General information/constraints:
- Cities can have several public sport centres.
- Each sport centre can have several badminton courts.
- Sport centres have the same operating hours: 7am to 9pm.
- Badminton courts can be booked either for 45 minutes, 1 hour, 
1 hour and 15 minutes or 1 hour and 30 minutes, 
within the operating hours, 7-days a week, all year round.      
- A user cannot book more than 3 badminton courts (in total) in advance.
- Payments are made at the sport centres. No online payment is available.
- If there are past booking pending of payment, no booking in advance is allowed.
- A user can cancel any booking (at not cost), 
but it must be done at least 24 hours before the start-time of the booking.

### Main functionality ###

#### For users/badminton players:
 - Upon selecting a city (within the consortium) and a date, 
 the user can see all the slots (i.e., badminton-court; 
 slot-start-time; slot-end-time) in all the sport centres in the city. 
 Then, upon selecting an available slot, the user can make a booking, 
 indicating the start-time and end-time of the booking, 
 within the start-time and end-time of the slot.
            
 - Upon selecting a city (within the consortium) and a date, 
 the user can see all his/her bookings for that date, in all the sport centres 
 in the city. Then, upon selecting a booking, the user can cancel it 
 (but it must be done at least 24 hours before the booking-start-time).

<del>        
For sport-centres/staff:
- Upon selecting a date, the staff in charge can see all the bookings 
for that date. 
Then, upon selecting a booking the staff can see: 
the name of the user who made the booking, 
the booking's badminton-court, start-time, and end-time), 
and the state of the booking (paid/unpaid). 
Also, upon selecting a booking the staff can change the state of the 
booking (from unpaid to paid and vice versa).
</del>
