# OOPJ-Assignment-2

## Problem 1: Counter for Cups

### Scenario: You are keeping track of how many cups of tea are prepared in your home.
### Requirements:
### 1. Create a class TeaCup with instance variable: teaType (String).
### 2. Create a static variable totalCups to count all cups created.
### 3. Constructor should initialize teaType and increment totalCups.
### 4. Create getter for teaType.
### 5. Create a static method showTotalCups() to print total cups.

**Input Example:
Cup1: teaType = "Masala Tea"
Cup2: teaType = "Green Tea"
Cup3: teaType = "Ginger Tea"**

**Expected Output:
Cup1 type: Masala Tea
Cup2 type: Green Tea
Cup3 type: Ginger Tea
Total cups made: 3**


<img width="1920" height="1080" alt="Screenshot from 2025-08-30 13-24-33" src="https://github.com/user-attachments/assets/110c330a-f463-4f75-85f5-adbde0152326" />

<img width="1306" height="294" alt="Screenshot from 2025-08-30 13-25-27" src="https://github.com/user-attachments/assets/315f7a32-509a-4cdd-9e5f-eb93a3f0f993" />


## Problem 2: Simple Mobile Tracker
### Scenario: A shop wants to count how many mobiles are added to their inventory.
### Requirements:
### 1. Create a class Mobile with instance variable: model (String).
### 2. Create a static variable totalMobiles to count total mobiles added.
### 3. Constructor should initialize model and increment totalMobiles.
### 4. Create a getter for model.
### 5. Create a static method showTotalMobiles() to print total mobiles.

**Input Example:
Mobile1: model = "Samsung Galaxy M32"
Mobile2: model = "Redmi Note 12"
Expected Output:
Mobile1 model: Samsung Galaxy M32
Mobile2 model: Redmi Note 12
Total mobiles in stock: 2**


<img width="1920" height="1080" alt="Screenshot from 2025-08-30 13-57-40" src="https://github.com/user-attachments/assets/8b48d4b8-533d-4952-9749-7ac2d8f7c7b6" />

<img width="1002" height="272" alt="Screenshot from 2025-08-30 13-58-14" src="https://github.com/user-attachments/assets/f61a5479-c047-4514-9b99-97337fa92962" />





## Problem 3: Library Book Tracker
### Scenario: A library in Delhi wants to track how many books are issued in total and details of each book.
### Requirements:
### 1. Create a Book class with instance variables: title (String), author (String), issued (boolean).
### 2. Create static variable totalIssuedBooks to keep track of the total number of books issued.
### 3. Create a constructor to initialize the book details.
### 4. Create getters and setters for all instance variables.
### 5. Create a static method showTotalIssued() to print total issued books.
### 6. Write a main class to create 3 books, issue some of them (issued = true), and show total issued
### books.
**Input Example:
Book1: "Harry Potter", Author: "J.K. Rowling", Issued: true
Book2: "Five Point Someone", Author: "Chetan Bhagat", Issued: false
Book3: "Rich Dad Poor Dad", Author: "Robert Kiyosaki", Issued: true
Expected Output:
Book1 issued? true
Book2 issued? false
Book3 issued? true
Total books issued: 2**

```
class Book{

	private String title;
	private String author;
	private Boolean issued;

	public static int totalIssuedBooks;

	Book(String title,String author,Boolean issued){
	
		this.title=title;
		this.author=author;
		this.issued=issued;
		if (this.issued==true){
			totalIssuedBooks++;
		}
	
	}
	public String getTitle()
	{
		return title;
	}
	public String getAuthor()
	{
		return author;
	}
	public Boolean getIssued()
	{
		return issued;
	}

	public void setTitle(String title)
	{
		this.title=title;
	}
	public void setAuthor(String author){
		this.author=author;
	}
	public void setIssued(Boolean issued){
		this.issued=issued;
	}
	public static void showTotalIssuedBooks(){ 
		System.out.println(totalIssuedBooks);
	}
	public static void main(String args[]){
		Book b1=new Book("Harry Potter","j.k.rowling",true);
		System.out.println("Book1 issued? "+b1.getIssued());
		Book b2=new Book("Five Point Someone","chetan bhagat",false);
	        System.out.println("Book2 issued? "+b2.getIssued());
		Book b3=new Book("Rich dad Poor dad","robert kiyosaki",true);
		System.out.println("Book3 issued? "+b3.getIssued());
		System.out.println("Total Books issued: "+b1.totalIssuedBooks);
	}
}
```

<img width="1103" height="255" alt="Screenshot from 2025-08-30 17-43-18" src="https://github.com/user-attachments/assets/d50c4876-b354-4924-8d74-c73290a742a0" />

