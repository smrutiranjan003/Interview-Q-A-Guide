# VVDN FRESHER INTERVIEW PREP

**Cloud + DevOps Trainee | Final Interview-Ready Guide**

---

## EXPECTED CODING QUESTIONS (WITH ANSWERS – C LANGUAGE)

---

## 1. Reverse a String

**Logic**

* Traverse string from end
* Print characters in reverse order

**C Code**

```c
#include <stdio.h>
#include <string.h>

int main() {
    char s[] = "cloud";
    int len = strlen(s);

    for(int i = len - 1; i >= 0; i--) {
        printf("%c", s[i]);
    }
    return 0;
}
```

---

## 2. Find Largest Number in Array

**Logic**

* Assume first element is max
* Compare with remaining elements

```c
#include <stdio.h>

int main() {
    int arr[] = {3, 5, 1, 9};
    int size = 4;
    int max = arr[0];

    for(int i = 1; i < size; i++) {
        if(arr[i] > max) {
            max = arr[i];
        }
    }

    printf("Largest number: %d", max);
    return 0;
}
```

---

## 3. Palindrome Check

```c
#include <stdio.h>
#include <string.h>

int main() {
    char s[] = "madam";
    int len = strlen(s);
    int flag = 1;

    for(int i = 0; i < len / 2; i++) {
        if(s[i] != s[len - i - 1]) {
            flag = 0;
            break;
        }
    }

    if(flag)
        printf("Palindrome");
    else
        printf("Not Palindrome");

    return 0;
}
```

---

## 4. Count Vowels in String

```c
#include <stdio.h>

int main() {
    char s[] = "cloudcomputing";
    int count = 0;

    for(int i = 0; s[i] != '\0'; i++) {
        if(s[i]=='a' || s[i]=='e' || s[i]=='i' || 
           s[i]=='o' || s[i]=='u') {
            count++;
        }
    }

    printf("Vowel count: %d", count);
    return 0;
}
```

---

## HOW TO EXPLAIN IN INTERVIEW (IMPORTANT FOR C)

If interviewer asks **how this works**, say:

> “I used basic loops and string handling in C. I focused on clarity and logic rather than complex functions, which is suitable for fresher-level programs.”

This answer is **safe and correct**.

---

## OOPS CONCEPTS (With Real-Life Examples)

### 1. Encapsulation

**Definition**
Encapsulation means wrapping data and the methods that operate on that data into a single unit and restricting direct access to it.

**Why it is used**

* Protects data
* Improves security
* Controls access

**Real-life example**
A **bank account**.
You cannot directly change your balance. You use methods like deposit or withdraw. The balance is hidden and accessed only through proper functions.

---

### 2. Inheritance

**Definition**
Inheritance allows a class to acquire the properties and behavior of another class.

**Why it is used**

* Code reusability
* Easy maintenance

**Real-life example**
A **car** is a type of **vehicle**.
Vehicle has common properties like engine and wheels. Car inherits them and adds its own features.

---

### 3. Polymorphism

**Definition**
Polymorphism means one action can be performed in different ways.

**Why it is used**

* Flexibility
* Cleaner code

**Real-life example**
A **remote control**.
The same power button works differently for TV, AC, or music system.

---

### 4. Abstraction

**Definition**
Abstraction means showing only essential features and hiding internal implementation.

**Why it is used**

* Reduces complexity
* Improves usability

**Real-life example**
A **car**.
You use steering, brake, and accelerator without knowing how the engine works internally.

---

## SOFTWARE FUNDAMENTALS

### SDLC Phases

SDLC stands for Software Development Life Cycle.

1. Requirement analysis
2. Design
3. Development
4. Testing
5. Deployment
6. Maintenance

Purpose: Build high-quality software in a structured way.

---

### Frontend vs Backend

**Frontend**

* What user sees
* UI part
* HTML, CSS, JavaScript

**Backend**

* Logic and data handling
* Server, database
* Java, Python, APIs

---

### Compiler vs Interpreter

**Compiler**

* Translates entire code at once
* Faster execution
* Example: C, C++

**Interpreter**

* Translates line by line
* Easier debugging
* Example: Python, JavaScript

---

### What is Debugging?

Debugging is the process of finding and fixing errors or bugs in a program to make it work correctly.

---

## DATABASE + API

### What is DBMS?

DBMS is a software that helps to store, retrieve, update, and manage data efficiently.

Examples: MySQL, Oracle, PostgreSQL

---

### SQL vs NoSQL

**SQL**

