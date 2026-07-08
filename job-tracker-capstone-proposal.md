Capstone Project Proposal
Project Title

Job Tracker Platform

Project Overview

The Job Tracker Platform is a full-stack web application that helps job seekers search for jobs, save interesting opportunities, and manage their job applications in one place.

Users will be able to:

Create an account
Log in securely
Search jobs using the Adzuna API
Save jobs
Apply to jobs
Track application status
Delete saved jobs
Update application progress

The application will use real-time job listings from the Adzuna API and store user information in MongoDB.

Problem Statement

Many job seekers use several different websites to search for jobs and manually track applications using spreadsheets or notes. This process is time-consuming and difficult to organize.

The Job Tracker Platform solves this problem by combining job searching and application tracking into one application.

Target Users
Students
Software Developers
Job Seekers
Career Changers
New Graduates
Technologies Used
Frontend
React.js
HTML5
CSS3
JavaScript
Axios
React Router DOM
Backend
Node.js
Express.js
Database
MongoDB
Mongoose
Authentication
JWT Authentication
bcrypt
External API
API Name

Adzuna Job Search API

Base API
https://api.adzuna.com/v1/api
Job Search Endpoint
https://api.adzuna.com/v1/api/jobs/gb/search/1
Authenticated API Request
https://api.adzuna.com/v1/api/jobs/gb/search/1?app_id=YOUR_APP_ID&app_key=YOUR_APP_KEY
Why This API?

The Adzuna API provides real-time job listings from multiple job boards.

It allows users to search jobs by:

Keyword
Location
Salary
Company
Category

This API makes the application display live job opportunities instead of static data.

Data Retrieved from the API

The application will retrieve:

Job Title
Company Name
Job Description
Job Location
Salary
Job Category
Contract Type
Job URL
Posting Date
Features
User Authentication
Register
Login
Logout
Secure Password Encryption
Job Search

Users can search jobs using keywords.

Example:

React Developer
Software Engineer
Frontend Developer
Save Jobs

Users can save jobs for later.

Application Tracker

Users can update application status.

Example statuses:

Saved
Applied
Interview
Offer
Rejected
User Dashboard

Dashboard will display:

Saved Jobs
Applied Jobs
Interview Jobs
Favorite Jobs
Search Filters

Users can filter jobs by:

Location
Salary
Company
Job Category
Database Collections
Users
{
name,
email,
password
}
Saved Jobs
{
userId,
jobId,
title,
company,
location,
salary,
status,
savedDate
}
API Example
Request
axios.get(
"https://api.adzuna.com/v1/api/jobs/gb/search/1",
{
params:{
app_id:"YOUR_APP_ID",
app_key:"YOUR_APP_KEY",
what:"Software Engineer",
where:"London"
}
})
Example Response
{
"title":"Software Engineer",
"company":{
"display_name":"Google"
},
"location":{
"display_name":"London"
},
"salary_min":65000,
"salary_max":90000,
"redirect_url":"https://..."
}
User Flow
Home Page

↓

Register/Login

↓

Search Jobs

↓

View Job Details

↓

Save Job

↓

Apply Job

↓

Update Status

↓

Dashboard

↓

Logout
Future Enhancements
Resume Upload
Email Notifications
AI Job Recommendations
Company Reviews
Interview Notes
Dark Mode
Mobile Responsive Design
Project Goals
Build a full-stack MERN application.
Integrate a third-party REST API (Adzuna).
Implement secure user authentication.
Store user data in MongoDB.
Allow users to manage and track job applications.
Create a responsive and user-friendly interface.
