Getting Started
Clone the repository to your local machine:

bash
Copy code
git clone https://github.com/your-username/login-page.git
Set up a web server with PHP and MySQL support. You can use tools like XAMPP or MAMP for a local development environment.

Create a MySQL database and import the provided database.sql file to set up the necessary table.

Update the connection.php file with your MySQL database credentials:

php
Copy code
$servername = "your_server_name";
$username = "your_username";
$password = "your_password";
$dbname = "your_database_name";

// Create connection
$conn = new mysqli($servername, $username, $password, $dbname);

// Check connection
if ($conn->connect_error) {
    die("Connection failed: " . $conn->connect_error);
}
Usage
Open the project in a web browser by navigating to the project folder.

Access the index.php file to see the login page.

Enter valid credentials to log in. Upon successful login, the user will be redirected to the welcome.php page.

Features
Session Management: The code utilizes PHP sessions to keep track of user authentication.

Cookie Storage: A cookie named user_cookie is set upon successful login, which stores the username and is valid for 1 day.

Database Interaction: The code interacts with a MySQL database to authenticate users against stored credentials.
