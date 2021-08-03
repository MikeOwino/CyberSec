SQL Injection Prevention
There are two main methods for preventing injection attacks: sanitization and prepared statements.

Sanitization
Sanitization is the process of removing dangerous characters from user input. When it comes to SQL injections, we would want to escape dangerous characters such as:

'
;
\--
These sorts of characters can allow attackers to extend queries to output more data from a database.

While this does provide a layer of protection, this method isn’t perfect. If a user finds a way to bypass your sanitization process, they can easily inject data into your system.

Additionally, depending on your query, removing certain characters may have no effect! Therefore, this shouldn’t be your only defense mechanism.

Prepared Statements
Writing prepared statements in backend code is a common, reliable, and secure solution against SQL injections. Prepared statements are nearly foolproof.

How does it work? We provide the database the query we want to execute in advance. First, the database processes our query. Then we pass in the parameters/user input. Any input, regardless of whether the content has SQL syntax, is then treated only as a parameter and will not be treated as SQL code.

Here is an example of what a prepared statement looks like in PHP web application backend code:

$username= $_GET['user'];
$stmt = $conn->prepare("SELECT * FROM Users WHERE name = '?'");
$stmt->bind_param("s", $username);
$stmt->execute();
In addition to providing added security, prepared statements also make queries far more efficient.