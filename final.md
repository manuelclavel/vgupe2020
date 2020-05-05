# Final classroom  exercise (due on May 5,  2020, at 1pm) #
## Problem ##
The Consortium (client) has decided the following:

1. The players can buy "10-booking cards". A player may buy
as many "10-booking cards" as he/she wish.
2. A "10-booking card" has a 30-days validity period. The beginning
of the Valry period is the day when the card is bought.
3. A "10-booking card" can be used by its owner
to make a booking (in any court, of any sport centre, of any city
within the consortium),  with the following conditions:
- the day of the booking (i.e., the day the player intends to play)
must fall within the card's validity period.
- the card must have at least one "unused" booking, i.e., 
the number of bookings currently "linked" to the card must be less than 10. 
4. When a player uses a "10-booking card" to make a
booking, the booking is automatically "payed".
5. When a player cancel a booking, if the booking was "linked" to a 
"10-booking card", then it is also "unlinked", i.e., the card has one more
"unused" booking.
6. The previous restriction about "no more than 3 bookings
in advanced" does not apply for bookings currently 
"linked" to a "10-booking card", i.e., bookings
"linked" to a "10-booking card does not count as "advanced" bookings.
7. The previous restriction about "no advance booking if there are
unpaid bookings" does not apply for bookings currently 
"linked" to a "10-booking card".
8. All the other constraints regarding booking creation
remain the same. 

## Task ## 

- Adapt your application to the new requirements. In
particular, when making a booking, the player should be able to select
a "10-booking card", among the ones that he/she owns (if any), and
make the booking using the selected card.

- However, ** do not ** develop a module for buying/selling/managing
"10-booking cards" 


# Final project (due on May 5, 2020, at 8.45am) #
## Basic Description ##
A mobile app (for Android) for booking online badminton courts

## Initial requirements ##

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

## Main functionality ##

### For users/badminton players: ###
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

