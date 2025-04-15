# NewRepo MOD 12



Setup: Getting Started with GitHub CodeSpaces
Introduction
Welcome to the GitHub and SQLite Lab! In this interactive lesson, you'll create a free GitHub account and make your first "codespace", a virtual environment for running Visual Studio Code in the cloud. Then you'll create a SQLite database in your virtual environment and populate it with tables and records. By the end of this lab, you'll have the knowledge and hands-on experience to use both GitHub CodeSpaces and SQLite for your personal and professional projects. Let's dive in and unlock the full potential of this indispensable tool for developers!

Instructions
Octocat
Step 1: Sign up for Your GitHub Account
Go to https://github.com/
Enter your Minneapolis College email address in the textbox. Your Minneapolis College email address ends in @go.minneapolis.edu.
Click the Signup for GitHub button.
Click Continue.
Enter a password and click Continue.
Enter a username and click Continue.
If you want email about GitHub, click the checkbox. Then click Continue.
Solve the Captcha puzzle and click Submit.
Open your Minneapolis College email inbox.
Locate the GitHub Launch email and copy the code. The email looks like this:

Paste the code into the GitHub website.
On the Welcome to GitHub screen, click Just Me and Student.
On the "What specific features are you interested in using?" screen click on Collaborative coding. Then click Continue.
Click Continue for free.
Now you are finished with the signup process! You should see your GitHub Dashboard displayed.
If you'd like free access to GitHub professional for a year (a $48 value), after class you can sign up for the student developer pack.
After class, please locate your student ID. If you don't have one, you can get one here: Campus Card | Minneapolis Community & Technical College 
Go to the Student Developer Pack signup page.
Click Signup for Student Developer Pack.
Click Get Student Benefits.
Select the radio button labeled Students.
Scroll down and enter the name of your school Minneapolis College. Then click Continue.
You may be prompted to add your school email to your profile and verify it.
Take a picture of your student ID and upload the picture.
Click Process my application.

If you need help signing up for your Student Developer Pack, you can get help from GitHub Support.
Step 2: Create a New Repository
Click on the green Create Repository button on the dashboard. If you don't see the button, click on the + symbol on the toolbar and click New Repository in the drop-down menu.

GitHub dashboard
In the repository name textbox, enter MyFirstRepo. (Developers sometimes call their repositories "repos" for short.) Leave all of the default settings.
Scroll down and check Add a README file.
Click the green Create Repository button.
Step 3: Create a new Codespace
Cat
Introduction
Welcome to the world of GitHub Codespaces, where your development environment is just a click away! Codespaces is a cloud-based platform that provides you with a fully-fledged, customizable, and ready-to-code development environment for your projects. It's like having a personal coding studio in the cloud, accessible from anywhere, at any time.

CodeSpaces uses Microsoft's Visual Studio Code editor: https://code.visualstudio.com/

This is one of the world's most popular Integrated Development Environments (IDEs)!

GitHub Codespaces supports a variety of programming languages, ensuring that developers can work with their preferred tools and frameworks. Some of the core languages supported by GitHub Codespaces include:

Node.js
Python
Java
C# (.NET)
Additionally, you can configure the display language for the Codespaces editor interface to suit your preferences. This flexibility allows for a wide range of development activities, from web development to data science, all within the cloud-based environment of Codespaces.

How to Code in GitHub CodeSpaces
Go to GitHub.com and sign in.
Click on the Octocat icon Octocat icon in the upper left corner to open the dashboard.
Click on the + symbol on the toolbar and choose New Codespace from the drop-down menu.

New Codespace
In the Create a new codespace dialog, click on Select a Repository and select MyFirstRepo. Then click the green Create Codespace button.
GitHub will open your new codespace. Be patient - it might take a few minutes to get your codespace ready.
Congratulations! Give yourself a pat on the back. Now you are ready to develop in the cloud using GitHub Codespaces! Keep in mind, you can only create one or two codespaces with your free GitHub account. Sign up for the Student Developer Pack to make more codespaces: https://education.github.com/pack/join

Part 1: Getting Started with SQLite (In-Class Activity)
Introduction
This lab provides a practical introduction to SQLite database development using GitHub Codespaces. You'll learn essential database operations including schema design, data manipulation, and query optimization. The lab is structured to build progressively from basic concepts to more advanced database operations.

Learning Objectives
• Implement SQLite database creation and configuration.
• Design and implement database schemas with appropriate constraints.
• Execute data manipulation operations using SQL.
• Develop efficient queries for data retrieval and analysis.
🎒 Before We Start
Make sure you have:

