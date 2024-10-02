Project Name: User Login & Register System

Description:
This project is a simple user authentication system built using PHP and MySQL. It allows users to register, log in, and manage their profile information. The project includes various features such as user sessions, form validation, and database interaction to handle user credentials securely.

Features:

User Registration: Allows new users to register by providing a username, email, age, and password.
                   User Login: Users can log in using their email and password.
Session Management: Sessions are used to track logged-in users across different pages.
Profile Management: Users can view and update their profile information such as username, email, and age.
Logout: Users can log out, and the session is destroyed.


File Structure: 
project-folder/
│
├── php/
│   ├── config.php            Database connection file
│   ├── logout.php            Handles user logout
│
├── style/
│   ├── style.css             Styles for the project
│
├── home.php                  User dashboard after login
├── index.php                 Login page
├── register.php              Registration page
├── edit.php                  Change profile page
├── README.md                 Project documentation



Setup Instructions:
1. Requirements:
                PHP (7.x or higher)
                MySQL Database
                Web server (e.g., XAMPP, WAMP, MAMP)
2. Database Setup:
                Create a MySQL database called tutorial.
                Run the following SQL script to create the users table:

SQL:

CREATE TABLE `users` (
  `Id` int(11) NOT NULL AUTO_INCREMENT,
  `Username` varchar(50) NOT NULL,
  `Email` varchar(50) NOT NULL UNIQUE,
  `Age` int(3) NOT NULL,
  `Password` varchar(255) NOT NULL,
  PRIMARY KEY (`Id`)
);

 3. Configuration:
                  Modify the php/config.php file to match your MySQL database credentials:
              php:
                  $con = mysqli_connect("localhost", "root", "", "tutorial") or die("Couldn't connect");
    
5. Running the Application:
                Start your web server (e.g., XAMPP or WAMP).
                Place the project files in your server's htdocs directory.
                Open the project in a browser: http://localhost/project-folder/index.php.
