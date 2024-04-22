# Manual-Testing-1
  
**Story Spoil Web Application** 

You are provided with a web application, Story Spoil, along with the specification of the requirements. The primary objective of the exam is to ensure the App functions as expected according to the provided use cases. This involves creating test cases for each use case. It also includes the detection and detailed documentation of any identified bugs. You have to document all your work in the provided Test Management and Bug Tracker Template. 

**Software Requirements**
**1. Introduction** 
 **1.1. Purpose** 
The objective of this document is to provide a description of the Story Spoil application (also referred to as Story Spoil or The App). It will present an overview of the key functionalities. 

 **1.2. Scope**
This document includes high-level descriptions of the basic functionalities of Story Spoil, such as user registration, login, profile editing, spoiler creation and management. It does not cover any special user (Administrator) functionalities. 
 
**2. Overall Description** 
 **2.1. System environment** 
The App hosts two primary actors: unregistered/non-logged users and registered/logged users. Both can access their respective parts of the application via the internet on the following url: 
https://d24hkho2ozf732.cloudfront.net/  
 
 **2.2. Key Features** 
Unregistered/non-logged users have access only to the Home page of The App, with the option to either SIGN UP or LOG IN. On the other hand, registered/logged users have access to the main functionalities, including Profile editing, Spoiler creation, and Spoiler management. 

 **2.2.1. Home Page for unregistered / non-logged users** 
The Home Page is the main gateway into The App. It contains a navigation bar (also referred to as Navbar) on top, with StorySpoil Home Page link on the left and SIGN UP and LOG IN buttons on the right. The Home Page is scrollable and the central focus is to encourage users to share their stories.  
Below, there are three sections promoting The App experience. Each consists of motivational phrase, short description and corresponding picture: Summarize the Story, Upload a Picture, Ready to Spoil a Story?.  
At the bottom, there is a Copyright Footer, which upon click, leads to the copyright page which includes the name of the copyright owner, the year of copyright, and any other relevant copyright information. 

 **2.2.2. Sign Up Page** 
The Sign Up page is accessed from the Home page via SIGN UP button on the Navbar. It contains registration form with fields for entering Username, Email, First Name, Middle Name, Last Name, Password, and Repeat Password. The form also includes a SIGN UP button to submit the form. There is also a LOG IN HERE button for registered users, which redirects to LOG IN page. 

The acceptable requirements for each field on the registration form are specified as follows: 
Username: A 2-30 character field, accepting all character types.  Email: Requires a valid email, 6-254 characters long. 
First Name: A 2-60 character field, accepting all character types. 
Middle Name: A 2-60 character field, accepting all character types. Not required. 
Last Name: A 2-60 character field, accepting all character types. 
Password: Any characters are acceptable, with a length of 6-30 characters Repeat Password: Must match password.

 **2.2.3. Login Page**
The Log In page can be reached from the Navbar LOG IN button on the Home page. The page provides fields for Username and Password, as well as a Forgot password option, also a LOG IN button and a CREATE NEW button, which leads to Sign Up page.  
Forgot Password functionality leads to a Restore password page, where the password can be restored by verified email. 

 **2.2.4. Home Page for logged users**
Once a user is logged in, they are redirected to a different version of the Home page. The page includes a Navbar on top, with links to the User's profile and Home page on the left, and CREATE SPOILER and LOGOUT buttons on the right. The Home page includes welcome message with the User's name, and a Search Field with a Search button. If there is no spoiler added, the Home page is showing No Spoilers Yet! message and a WRITE SPOILER button, which leads to Create Spoiler page. 

**а.Home Page Search Functionality** 
The search functionality is available on Home Page and contains  a Search field and a Search button. Users can enter title of the spoiler and click the Search button to initiate the search. The search functionality then filters the list of spoilers based on the provided titles. If there are no spoilers found, There are no spoilers :( message is shown again, as well as the WRITE SPOILER button, which leads to Create Spoiler page.  

 **2.2.5. My Profile Page** 
This page is accessible for logged users from the Navbar, top-left icon.  It includes three sections. On the left, by default an empty profile picture, Username and EDIT button. On the right are User's attributes  - Full Name, Email and Total spoilers counter (zero by default). Below the User's attributes, the About me section is located (displaying "You haven’t written anything about yourself…" by default). 

  **2.2.6. Edit Profile Info Page**
 Accessible from EDIT button on My Profile page, this page allows users to edit their profile information, including Profile picture (picture is not uploaded, but must be a valid URL of a picture, for example http://......jpg), First name (max 60 characters length) , Middle Name (max. 60 characters length), Last name (max. 60 characters length), About me (max. 256 characters length).  
 
 **2.2.7. Create Spoiler Page** 
This page is accessible from the Create Spoiler link on the navbar and contains the following: Story Title field (max. 70 characters length), Describe your story spoiler field (max. 400 characters length), Add a picture for the spoiler field (picture is not uploaded, but must be a valid URL of a picture, for example http://......jpg) and CREATE button. 
  Upon creating a Spoiler, it redirects to Home page for logged users, where the new added Spoiler is present with it's attributes and buttons for SHARE, EDIT, and DELETE 

 **2.2.8. Story Spoiler Management**
Story Spoiler Functionalities are available from the Home Page. Each created Story Spoiler has its own SHARE, EDIT and DELETE buttons.

**a. Share** - Available after clicking on SHARE button.
**b. Edit** - Available after clicking on EDIT button.
**c. Delete** - After clicking on DELETE button, the Spoiler is deleted and it disappers from the Home page. 

**Functional Requirements**  
**1. Use Case 1 (Home Page)** 
Users should be able to access The Story Spoil App from its designated URL via the Internet, which should load the Home page, appropriate to the user's logged-in status (unregistered/non-logged or registered/logged). 

**2. Use Case 2 (User Registration)** 
Unregistered users should be able to successfully go through the Sign Up process. This involves the utilization of fields such as Username, Email, First name, Middle Name, Last name, Password and Repeat Password, all subject to their respective constraints and character type acceptance.  

**3. Use Case 3 (User Sign In)** 
Registered users should be able to successfully go through the Log In process. They should be able to log in using  Username and Password. 

**4. Use Case 4 (Profile Management)** 
Upon successful Log In, logged users should be able to navigate to their Profile page, edit their profile details, and view their Spoilers count. This involves the changing of profile picture inserted via URL, and editing of user data fields including First Name, Middle Name, Last Name and About me sections. 

**5. Use Case 5 (Spoiler Creation)** 
Logged users should be able to navigate to the Create Spoiler page, where they can create a new Spoiler with a Title, Description, and a Picture (URL). After the Spoiler creation process, users should be redirected to the Home page, where the newly created Spoiler should be present. 
 
**6. Use Case 6 (Spoiler Management)** 
On the Home page, logged users should see all their Spoilers listed. Each Spoiler should have options for Share, Edit, and Delete. If no spoilers have been created yet, a "No Spoilers Yet!" message should be displayed. Users also should have the option to search for spoilers, based on spoiler titles. 

**Spoiler Web App Tasks** 
**1. Test Cases** 
You need to write test cases for each of the 6 Use cases. 
Each Use case should have at least 2 Test Cases. You should write at least 15 test cases. 

**2. Bug Reports**  
You should find and describe at least 5 bugs. 
2 of the bugs should have high priority OR blocking/critical severity. 

**3. Template** 
Use the provided Test-Management-and-Bug-Tracking-Template.xlsx to document your work. 

