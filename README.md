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

