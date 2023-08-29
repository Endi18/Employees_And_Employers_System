# Employees and Employers System

## Structure of the Application

### Employee File & Class
Employee’s data should be saved in a file named “employees.txt”. Each employee has the following data:
- personId (String)
- name (String)
- surname (String)
- date of birth (Date)
- password (String) – The password must start with a number and have more than 6 characters
- yearsOfExperience (integer)
- isEmpolyed (boolean)
- employmentRequestId (null if the employee has not made any employment request)
- companyId (null if the employee is not employed)

### Employer File & Class
Employer’s data should be saved in a file named “employers.txt”. Each employer has the following data:
- personId (String)
- name (String)
- surname (String)
- date of birth (Date)
- password (String) – The password must contain more than 8 characters
- companyId (String)
- companyName (String)
- numberOfEmplyees (integer)
- industry (String)

### Vacancies File & Class
Job vacancies should be saved in a file named “vacancies.txt”. Each job vacancy has the following data:
- vacancyId (String)
- companyId (String)
- jobDescription (String)
- isVacancyOpen (boolean)


## Functional Requirements

### Start Up Menu
When the application is started, this question should be displayed:</br>
<b><em>Are you an employee / employer / admin?</em></b>

### Admin Menu
If the user’s answer is “admin”, then the admin password is required -> if the password is correct, then the application menu (for admins) is displayed:</br>
<ol>
  <li>Add a new employee in file “employees.txt”</li>
  <li>Add a new employer in file “employers.txt”</li>
  <li>Display the company name which has added more job vacancies</li>
  <li>Enter the name of a company and display the names of all employees of this company</li>
</ol></br>

- If the given password is not correct no menu is displayed and the application is terminated.
- The admin password should be ‘admin’!

### Employer Menu
If the user’s answer is “employer”, then the employer password is required -> if the password is correct, then the application menu (for employers) is displayed:</br>
<ol>
  <li>Add a new vacancy in file “vacancies.txt” (the companyId should be the same as the logged in employer companyId)</li>
  <li>View the list of all employees who are not employed.</li>
  <li>View the list of all employees who are employed in his/her company</li>
  <li>View the list of all employees who have applied for a vacancy from his/her company</li>
  <li>Accept the application of an employee (the vacancy’s isVacancyOpen should be set as false, employee’s isEmployed should be set to true, employmentRequestId should be set to null and companyId should be set to the same value as the value of companyId in the accepted vacancy)</li>
  <li>Terminate the program</li>
</ol></br>

- If the given password is not correct no menu is displayed and the application is terminated.

### Employee Menu
If the user’s answer is “employees”, then the employee password is required -> if the password is correct, then the application menu (for employees) is displayed:</br>

<ol>
  <li>View the list of all job vacancies (only vacancies which are open)</li>
  <li>Apply for a job vacancy (employmentRequestId should be set as the vacancyId)</li>
</ol></br>

- If the given password is not correct no menu is displayed and the application is terminated.
