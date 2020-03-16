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

### Client (initial) requirements

* General information/constraints:
  - Cities can have several public sport centres.
  - Each sport centre can have several badminton courts
  - Sport centres have the same operating hours: 7am to 9pm,
   - Badminton courts can be booked  either for 45 minutes, 1 hour, 1h 15 minutes
or 1h 30 minutes. within the operating hours, 7-days a week, all year round.
   - A user can not book more than 3 badminton courts (in total) in advance.
   - No online payment. Payment is made at the sport centres
   - If there are past booking  pending of payment, no booking in advance is allowed.
   - A user can cancel any booking, but at least 24 hours before the start-time of the booking.
Cancel a booking does have any cost (free cancelling).
 
* Main functionality:
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
at least 24 hours before the booking-start-time).

* For sport-centres/staff:
   - Upon selecting a date, the staff in charge can see all the bookings
for that date. Then, upon selecting a booking the staff can see:
the name of the user who made the booking, 
the booking's badminton-court, start-time, and end-time),
and the state of the booking
(paid/unpaid). Also, upon selecting a booking the staff can change
the state of the booking (from unpaid to paid and vice versa).


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
 
2. Version control: Git repository
[git](https://guides.github.com/activities/hello-world/)

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



## ANNEX
### Teams
#### TeamA
1. (L) Đặng Kim Bảo 
2. Bùi Xuân Phước 
3. Hoàng Văn Thiên 
4. Trần Xuân Khôi 
5. Phạm Nguyễn Thanh An 
6. Lê Minh Thư 
7. Tạ Thị Phương Liên 

#### TeamB

1. (L) Trương Minh Hiếu 
2. Huỳnh Quang Phước Thịnh 
3. Nguyễn Trần Quang Anh 
4. Nguyễn Đình Thi 
5. Nguyễn Hữu Đức
6. Trần Hữu Lê Huy
7. Phan Nhật Nguyên

#### TeamC

1. (IL) Hoàng Xuân Bắc
2. Nguyễn Bảo Duy 
3. Huỳnh Đức Khải
4. Lưu Nguyễn Phát
5. Đinh Quý Trí Thông
6. Đoàn Hoàng Tuấn
7. Đặng Chí Công

#### TeamD

1. (IL) Phạm Gia Bảo
2. Vũ Đức Hải
3. Lữ Minh Khương
4. Nguyễn Cường Phát
5. Ngô Minh Thông
6. Trần Nguyễn Quang Huy
7. Nguyễn Quỳnh Hương

#### TeamE

1. (IL) Nguyễn Tiến Đạt
2. Lê Đình Trung Hiếu
3. Nguyễn Quý Minh
4. Tường Duy Tân 
5. Tô Trần Nhật Trường
6. Đinh Hà Nguyên
7. Trần Minh Long 

#### TeamF

1. (IL) Nguyễn Tất Đạt
2. Nguyễn Minh Hoàng
3. Nguyễn Trí Nguyên
4. Nguyễn Toàn Thắng
5. Võ Lê Tùng
6. Đào Thiện Tước
7. Nguyễn Hoàng Quân
8. Bùi Nguyễn Mai Trúc
 

## Version control: Git repository

### clone with https

```unix
git clone https://github.com/manuelclavel/vgupe2020.git
```

