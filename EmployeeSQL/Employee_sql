--1. List the following details of each employee:
--employee number, last name, first name, sex, and salary.

Select distinct emp.emp_no as Employee_Number, emp.last_name as LastName, 
emp.first_name as FirstName, emp.sex as Sex, 
salary.salary
 from employee emp ,salaries salary 
 where emp.emp_no=salary.emp_no;
 

--2. List first name, last name, and hire date for employees who were hired in 1986.

Select  distinct emp.emp_no as Employee_Number, emp.last_name as LastName, 
emp.first_name as FirstName,
emp.hire_date as HireDate
 from employee emp
 where to_char(emp.hire_date,'yyyy') = '1986';
 

--3. List the manager of each department with the following information: 
--department number, department name, the manager's employee number, last name, first name.

select distinct emp.emp_no as Employee_Number, emp.last_name as LastName, 
emp.first_name as FirstName, 
dept.dept_no as Dept_Number, dept.dept_name as Dept_Name
from
employee emp, departments dept, 
dept_manager deptMngr
where 
emp.emp_no = deptMngr.emp_no 
and deptMngr.dept_no = dept.dept_no 
and emp.emp_title_id = 'm0001';

--4. List the department of each employee with the following information: 
--employee number, last name, first name, and department name.

select distinct emp.emp_no as Employee_Number, emp.last_name as LastName, 
emp.first_name as FirstName, 
dept.dept_no as Dept_Number, dept.dept_name as Dept_Name
from
employee emp,departments dept, deptemp deptemp1
where 
emp.emp_no = deptemp1.emp_no 
and dept.dept_no = deptemp1.dept_no
;

--5. List first name, last name, and sex for employees whose first name is "Hercules" 
--and last names begin with "B."

Select distinct emp.emp_no as Employee_Number, emp.last_name as LastName, 
emp.first_name as FirstName, emp.sex as Sex
 from employee emp 
 where emp.first_name ='Hercules' and emp.last_name like 'B%';

--6. List all employees in the Sales department, including their employee number, 
--last name, first name, and department name.


select distinct emp.emp_no as Employee_Number, emp.last_name as LastName, 
emp.first_name as FirstName, 
dept.dept_no as Dept_Number, dept.dept_name as Dept_Name
from
employee emp,departments dept, deptemp deptemp1
where 
emp.emp_no = deptemp1.emp_no 
and dept.dept_no = deptemp1.dept_no
and dept.dept_name = 'Sales' 
order by emp.emp_no asc;



--7. List all employees in the Sales and Development departments, 
--including their employee number, last name, first name, and department name.

select distinct emp.emp_no as Employee_Number, emp.last_name as LastName, 
emp.first_name as FirstName, 
dept.dept_no as Dept_Number, dept.dept_name as Dept_Name
from
employee emp,departments dept, deptemp deptemp1
where 
emp.emp_no = deptemp1.emp_no 
and dept.dept_no = deptemp1.dept_no
and dept.dept_name in ('Sales' ,'Development')
order by emp.emp_no asc;

--8. In descending order, list the frequency count of employee last names, 
--i.e., how many employees share each last name.

Select   emp.last_name as LastName,count(distinct emp.emp_no) 
 from employee emp 
 group by emp.last_name 
 order by count(distinct emp.emp_no) desc;
