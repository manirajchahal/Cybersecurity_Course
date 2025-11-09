# Lab 1: SQL Injection Fundamentals

## Objective
Understand SQL injection vulnerabilities and learn how to prevent them.

## Prerequisites
- Basic understanding of SQL
- Web browser
- (Optional) SQLite or MySQL for local testing

## Legal Notice
⚠️ **IMPORTANT**: Only practice on authorized test environments, CTF platforms, or your own applications.

## Background
SQL Injection occurs when user input is improperly sanitized and directly inserted into SQL queries, allowing attackers to manipulate the database.

## Tasks

### Task 1: Understanding Vulnerable Code
Study this vulnerable PHP code:
```php
<?php
$username = $_POST['username'];
$password = $_POST['password'];

// VULNERABLE - Never do this!
$query = "SELECT * FROM users WHERE username='$username' AND password='$password'";
$result = mysqli_query($conn, $query);

if (mysqli_num_rows($result) > 0) {
    echo "Login successful!";
} else {
    echo "Login failed!";
}
?>
```

Explain why this is vulnerable and what an attacker could do.

### Task 2: SQL Injection Examples
Try these injection payloads (in a test environment):

1. **Authentication Bypass:**
   ```
   Username: admin' OR '1'='1
   Password: anything
   ```
   Resulting query: `SELECT * FROM users WHERE username='admin' OR '1'='1' AND password='anything'`

2. **Comment-based injection:**
   ```
   Username: admin'--
   Password: (leave empty)
   ```
   The `--` comments out the password check

3. **UNION-based injection:**
   ```
   ' UNION SELECT username, password FROM users--
   ```

### Task 3: Create a Simple Vulnerable App
Create a simple Python/Flask or Node.js app with SQL injection vulnerability:

```python
from flask import Flask, request
import sqlite3

app = Flask(__name__)

@app.route('/login', methods=['POST'])
def login():
    username = request.form['username']
    password = request.form['password']
    
    # VULNERABLE CODE - for demonstration only!
    conn = sqlite3.connect('users.db')
    cursor = conn.cursor()
    query = f"SELECT * FROM users WHERE username='{username}' AND password='{password}'"
    cursor.execute(query)
    result = cursor.fetchone()
    
    if result:
        return "Login successful!"
    else:
        return "Login failed!"

if __name__ == '__main__':
    app.run(debug=True)
```

### Task 4: Secure the Code
Fix the vulnerable code using parameterized queries:

```python
# SECURE VERSION
query = "SELECT * FROM users WHERE username=? AND password=?"
cursor.execute(query, (username, password))
```

### Task 5: SQL Injection Types
Research and document:
1. **In-band SQLi**: Union-based, Error-based
2. **Blind SQLi**: Boolean-based, Time-based
3. **Out-of-band SQLi**: Using DNS or HTTP requests

## Practice Platforms
- [PortSwigger Web Security Academy](https://portswigger.net/web-security/sql-injection)
- [DVWA (Damn Vulnerable Web Application)](https://github.com/digininja/DVWA)
- [SQLi Labs](https://github.com/Audi-1/sqli-labs)

## Deliverables
1. Document vulnerable code examples
2. Show exploitation attempts
3. Provide secure code alternatives
4. Answer the questions below

## Questions
1. What is the difference between prepared statements and parameterized queries?
2. How can you detect SQL injection vulnerabilities?
3. What is the purpose of the UNION operator in SQL injection?
4. Why is input validation alone not sufficient to prevent SQL injection?
5. What tools can automate SQL injection testing?

## Prevention Techniques
1. **Use Parameterized Queries/Prepared Statements**
2. **Input Validation**: Whitelist acceptable inputs
3. **Least Privilege**: Database user should have minimal permissions
4. **Web Application Firewall (WAF)**
5. **Regular Security Audits**

## Tools
- **sqlmap**: Automated SQL injection tool
- **Burp Suite**: Web application testing platform
- **OWASP ZAP**: Free security scanner

## Additional Resources
- [SQL Injection Cheat Sheet](https://portswigger.net/web-security/sql-injection/cheat-sheet)
- [OWASP SQL Injection](https://owasp.org/www-community/attacks/SQL_Injection)