✅A GitHub account (it's free!)
✅Basic understanding of SQL (don't worry, we'll review as we go)
🛠️ Step 1: Setting Up Your Workspace  
1. Getting Started with GitHub Codespaces
Sign into your GitHub account.
Create a new repository with a ReadME file.
Click the green "Code" button and select "Create codespace on main".
Wait for the development environment to initialize.
2. Development Environment Configuration
Configure VS Code with the necessary extensions for SQLite development:

Open the Extensions panel, by clicking the Extensions button on the left menu or by pressing Ctrl+Shift+X on Windows or Cmd+Shift+X on Mac.
Search for "SQLite".
Install the official "SQLite" extension.
Search for "SQLite Viewer" and install it for a nice visual interface.
💻 Step 2: Creating Your First Database  
Let's Create Our Database!
Open your terminal in VS Code (Ctrl+` or Cmd+`) and type:

sqlite3 school.db
Congratulations! You've just created your first database! 🎉

Building Our Tables
Let's create some tables to store our school data. Copy and paste each command:

CREATE TABLE students ( student_id INTEGER PRIMARY KEY AUTOINCREMENT, first_name TEXT NOT NULL, last_name TEXT NOT NULL, email TEXT UNIQUE, enrollment_date DATE );
Great job! Now let's add a table for courses:

CREATE TABLE courses ( course_id INTEGER PRIMARY KEY AUTOINCREMENT, course_name TEXT NOT NULL, department TEXT, credits INTEGER );
🎨 Step 3: Adding Data to Your Tables
Let's Add Some Students!
Here's how to add multiple students at once:

INSERT INTO students (first_name, last_name, email, enrollment_date)
VALUES ('Emma', 'Watson', 'emma.w@school.edu', '2024-01-15'),
('Tom', 'Holland', 'tom.h@school.edu', '2024-01-16'),
('Zendaya', 'Coleman', 'zendaya.c@school.edu', '2024-01-17');
✨ Successfully inserted initial student records into the database.

Inserting Course Data
INSERT INTO courses (course_name, department, credits)
VALUES ('Python Programming', 'Computer Science', 3),
('Data Science 101', 'Data Analytics', 4),
('Web Development', 'Computer Science', 3),
('AI Fundamentals', 'Computer Science', 4);
Course data successfully inserted into the database.

🛍️Step 4: Data Retrieval with SELECT and WHERE Clauses
Finding Specific Students
Want to find all students who enrolled after January 15th, 2024?

SELECT first_name, last_name, enrollment_date
FROM students
WHERE enrollment_date > '2024-01-15'
ORDER BY enrollment_date;
        
👀 This will show us our newest students!

Finding Computer Science Courses
SELECT course_name, credits FROM courses WHERE department = 'Computer Science' AND credits >= 3;
🎯 Perfect for finding those tech-focused classes!

✏️ Step 5: Updating Your Data
Updating Student Information
Need to update a student's email address?

UPDATE students
SET email = 'emma.watson.new@school.edu'
WHERE first_name = 'Emma' AND last_name = 'Watson';
✅ Email updated successfully!

Updating Course Credits
UPDATE courses
SET credits = 5
WHERE course_name = 'Data Science 101';
🌟 Course credits updated! This is a more advanced course now!

Closing SQLite
In your VS Code terminal, type:
.quit
➡️ This exits the SQLite environment. 

🐙Step 6: Initialize Git Repository
Now it is time to save and share your SQLite database using GitHub.

In your VS Code terminal within GitHub Codespaces, type:
git init
Add your database file to Git:
git add school.db
Create your first commit:
git commit -m "Initial commit of school database"
4. Push your database to GitHub:

git push -u origin main
✅Step 7: Verify Your Upload
Go to your GitHub repository in your web browser.
You should see school.db listed in your repository. (You may have to refresh the browser.)
⬆️Step 8: Submit Your Work
On your GitHub repository page, copy the HTTPS URL (it should look like: https://github.com/your_username/repository_name)
Paste this URL into the submission textbox at the bottom of the assignment and click Submit.
Celebrate finishing your SQLite Lab! 🎉😉
Bonus Fun: OctocatOctocat
Octocat, GitHub’s iconic mascot, is a unique character that combines the features of an octopus and a cat. The origin of Octocat dates back to when GitHub’s founders were looking for a fun and memorable image for their error pages. They came across a stock illustration created by graphic designer Simon Oxley, which depicted a half-cat, half-octopus character standing in a puddle, then known as “Octopuss.” They purchased the illustration and it quickly became associated with GitHub.

The name “Octocat” emerged as a play on words, combining “octopus” and “cat,” and it resonated with the GitHub community. The mascot was not only a nod to Git’s “octopus merge” (a term used in version control when merging multiple branches), but it also captured the collaborative and multifaceted nature of software development that GitHub embodies. 

Due on Apr 15, 2025 6:00 PM
Available until May 15, 2025 4:00 PM. Access restricted after availability ends.
