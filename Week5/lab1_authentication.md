Week 5 Lab — Authentication, Cookies, and Sessions (Beginner-Friendly)
=========================================================================

**Objective**
-------------

Learn how authentication works on the web by exploring insecure login pages, cookies, and session behavior — without needing to write code.

**Prerequisites**
-----------------

No coding required.You only need:

*   A browser (Chrome recommended)
    
*   Access to one of the demo sites below
    

**Demo Sites (Choose One)**
---------------------------

Safe intentionally-vulnerable sites:

*   **AltoroJ Testfire**: [https://demo.testfire.net/login.jsp](https://demo.testfire.net/login.jsp)
    
*   **OWASP Juice Shop**: https://juice-shop.herokuapp.com/#/login
    

**Task 1 — Explore an Insecure Login Page**
==============================================

1.  Visit the demo site’s login page.
    
2.  Try random usernames & passwords.
    
3.  Observe error messages.
    
4.  Open:
    
    *   DevTools → **Network** → Submit login again
        
5.  Notice how the browser sends authentication data to the server.
    

**Goal:** Understand the basic login flow.


**Task 2 — Test Simple Authentication Weaknesses**
=====================================================

### **Option A — Username Enumeration**

1.  Try logging in with a fake username.
    
2.  Try logging in with "admin".
    
3.  Compare error messages.
    

### **Option B — Weak Password Attempts**

Try passwords like:

*   admin
    
*   password
    
*   123456
    
*   admin123
    

**Goal:** Learn how attackers spot weak authentication behaviors.



**Review Questions**
===================================

Students submit short answers (1–2 sentences each):

1.  What is authentication?
    
2.  What is a cookie and why do websites use them?
    
3   What weakness did you find on the demo site?
    
4.  Why is multi-factor authentication safer than a password alone?
