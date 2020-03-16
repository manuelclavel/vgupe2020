# Day 1
## Introduction
1. Module description
- [ ] @manuelclavel comments the description of the module
  * Project
  * Teamwork
  * __online__: teaching, but also teamwork.

## Project

### Client
* Consortium of local/city governments
### Basic Description
* A mobile app (for Android and iOS) for booking online badminton courts

### Initial requirements

* General information/constraints:
  - Cities can have several public sport centres.
  - Each sport centre can have several badminton courts.
  - Sport centres have the same operating hours: 7am to 9pm.
   - Badminton courts can be booked  either for 45 minutes, 1 hour, 1 hour and 15 minutes
or 1 hour and 30 minutes, within the operating hours, 7-days a week, all year round.
   - A user cannot book more than 3 badminton courts (in total) in advance.
   - Payments are made at the sport centres. No online payment is available.
   - If there are past booking  pending of payment, no booking in advance is allowed.
   - A user can cancel any booking (at not cost), but it must be done 
at least 24 hours before the start-time of the booking.

 
* Main functionality
  * For users/badminton players:
    - Upon selecting a city (within the consortium) and a date, 
the user can see all the __slots__ 
(i.e., badminton-court; slot-start-time; slot-end-time)
in all the sport centres in the city. Then,  
upon selecting an available slot, the user can make a __booking__, indicating 
the start-time and end-time of the booking, 
within the start-time and end-time of the slot.
     - Upon selecting a city (within the consortium) and a date, 
the user can see all his/her bookings for that date, in all the sport centres
in the city. Then, upon selecting a booking, the user can cancel it (but 
it must be done at least 24 hours before the booking-start-time).

  * For sport-centres/staff:
    - Upon selecting a date, the staff in charge can see all the bookings
for that date. Then, upon selecting a booking the staff can see:
the name of the user who made the booking, 
the booking's badminton-court, start-time, and end-time),
and the state of the booking
(paid/unpaid). Also, upon selecting a booking the staff can change
the state of the booking (from unpaid to paid and vice versa).


## Architecture

* Three-tier architecture 
  - From Wikipedia:
> Three-tier architecture is a __client-server__
> software architecture pattern in which the user interface
> (__presentation__), functional process logic (__"business rules"__), computer
> __data storage__ and __data access__ are developed and maintained as
> independent modules, most often on separate platforms.

> Apart from the usual advantages of __modular__ software with well-defined
> __interfaces__, the three-tier architecture is intended to allow any of
> the three tiers to be upgraded or replaced independently in response
> to __changes__ in requirements or technology. (...) 

> Typically, the user interface runs on a desktop PC or workstation and
> uses a standard graphical user interface, functional process logic
> that may consist of one or more separate modules running on a
> workstation or application server, and an RDBMS on a database server
> or mainframe that contains the computer data storage logic. The middle
> tier may be multitiered itself (in which case the overall architecture
> is called an "n-tier architecture").

[Three-tier architecture](https://en.wikipedia.org/wiki/Multitier_architecture#/media/File:Overview_of_a_three-tier_application_vectorVersion.svg)

* Technologies (Required)
  - Presentation tier: Swift (iOS app), Kotlin (Android app)
  - Logic tier: Java 
  - Data tier: MySQL

* IDE (Suggested)
  - Xcode for iOS development (it requires more than 4GB RAM)
  - Android Studio for Android development (it requires more than 4GB RAM)

## Teams
* Project Leader (1)
  - Coordination. Planning. Monitoring. Risk management. 
  - __Testing__: 
    - Functionality: test cases and scenarios, for each tier.
    - Integration. 
  - __Documentation__.
* Presentation tier 
  - iOS app (2)
  - Android app (2)
* Logic tier (1)
* Data tier (1)

## Evaluation
- __Project__ [functionality and other quality-related features]. 
Based on final oral presentation. Time for
each sub-team/task.  40% 
- __Project report__. Based on final document. Sections for each
sub-team/tasks 40%
- __Individual contribution__. Based on __Github activity__, and __individual
questions__ during final presentation. 20%

## Organization
1. Groups
- [ ] @manuelclavel communicates team distribution
- [ ] @manuelclavel checks that interim leader (IL) is participating.
- [ ] (IL) leader sends notification (before Thu, 19 March) to @manuelclavel about: 
    * team leader
    * members
    * sub-teams
 
2. Version control: Git repository
[git](https://guides.github.com/activities/hello-world/)

- [ ] @manuelclavel presents the module public git repository:

   -  clone with https
```unix
git clone https://github.com/manuelclavel/vgupe2020.git
```
- [ ] Each student creates his/her own github account.
- [ ] Team leader sends (before Thu, 19 March) 
to @manuelclavel the github usernames of 
the members of his/her team.
- [ ] @manuelclavel creates private repositories for each team.
- [ ] @manuelclavel will have access to the private repositories of each team.


3. Documentation: Markdown language [Compulsory]
[Markdown](https://guides.github.com/features/mastering-markdown/)

-  [ ] Learn Markdown language: 
[Markdown](https://guides.github.com/features/mastering-markdown/)

## Homework (before Thu, 19 March)
- [ ] Send by email to @manuelclavel a file (written using the Markdown language)
with the points (if any) in the initial lists of requirements that, in their opinion,
are in need of further clarification. 

## Additional recommended activities
- [ ] Get familiar with Git. 
- [ ] Depending on your sub-team/task,  start getting familiar with:
Swift,  Kotlin/Java, or  SQL. 
- [ ] Depending on your sub-team/task, set up & configure in your laptop/desktop 
your favorite IDE for iOS or Android development.


## ANNEX
### Teams
#### TeamA (7)
1. (L) Đặng Kim Bảo 
2. Bùi Xuân Phước 
3. Hoàng Văn Thiên 
4. Trần Xuân Khôi 
5. Phạm Nguyễn Thanh An 
6. Lê Minh Thư 
7. Tạ Thị Phương Liên 

#### TeamB (1-4)

1. (L) Trương Minh Hiếu 
2. Huỳnh Quang Phước Thịnh 
3. Nguyễn Trần Quang Anh 
4. Nguyễn Đình Thi 
5. Nguyễn Hữu Đức
6. Trần Hữu Lê Huy
7. Phan Nhật Nguyên

#### TeamC (1-6)

1. Huynh Duc Khai
2. Nguyen Quy Minh
3. Pham Gia Bao
4. Nguyen Cuong Phat
5. Le Dinh Trung Hieu
6. Vo Le Tung 
7. Hoàng Xuân Bắc

#### TeamD 
1. (IL) Nguyễn Bảo Duy 
2. Lưu Nguyễn Phát
3. Đinh Quý Trí Thông
4. Đoàn Hoàng Tuấn
5. Đặng Chí Công
6. Vũ Đức Hải
7. Lữ Minh Khương

#### TeamE
1. (IL) Ngô Minh Thông
2. Trần Nguyễn Quang Huy
3. Nguyễn Quỳnh Hương
4. Nguyễn Tiến Đạt
5. Tường Duy Tân 
6. Tô Trần Nhật Trường
7. Đinh Hà Nguyên


#### TeamF

1. (IL) Nguyễn Tất Đạt
2. Nguyễn Minh Hoàng
3. Nguyễn Trí Nguyên
4. Nguyễn Toàn Thắng
5. Đào Thiện Tước
6. Nguyễn Hoàng Quân
7. Bùi Nguyễn Mai Trúc
8. Trần Minh Long  



