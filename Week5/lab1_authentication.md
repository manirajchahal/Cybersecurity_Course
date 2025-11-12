# Lab 1: Authentication and Session Management

## Objective
Learn secure authentication practices and session management.

## Prerequisites
- Understanding of HTTP and cookies
- Basic web development skills

## Tasks

### Task 1: Insecure Authentication
Identify vulnerabilities in this code:
```python
@app.route('/login', methods=['POST'])
def login():
    username = request.form['username']
    password = request.form['password']
    
    # INSECURE - plaintext password comparison
    if username == "admin" and password == "password123":
        session['user'] = username
        return "Login successful"
    return "Login failed"
```

### Task 2: Secure Password Storage
Implement secure password hashing:
```python
from werkzeug.security import generate_password_hash, check_password_hash

# Storing password
hashed_password = generate_password_hash('user_password', method='pbkdf2:sha256')

# Verifying password
if check_password_hash(hashed_password, provided_password):
    print("Password correct!")
```

### Task 3: Session Management
Implement secure session handling:
```python
from flask import Flask, session
import secrets

app = Flask(__name__)
app.secret_key = secrets.token_hex(32)  # Generate secure secret key

@app.route('/login', methods=['POST'])
def login():
    # After successful authentication
    session.permanent = True
    session['user_id'] = user.id
    session['csrf_token'] = secrets.token_hex(16)
    return "Login successful"

@app.route('/logout')
def logout():
    session.clear()
    return "Logged out"
```

### Task 4: Multi-Factor Authentication (MFA)
Research and document MFA implementation using TOTP:
```python
import pyotp

# Generate secret for user
secret = pyotp.random_base32()

# Create TOTP object
totp = pyotp.TOTP(secret)

# Verify token
if totp.verify(user_provided_token):
    print("Valid token!")
```

## Deliverables
- Secure authentication implementation
- Session management code
- MFA research report

## Questions
1. What is the difference between authentication and authorization?
2. Why should passwords never be stored in plaintext?
3. What is a session token and how should it be protected?
4. What are the benefits of multi-factor authentication?
5. What is OAuth and how does it differ from traditional authentication?
