
### Case Study 1: Employee Management System

**Scenario**:  
You are tasked with creating an employee management system for a company. The system should store information about employees, departments, and the projects they work on. You need to write SQL queries to perform various tasks such as retrieving employee details, assigning employees to projects, and generating reports.

#### Tables:

1. **employees**
   - Columns: `employee_id` (integer, primary key), `name` (varchar), `department_id` (integer)

2. **departments**
   - Columns: `department_id` (integer, primary key), `department_name` (varchar)

3. **projects**
   - Columns: `project_id` (integer, primary key), `project_name` (varchar)

4. **employee_projects**
   - Columns: `employee_id` (integer), `project_id` (integer)

---

**Practice Questions**:
1. Write a SQL query to retrieve the names of all employees working on a project named 'Project X'.
2. Write a SQL query to count the number of employees in each department.
3. Write a SQL query to find all projects that have no employees assigned.

---

### Case Study 2: E-commerce System

**Scenario**:  
You are responsible for managing the database of an e-commerce system. The system should store information about products, customers, and orders. You need to write SQL queries to manage inventory, track customer orders, and generate sales reports.

#### Tables:

1. **products**
   - Columns: `product_id` (integer, primary key), `product_name` (varchar), `price` (decimal)

2. **customers**
   - Columns: `customer_id` (integer, primary key), `customer_name` (varchar), `email` (varchar)

3. **orders**
   - Columns: `order_id` (integer, primary key), `customer_id` (integer), `order_date` (datetime)

4. **order_items**
   - Columns: `order_id` (integer), `product_id` (integer), `quantity` (integer)

---

**Practice Questions**:
1. Write a SQL query to generate a sales report showing the total sales amount for each product in the 'products' table.
2. Write a SQL query to find the total number of orders placed by each customer.
3. Write a SQL query to list all customers who have not placed any orders.

---

### Case Study 3: Library Management System

**Scenario**:  
You are developing a library management system to keep track of books, members, and borrowings. You need to write SQL queries to manage book inventory, register new members, and track borrowings.

#### Tables:

1. **books**
   - Columns: `book_id` (integer, primary key), `title` (varchar), `author` (varchar)

2. **members**
   - Columns: `member_id` (integer, primary key), `member_name` (varchar), `membership_date` (datetime)

3. **borrowings**
   - Columns: `borrowing_id` (integer, primary key), `book_id` (integer), `member_id` (integer), `borrow_date` (datetime), `return_date` (datetime)

---

**Practice Questions**:
1. Write a SQL query to find all books borrowed by a member named 'John Doe'.
2. Write a SQL query to count the number of books borrowed by each member.
3. Write a SQL query to list all books that have never been borrowed.

---

### Case Study 4: Hospital Patient Management

**Scenario**:  
You are tasked with managing patient records, including admissions, discharges, treatments, and billing. You need to write SQL queries to analyze patient data, track treatments, and generate billing reports.

#### Tables:

1. **patients**
   - Columns: `patient_id` (integer, primary key), `patient_name` (varchar), `date_of_birth` (date)

2. **admissions**
   - Columns: `admission_id` (integer, primary key), `patient_id` (integer), `admission_date` (datetime), `discharge_date` (datetime)

3. **treatments**
   - Columns: `treatment_id` (integer, primary key), `patient_id` (integer), `treatment_date` (datetime), `treatment_description` (varchar)

4. **billing**
   - Columns: `billing_id` (integer, primary key), `patient_id` (integer), `billing_date` (datetime), `amount` (decimal)

---

**Practice Questions**:
1. Write a SQL query to find all treatments provided to a patient named 'Jane Smith'.
2. Write a SQL query to calculate the total billing amount for each patient.
3. Write a SQL query to list all patients who have been admitted but not yet discharged.

---

### Case Study 5: University Course Enrollment

**Scenario**:  
You are tasked with managing course enrollments, student records, and grades at a university. You need to write SQL queries to track enrollments, calculate grades, and generate reports.

#### Tables:

1. **students**
   - Columns: `student_id` (integer, primary key), `student_name` (varchar), `enrollment_date` (date)

2. **courses**
   - Columns: `course_id` (integer, primary key), `course_name` (varchar), `credits` (integer)

3. **enrollments**
   - Columns: `enrollment_id` (integer, primary key), `student_id` (integer), `course_id` (integer), `grade` (varchar)

---

**Practice Questions**:
1. Write a SQL query to list all courses a student named 'Alice Johnson' is enrolled in.
2. Write a SQL query to calculate the GPA for each student based on their grades.
3. Write a SQL query to find all courses that have no students enrolled.

---