* Structured data
* Tables, rows, columns
* Fixed schema

**NoSQL**

* Unstructured or semi-structured data
* Flexible schema
* Used in big data and cloud apps

---

### Primary Key and Foreign Key

**Primary Key**

* Uniquely identifies a record
* Cannot be null

**Foreign Key**

* Links one table to another
* Refers to primary key

---

### Basic SQL Queries

```sql
SELECT * FROM students;
INSERT INTO students VALUES (1, 'Ravi');
UPDATE students SET name='Amit' WHERE id=1;
DELETE FROM students WHERE id=1;
```

---

## API CONCEPTS

### What is an API?

API allows two applications to communicate with each other.

Example: Login app sending request to server and getting response.

---

### What is REST API?

REST API follows standard rules using HTTP methods and works over the internet.

It is simple, scalable, and widely used in cloud systems.

---

### HTTP Methods

* GET – Fetch data
* POST – Send data
* PUT – Update data
* DELETE – Remove data

---

### What is JSON?

JSON is a lightweight data format used to exchange data between client and server.

```json
{
  "name": "Smruti",
  "role": "Cloud Trainee"
}
```

---

### Request vs Response

**Request**

* Sent by client
* Contains data or action

**Response**

* Sent by server
* Contains result or data

---

## CLOUD COMPUTING (DAY 2 – HIGH IMPACT)

## INTERVIEW-LEVEL QUESTIONS & ANSWERS (CLOUD FOCUS)

### What is cloud computing?

Cloud computing means using servers, storage, databases, and software over the internet instead of maintaining physical hardware locally.

---

### Why do companies use cloud?

* Cost saving
* Scalability
* High availability
* Faster deployment
* Less maintenance

---

### Difference between IaaS, PaaS, SaaS?

* **IaaS**: Infrastructure as a Service - Infrastructure like Virtual servers and storage (example: EC2)
* **PaaS**: Platform as a Service - Platform to develop and deploy applications
* **SaaS**: Software as a Service - Ready-to-use software over internet (example: Gmail)
---

### What is AWS?

AWS is Amazon’s cloud platform that provides compute, storage, networking, and other services on demand.

---

### What is virtualization?

Virtualization allows multiple virtual machines to run on a single physical server.

---

### What is an API?

API allows two applications to communicate with each other using request and response.

---

## LINUX BASICS

### What is Linux?

Linux is an open-source operating system widely used in servers due to stability and security.

### Common Commands

* ls – list files
* cd – change directory
* pwd – current path
* mkdir – create folder
* rm – delete files

### Why Linux for servers?

Lightweight, secure, stable, and cost-effective.

---

## GIT BASICS

### What is Git?

Git is a version control system used to track code changes and collaborate with teams.

### Git vs GitHub

* Git: Tool for version control
* GitHub: Platform to host Git repositories

### Basic Git Workflow

* git clone
* git add
* git commit
* git push

---
## PERFECT “TELL ME ABOUT YOURSELF” (VVDN – CLOUD)

Use this **as-is**, or slightly personalize.

> Good morning, thank you for the opportunity.
>
> I am a Computer Science graduate from the 2024/2025 batch with a strong interest in cloud and backend technologies. I have a solid foundation in programming, mainly using Python/Java, along with knowledge of databases, APIs, and software development fundamentals.
>
> Recently, I have been focusing on cloud computing concepts such as virtualization, cloud service models, and basic AWS services like compute and storage. I also have basic exposure to Linux commands and Git, which I understand are important for cloud and server-side environments.
>
> I am particularly interested in this trainee role at VVDN because it offers structured training, exposure to real-world projects, and long-term growth in advanced technologies like cloud and embedded solutions. I am eager to learn, adaptable to new environments, and comfortable with the service agreement and relocation.
>
> I’m looking forward to contributing, learning from experienced teams, and building a strong career with VVDN.


---

## FINAL INTERVIEW TIP

If interviewer goes deeper:

> At a fresher level, I focused on understanding concepts and implementation basics, and I’m eager to learn deeper in real projects.

---

## Explain Cloud in Simple Words (Interview Gold Answer)

Cloud computing means using servers, storage, and software over the internet instead of installing and maintaining them on our own systems. It helps companies reduce cost, scale easily, and deploy applications faster.

---

## Final Tip

If you forget an answer:
> Say calmly
“I am not fully sure, but I approach this-way based on my understanding…”

This shows honesty and learning mindset.

* Revise this document end to end
* Speak slowly and clearly
* Explain workflow step by step
* Stay calm and confident


---
