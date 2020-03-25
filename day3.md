# Day 3
## Review Day 2
- [ ] Interfaces: client-server communication; stateless protocol
- [ ] [Git: workflows](https://www.atlassian.com/git/tutorials/comparing-workflows)

## Presentations: Homework #2.1

## Discussion: Homework #2.1: _Design/describe interfaces [client-server] Presentation-Logic_

### Notes
* unique identifiers known/agreed upon by presentation/client and 
logic/server: cityId, venueId, courtId, userId/playerId, bookingId, statusId.
* success/errorCode known/agreed upon by client and server
* ordering (if any), when response is a list/array, known/agreed upon by client and server
* structure (if any), when response contains (potentially) structured data,
known/agreed upon by client and server

### _getAvailableSlots_
* __Description__: for a given day and cityId, get all the slots available:
* __security/caller__: anonymous
* __request__: getSlots(day, cityId)
* __response__: 
  * __success__: successCode + array of (centreId, venueSlots), where
venueSlots is an array of (venueId, courtSlots), where
courtSlots is an array of (courtId, slots), where
slots is an array of (startHour, endHour)
  * __error__: errorCode [Homework #3]

### _getPlayerBookings_
* __Description__: for a given day, city, and playerId, 
get all the  bookings:
* __security/caller__: callerId
* __request__: getPlayerBookings(day, cityId, playerId)
* __response__: 
  * __success__: successCode + array of (centreId, venueBookings), where
venueBookings is an array of (venueId, courtBookings), where
courtBookings is an array of (courtId, bookings), where
bookings is an array of (startHour, endHour)
  * __error__: errorCode [Homework #3]

### _getVenueBookings_
* __Description__: for a given day and venueId
get all the bookings:
* __security/caller__: callerId
* __request__: getVenueBookings(day, venueId)
* __response__: 
  * __success__: successCode + array of (courtId, bookings), where
bookings is an array of (startHour, endHour)
  * __error__: errorCode [Homework #3]

### _createBooking_
* __Description__: for a given day, court, start, end, and playerId, 
create a new booking.
* __security/caller__: callerId
* __request__: createBooking(day, courtId, start, end, playerId)
* __response__: 
  * __success__: successCode
  * __error__: errorCode [Homework #3]

### _cancelBooking_
* __Description__: for a given bookingId, cancel the booking
* __security/caller__: callerId
* __request__: cancelBooking(bookingId)
* __response__: 
  * __success__: successCode
  * __error__: errorCode [Homework #3]

### _getBookingInfo_
* __Description__: for a given bookingId, get all the booking's
information: cityId, venueId, courtId, day, start, end, playerId,
statusId.
* __security/caller__: callerId
* __request__: getBookingInfo(bookingId)
* __response__: 
  * __success__: successCode
  * __error__: errorCode [Homework #3]

### _updateBookingPaymentStatus_
* __Description__: for a given bookingId, update the booking's 
payment status
* __security/caller__: callerId
* __request__: updateBookingPaymentStatus(bookingId, statusId)
* __response__: 
  * __success__: successCode
  * __error__: errorCode [Homework #3]

### _getNameCity_/_getNameVenue_/_getNameCourt_/_getNameUser_
* Description: for a given cityId/venueId/courtId/userId,
get the corresponding name (to display)
* security/caller: callerId
* request: getNameCity(cityId)/getNameVenue(venueId)/getNameCourt(courtId)/getNameUser(userId)
* response: 
  * success: successCode + name of the cityId/venueId/courtId/userId
  * error: errorCode [Homework #3]



## Homework #3
- [ ] Test cases/scenarios [+ errors]: interfaces Presentation-Logic
- [ ] Review/Update (if needed) design/describe interfaces [client-server] 
Logic-Data 
- [ ] Review/Update (if needed) design database (Entity-Relationship Diagram)
- [ ] Review/Update (if needed) design UI (Activity diagram + mockups)