## Problem 4: Employee Salary Manager
### Scenario: A company in Bengaluru wants to maintain employee details and give a bonus to employees
### who have worked more than 5 years.

**Requirements:
1. Create a class Employee with instance variables: name (String), salary (double), yearsOfService (int).
2. Create static variable totalEmployees to store the number of employees created.
3. Constructor should initialize all instance variables and increment totalEmployees.
4. Create getters and setters for all instance variables.
5. Create a method calculateBonus() that returns 5% of salary if yearsOfService > 5, otherwise 0.
6. Create a static method showTotalEmployees() to print total employees created.
7. Write a main class to create 3 employees, print their bonuses, and print total employees.
Input Example:
Employee1: Name: "Ravi", Salary: 150000, Years of Service: 6
Employee2: Name: "Anita", Salary: 120000, Years of Service: 3
Employee3: Name: "Suresh", Salary: 100000, Years of Service: 5
Expected Output:
Employee Ravi Bonus: 7500.0
Employee Anita Bonus: 0.0
Employee Suresh Bonus: 0.0
Total employees: 3**

```
class Employees{
	String name;
	double salary;
	int year_of_service;

	static int totalEmployees;

	Employees(String name,double salary,int year_of_service){
		this.name=name;
		this.salary=salary;
		this.year_of_service=year_of_service;

		totalEmployees++;
	}





	String getName(){
		
		return name;
	
	}

	double getSalary(){

		return salary;
	
	}

	int getYearOfService(){
		return year_of_service;	
	}

	double calculateBonus(){
		double bonus;
		bonus=year_of_service>5 ? salary*0.05 :0;
		return bonus;	
	}
	static void showTotalEmployees(){
		System.out.println(totalEmployees);
	
	}


	public static void main(String args[]){

		Employees e1=new Employees("Ravi",150000,6);
		System.out.println("Employee Ravi Bonus : "+e1.calculateBonus());
		Employees e2=new Employees("Anita",120000,3);
		System.out.println("Employee Anita Bonus : "+e2.calculateBonus());
		Employees e3=new Employees("Suresh",100000,5);
		System.out.println("Employee Suresh Bonus : "+e3.calculateBonus());
		showTotalEmployees();

	}


}
```

## Problem 5: Student Marks Calculator
### Scenario: A school in Mumbai wants to calculate marks of students and also maintain total students in
### the class.

**Requirements:
1. Create a class Student with instance variables: name (String), marks (int).
2. Create static variable totalStudents to count total number of students.
3. Constructor to initialize student details and increment totalStudents.
4. Getter and Setter for marks.
5. Method isPassed() returns true if marks >= 35, false otherwise.
6. Static method showTotalStudents() prints total students.
7. In main class, create 3 students, check if they passed, and show total students.
Input Example:
Student1: Name: "Rahul", Marks: 78
Student2: Name: "Pooja", Marks: 34
Student3: Name: "Amit", Marks: 65
Expected Output:
Student Rahul Passed? true
Student Pooja Passed? false
Student Amit Passed? true
Total students: 3**

```
import java.util.Scanner;

class Students{

	String name;
	private int marks;

	static int totalStudents;

	Students(String name,int marks){
		this.name=name;
		this.marks=marks;

		totalStudents++;
	}



	void setMarks(int marks){
		this.marks=marks;
	}

	int getMarks(){
		return marks;
	}

	Boolean isPassed(int marks){
		Boolean pass;

		return pass = (marks>35) ? true : false;
	}

	static void showTotalStudents(){
		System.out.println(totalStudents);
	}

	public static void main(String args[]){

		Scanner s = new Scanner(System.in);

		System.out.print("Student1 Name: ");
		String Student1=s.nextLine();
		System.out.print("Marks");
		int marks1=Integer.parseInt(s.nextLine());

		Students s1= new Students(Student1,marks1);


		System.out.print("Student2 Name: ");
                String Student2=s.nextLine();
		//System.out.println(Student2);
                System.out.print("Marks");
                int marks2=Integer.parseInt(s.nextLine());

		Students s2= new Students(Student2,marks2);


		System.out.print("Student3 Name: ");
                String Student3=s.nextLine();
                System.out.print("Marks");
		// dont use nextInt As it add /n character to input buffer
                int marks3=Integer.parseInt(s.nextLine());
                System.out.print(" ");

		Students s3= new Students(Student3,marks3);

		System.out.println("Student "+Student1+" passed?"+ s1.isPassed(s1.getMarks()));


		System.out.println("Student "+Student2+" passed?"+ s2.isPassed(s2.getMarks()));

                System.out.println("Student "+Student3+" passed?"+ s3.isPassed(s3.getMarks()));

		showTotalStudents();


	}

}
```
