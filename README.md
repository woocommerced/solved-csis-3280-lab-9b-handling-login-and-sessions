Download Link: https://assignmentchef.com/product/solved-csis-3280-lab-9b-handling-login-and-sessions
<br>
Visual Studio Code

<ol>

 <li>Download the lab template from Blackboard</li>

 <li>Extract it</li>

 <li>Fill in the relevant code to create the solution and meet the requirements Solution</li>

</ol>

Based on thep provided template create a web application that completes the following workflow:

<ol>

 <li>The user starts at the login page.</li>

 <li>The user logs in and their password is verified against the database. If the login is successfull a new session is started and the users details are copied to the session.</li>

 <li>The user is redirected to the welcome page and their details are displayed.</li>

</ol>

<table width="0">

 <tbody>

  <tr>

   <td width="244">inc/config.inc.php</td>

   <td width="436">Database configuration information</td>

  </tr>

  <tr>

   <td width="244">inc/Utility/PDOAgent.class.php</td>

   <td width="436">PDO Wrapper Class</td>

  </tr>

  <tr>

   <td width="244">inc/Utility/Page.class.php</td>

   <td width="436">Page Class</td>

  </tr>

  <tr>

   <td width="244">inc/Utility/UserMapper.class.php</td>

   <td width="436">Static User Mapper responsible for CRUD operations</td>

  </tr>

  <tr>

   <td width="244">inc/Entities/User.class.php</td>

   <td width="436">User Entity with getters and setters.</td>

  </tr>

  <tr>

   <td width="244">inc/Utility/LoginManager.class.php</td>

   <td width="436">LoginManager responsible for checking if a user is logged in</td>

  </tr>

 </tbody>

</table>

<ol start="4">

 <li>When the user selects to log off, they are redirected to a page that wishes them good bye. There session is terminated and then after 10 seconds redirects them to the main page.</li>

</ol>

You must utilize the database provided in the sql directory. You must use password_verify and password_hash to verify the username and password stored in the database. The passwords are all set to the same value of respective usernames.

<h1>Requirements</h1>

<ol>

 <li>You must use a database called “<strong>Lab09</strong>“, your username should be ‘root’ and your password should be ” just like the lab computers.</li>

 <li>You must use the PDO class we created based on the template provided.</li>

 <li>You muse use a User class to map the user details</li>

 <li>You must use a UserMapper class to get information from the database 5. You must use the LoginManager static class to verify the login</li>

 <li>You must store if the user is logged in in a session.</li>

</ol>

<h1>Structure</h1>

<strong>FileName                                             Description</strong>

<strong>FileName                                             Description</strong>

<table width="0">

 <tbody>

  <tr>

   <td width="244">inc/Utility/Validation.class.php</td>

   <td width="436">Responsible for Validating user input</td>

  </tr>

  <tr>

   <td width="244">Lab08_SWh-56789-login.php</td>

   <td width="436">This file displays the login page to the user and processes logins.</td>

  </tr>

  <tr>

   <td width="244">Lab08_SWh-56789-welcome.php</td>

   <td width="436">This page welcomes the user, it should not be visisble if the user has not provided a proper login</td>

  </tr>

  <tr>

   <td width="244">Lab08_SWh-56789-logout.php</td>

   <td width="436">This file displays the logout page to the user and redirects them after 10 seconds to the login page.</td>

  </tr>

 </tbody>

</table>

sql/Lab09.sql                                         User database with accounts

Hints:

Use header() to redirect between pages

You can use the META REFRESH tag to redirect with a delay session_destory() doesnt actually work well, you should unset() the session

Use your browsers “In Private” or “Incognito Mode” to test the effects of different sessions.

Appendix:

<ol>

 <li>Login Page</li>

 <li>Welcome Page</li>

 <li>Good Bye!</li>

</ol>