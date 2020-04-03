# Final Homework #1 (Data tier) # 

## Assignment ##
Create a database for our booking app.

This database should include (at least)
the stored procedures described below.

## Deliverable ##
The expected deliverable for this homework is a zipped file 
containing:

1. the **database definition** (in MySQL)
2. the **stored procedures definitions** (in MySQL)
3. the **list of error codes with their descriptions** (in plain text).
You decide about which specific codes you will use for signaling errors.
4. the **tests** (in MySQL) that you have carried out to convince yourself
that your definitions of the stored procedures are correct. 
Each test should be a sequence of n stored-procedure calls.
For each test, the first (*n* - 1)th  calls 
serve to set the *scenario* for the test. 
Then, the *n*th call is the actual *test*. Each test should be ended
with a comment (in MySQL) indicating the *expected result*.
E.g.,

> `/* test 1 */`
> `CALL createCity("Hanoi");`
> `CALL createCity("Hanoi");`
> `/* error: CC001 */`

## Store procedures ##
### createCity(cityId) ###

The cityId is an alphanumeric character (\*). 
If there are no errors, it creates city. This city can be  
referred to (i.e., identified) later on by using cityId. 
Therefore, cityId should be unique (among cities). 

### createCityCenter(centerId, cityId) ###

The centerId and cityId are alphanumeric character (\*). 
If there are no errors, it creates a (sport) center for the
city identified by cityId. The (sport) center can be
later on referred to (i.e., identified) by using both 
cityId and centerId. Therefore, centerId should be
unique within the (sport) centers of the city identified
by cityId.

### createCityCenterCourt(courtId, cityId, centerId) ###

The courtId, cityId, and centerId are alphanumeric character (\*). 
If there are no errors, it creates a (badminton) court in the 
(sport) center identified by centerId for the
city identified by cityId. The (badminton) court can be
later on referred to (i.e., identified) by using 
cityId, centerId, and courtId. Therefore, courtId should
be unique within the (badminton) courts of the (sport) center
identified by cityId and centerId.

### createPlayer(playerId) ###

The playerId is an alphanumeric character (\*). 
If there are no errors, it creates a player. This player can be  
referred to (i.e., identified) later on by using playerId. 
Therefore, playerId should be unique (among players).

### createStaff(staffId, cityId, centerId) ###

The staffId, cityId, and centerId are alphanumeric characters (\*). 
If there are no errors, it creates a staff member of the
(sport) center identified by cityId and centerId. 
Therefore, staffId should
be unique within the staff members of the (sport) center
identified by cityId and centerId.

### createBooking(booking_id, timestamp, date, startTime, endTime, cityId, centerId, courtId, playerId) ###

The bookingId is an alphanumeric character (\*). 
The date is a string with "YYYY-MM-DD" format (i.e., a value
of MySQL type DATE).
The startTime and endTime are both strings with  "hh:mm:ss" format
(i.e., a value of MySQL type TIME).
The timestamp  is a string with "YYYY-MM-DD hh:mm:ss" format
(i.e., a value of MySQL type DATETIME).
The cityId, centerId, courtId, and playerId are 
alphanumeric characters (\*). 
If there are no errors, 
the player identified by playerId
creates an unpaid (\*\*) booking,
on the date indicate by timestamp,
for the date indicate by date (i.e., this is the date the players will play),
starting at the time indicated by startTime
and ending at the time indicated by endTime,
for the court identified by cityId, centerId, and courtId.
This booking can be referred to (i.e., identified) later on 
by using bookingId. 
Therefore, bookingId should be unique (among bookings). 

### cancelBooking(bookingId, playerId) ###
The bookingId and playerId are 
alphanumeric characters (\*). 
If there are no errors,
the player identified by playerId
cancels the booking identified
by bookingId.

### updateBookingStatus(status, bookingId, cityId, centerId, staffId) ###
The status is an integer.
The bookingId, cityId, centerId, and staffId are 
alphanumeric characters (\*). 
If there are no errors,
the staff member identified by staffId
updates the status of the booking identified
by bookingId.

___

(\*) Alphanumericals are a combination of alphabetical and numerical
characters, and is used to describe the collection of Latin letters
and Arabic digits or a text constructed from this collection.

(\*\*) 0 represents "unpaid"; 1 represents ("paid).
