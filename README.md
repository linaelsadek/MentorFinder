# MentorFinder
This application is an interactive prototype that matches students with potentials mentors 

# Purpose
The purpose of this application is to allow students to look for mentors to help them out with a course they need assistance with. The application will allow the students to enter their school information, course number, and budget. The application will then display a list of mentors with a synopsis of each mentor’s experience for the student to select from.

# Target user
The target audience for this project will be focused on undergraduate students. However, it can later be expanded to include any student seeking assistance.

# Tasks
Task 1 Finding mentor for course 
  • Specify an institution*
  •	Specify a faculty**
  •	Specify a department
  •	Specify a course ID
  •	Specify minimum and maximum budget
  *  This field will contain a lookup button to show a list of available institutions
  ** This field will be a dropdown that the user can select from
Task 2 Show list of available mentors
  •	Search by mentor’s name
  •	Sort based on mentor’s name, ratings, or budget
  •	Filter list based on the following criteria: First Name, Last Name, Rate, and budget.
  •	Select a mentor to display detailed information
Task 3 Mentor’s Profile
  •	Display mentor’s name, detailed information on experience, overall rating, and existing comments.
  •	Rate mentor 
  •	Review mentor
  •	Hire mentor (see task 4)
Task 4 Hire Mentor
  •	Set mentoring hours
  •	Confirm rate/hour is correct
  •	Submit payment
  •	Open email client with pre-set subject and body

# Design Decisions
Find a Mentor Page
  •	Find a Mentor page is a simple input form. Its purpose is to retrieve a focused list of mentors to the user based on the input of this form. The limited mentors retrieved      allows for a smaller query result from the database which enhances site performance, and load time.
  •	All required fields such as Institution, Faculty, and Department have some form of assistive input, such as a lookup button or a dropdown menu as shown in Layout 1. This       decision is set to decrease the user’s error rate.
  •	Referring to Layout 1, the form input fields have been designed to group fields that require mouse action together followed by fields that require keyboard typing. This is     designed to promote consistency of data-entry as per data entry guidelines. This consistency will prevent the user from having to constantly switch between mediums of input.     It will also enhance the users’ learnability of the system as well as retention.
Browse Available Mentors Page
  •	Browse Available Mentors page will limit mentors displayed to three mentors per page as shown in Layout 2. This will avoid cluttered displays and allow for an easier           comparison as per the Research-Based Web Design & Usability Guidelines 6:1 and 6:4 [1]. This design decision will give a cleaner look to the interface and display the contents   of the page without requiring the user to scroll between mentors for comparison. Avoiding scrolling is important, since the user is expected to look at different mentors         multiple times before making a decision. The frequent scrolling can cause dizziness or eye strain, which might negatively impact user satisfaction. Not only that, but also       lower user performance since the user might need to take frequent breaks while using the website.  
  •	Each mentor will have a description excerpt that is limited to 50 characters per line with a maximum of two lines, overall rating in “stars” ranking, and “Read More” button.   If a mentor does not provide an excerpt, the first 100 characters of the description will be put instead. The 50 characters per line limitation is put to enhance the             readability of the description section and is within the industry’s accepted range of 45-75 characters [2]. 
  •	On click of “Read More” button, a non-modal appears to the user. The choice of using a non-modal in this case, instead of opening a new page is due to the anticipated          frequency of this action. Since users are expected to click on the “Read More” button of different mentors and possibly the same mentor but multiple times, it will become        tedious to have a page reload on every click. Performance will be affected since filters, sorting, pagination, and media will need to be reloaded to the place the user left      off. This can negatively affect the website’s load time and as a result, the user’s perceived satisfaction.
Mentor’s Profile Dialogue
  •	Mentor’s Profile dialogue is a non-modal that appears on “Read More” button click. The design of the dialogue is shown in Layout 3. It is grouped into 3 sections. The top     section shows the most important information to the user: the mentor’s picture and name, their rating in stars, and the hourly fees associated with them. The middle section     shows the detailed experience of the mentor. The lower section shows the reviews received from other students, as well as a “Hire Me” button.
  •	Grouping the most important information together in the top section is intended to enhance the user’s performance in making a decision about mentor selection. Not only that,   but it is also intended to enhance the trustability of the system in the eyes of the user. Since all important information is clearly displayed with no additional clutter       surrounding it, it does not give the perception that the system is trying to hide some information from the user. 
  •	We also added a review option in terms of “stars” since this is the most commonly used method and is widely known and understood. It is also used in eCommerce giants such as Amazon, and eBay. 
  •	The non-modal dialog was implemented based on industry accepted guidelines. According to Nielsen Norman Group, a company for research-based user experience, the first         requirement is to provide a way to return to the main page [3]. This is implemented using the “x” button located in the top right corner of the dialogue and the option for       the user to click anywhere outside the dialog to return to the main screen. The second requirement is to prevent the dialog from appearing unless prompted by the user, which      is implemented by having the user click “Read More” button in Browse Available Mentors page.  
