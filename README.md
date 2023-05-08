Download Link: https://assignmentchef.com/product/solved-sdev350-week6
<br>
In this lab, you will demonstrate how to identify database code that is susceptible to SQL Injection and make recommendations to fix the code. You will also review and application for privacy violations and make recommendations for improvement.

<strong>Existing Application Description: </strong>

An existing PHP-based application connects to a database providing functionality for retrieving table information for a specific employee. The application also has the ability to update specific user fields. In both cases, a Web-based form is used allowing a user to search for an employee and then either display their employee information or update it.

The web-form display functionality asks the user to enter a specific employee ID and then retrieves the following fields:

<ul>

 <li>Employee_id,</li>

 <li>firstname,</li>

 <li>lastname,</li>

 <li>salary,</li>

 <li>birthdate,</li>

 <li>SSN,</li>

 <li>phonenumber,</li>

 <li>address,</li>

 <li>email,</li>

 <li>nickname,</li>

 <li>Password</li>

</ul>

The update form allows the user to enter a specific employee ID and then update most of the fields in the list above.

As you look at this list, you should definitely be concerned. Part of this exercise will be to identify those concerning fields and make recommendations for changes. However, you were also given access to the PHP code and flag the following code as being suspect.

$conn = getDB();

$sql = “SELECT id, firstname, lastname, salary, birth, ssn,

phonenumber, address, email, nickname, Password

FROM data

WHERE id= ‘$input_id’ and password=’$input_pwd'”;

$result = $conn-&gt;query($sql))




Figure 1. PHP Retrieve Data code

$conn = getDB();

$sql = “UPDATE data

SET nickname=’$nickname’,

1




email=’$email’, address=’$address’, phonenumber=’$phonenumber’, Password=’$pwd’,

Firstname = ‘$firstname’,

Lastname = ‘$lirstname’

WHERE id= ‘$id’ “;

$conn-&gt;query($sql))

Figure 2. PHP Update Data code

<strong>Lab Requirements </strong>

<ol>

 <li>As you review the overall functionality of the application. What concerns do you have with the data and display of the data. For example, are there any privacy concerns? What are best practices for protecting private data? What are best practices for changing a password? Note: you can ignore the SQL Injection issues in this discussion as we will be addressing that in a separate requirement.</li>

 <li>Now that your concerns about the application have been documented, what specific recommendations do you have to address your concerns? Be specific with your recommendations. You should consider items such as using roles to restrict access, limiting access to the form, encrypting fields, applying security controls and others. Discuss if the recommended changes will impact the functionality of the application and if so why that is Okay.</li>

 <li>Review the code and determine is SQL Injection is a problem. Describe specifically how you would test to see if SQL injection was a problem. For example, show exactly what you would input into the form fields to determine if SQL injection was a problem. Discuss the code issues pointing to where the SQL injection could happen.</li>

 <li>Now, that you have identified the code issues, describe what you need to do to fix it. You don’t have to rewrite the code, but you do need to provide specific mitigation strategies, explain why the strategy works, and provide an example code (in PHP) that would resolve the issue<strong>. </strong></li>

 <li>The file should be well-organized, well-written using full sentences and paragraphs and include all required components.</li>

</ol>

<strong>Deliverables: </strong>

One word (or PDF) document should be provided with your name, date, course information (e.g. SDEV 350 6380) and professor name fulfilling all of the requirements listed above.