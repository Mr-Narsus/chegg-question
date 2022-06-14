This is a solution to a university question, which some students need.

I found a solution on [chegg](https://www.chegg.com/homework-help/questions-and-answers/home-directory-create-directory-called-finalproject-underneath-following-write-shell-scrip-q79101705) site, But it is a wrong solution, That's why I wrote this solution

## The  Question

On your machine, create a subdirectory under your home directory called youruserid_prj3 (e.g. **u119xxxx_prj3**).
In addition, create the following under it: Write a shell script called _**mycourses**_ that when
executed displays the following four choices: (Your script should work on your own created courses file called _**courses**_.)

1. Add Course

This option allows the admin to create a new course containing the following items:
 * a) Course id: a unique string made of exactly eight or seven digits 4 small letters followed by 3 digits numbers for example comp311 or 3 small letters followed by 4 digits number for example comp1310.
 Id that are already in use as well as id numbers that contain anything other than the formats above should be continuously rejected until a unique id of the correct format is entered.
 
 * b) Full name: Full name of the course to be added for example (e.g: LinuxOSLab).
 * c) Book ISBN number: Should be in the format x-xxx-xxxx where each x is a digit numbers. ISBN numbers that have chars other than digits or that are not in the correct format should be continuously rejected until an ISBN number with the correct format is entered.
 * d) Instructor name: Full name of the instructor to be added (First Name and Last Name) The admin should be able to add as many courses as he/she wishes.

2. Change Course

This option gives the admin three choices:

 * a) Delete a course.
   A course entry should be deleted according to a given id (exact id and not part of it). If the given id does not exist, a suitable message should be displayed.
  The admin should be able to delete as many courses as he/she wishes.
  
 * b) Delete all courses
Selecting this option deletes all the course entries that have been added to the system.
 * c) Change course info
Selecting this option will allow the admin to select whether to modify the ISBN number or the instructor last name. (Those are the only two items that are open for modifications) and make the
necessary modification. New ISBN numbers should be checked for the correct format as mentioned in the add section above.
The admin should be able to modify/delete as many courses as he/she wishes.


3. Search Courses

This option gives the admin two choices:
 * a) Search by id number
   All course information (Name, id, ISBN #, Instructor Name) should be displayed in a suitable and organized format according to a given id. If the given id does not exist, a suitable message should be displayed.
  The admin should be able to search for as many courses as he/she wishes.
 * b) Search by name of instructor
The admin should be given a choice to search by first name or last name and if more than, one match is found for either, the info for all the courses that match should be displayed sorted by the full name of the course. Admins may also enter a part of a name (first or last) and any matches should be displayed sorted by course full name.

   The admin should be able to add, modify, or search for courses in any order and as many times as he/she wishes during the same session of executing the mycourses script.
   
   Be sure to use the same names for your shell script(s) and options as given above and to make your shell script(s) as modular as possible.
   
   Also, be sure to include any error checking necessary.
   
   
   

# The Solution

`cd /tmp; git clone https://github.com/Mr-Narsus/chegg-question`

`dir=$(id | awk -F= '{print $2}'| cut -d"(" -f 1)_prj3; mkdir $HOME/$dir`

`cp chegg-question/* $HOME/$dir`


