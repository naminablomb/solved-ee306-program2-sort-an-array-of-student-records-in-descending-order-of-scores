Download Link: https://assignmentchef.com/product/solved-ee306-program2-sort-an-array-of-student-records-in-descending-order-of-scores
<br>
The purpose of this assignment is to write a program in LC-3 assembly language to sort an array of student records in descending order of scores. Additionally, the program should search the array (post sorting) to find the score of a student given a name.

Details

An array of student records is given at address ​x3500​. Each record holds information about a student with two fields in this order:

<ul>

 <li><em>Score</em>​ (ranges from 0 to 100)</li>

 <li><em>Address of Name</em>​ (the address of the memory location where this student’s name is stored) Both fields take up 16-bits each so all elements of the array are of the same length. The end of the array of student records is indicated by the sentinel record which has a score of -1. The array itself is unordered meaning that the student records don’t follow any ordering by score or name.</li>

</ul>




A few example files are provided for you so you can make sure you are reading the correct input and

producing the correct output. These files are: ​<strong>Students.asm</strong>, ​ <strong>Joe.asm</strong>​      ,​ <strong>Batman.asm</strong>​,​<strong>Wow.asm</strong>​ and ​<strong>Lookup.asm</strong>​.

Tasks: You have to complete two tasks.

<ul>

 <li><strong><u>Task 1</u></strong>​: Sort the array in decreasing order of score. Highest score first. Note that the sorted array will be ordered by score but each record has an associated name that needs to go with the record.</li>

</ul>

Here is an example test case with an array of 3 student records prior to sorting:

After sorting, the array looks like so:

<ul>

 <li><strong><u>Task 2</u></strong>​: You are given a lookup name at location ​x6000​. You have to lookup this student in the array (post Task 1) and put the student’s score at ​x5FFF ​(i.e., in front of the name). If the student is not in the array then the a -1 should be written at ​x5FFF​. If you are given a lookup name of “Joe” (at address ​x6000​) then the score 55 should be written at ​x5FFF​. If you are given a lookup name of “Bat man” then -1 should be written at ​x5FFF​, because “Bat man” is not a student. (Notice the difference in case.)</li>

</ul>

Note: Each name in the array will be unique. (There will be no duplicate names.) Additionally, the names in the array and in the lookup string must match exactly for the lookup to match. (The capitalization, length, spacing, etc. must all match exactly.)




<h1>Testing</h1>

To check to see if your code executes properly, you need to load in ​Students.asm, Joe.asm, Batman.asm,Wow.asm​ and ​Lookup.asm​ ​<strong>before</strong>​ you load in ​Program2.asm​.

You can test the different lookups by commenting/uncommenting lines in ​<strong>Lookup.asm</strong>​ ​and then loading that in.