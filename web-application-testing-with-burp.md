# Web Application Testing with Burp Suite

## Objective

Learn web application testing fundamentals by configuring Burp Suite as an intercepting proxy and analyzing traffic to DVWA hosted on Metasploitable.

## Environment

### Attacker

- Kali Linux
- Burp Suite

### Target

- DVWA
- Metasploitable 2

## Lab Architecture

Kali Linux
↓
Burp Suite
↓
DVWA on Metasploitable

## Activities Performed

### Proxy Configuration

Configured Firefox to route HTTP traffic through Burp Suite on port 8080.

### Request Interception

Captured HTTP requests and responses between the browser and DVWA.

### Authentication Analysis

Observed login requests and analyzed submitted credentials and session cookies.

### Repeater Testing

Modified requests using Burp Repeater and compared application responses.

### Cookie Inspection

Reviewed session cookies and application security settings.

## Skills Demonstrated

- HTTP Fundamentals
- Web Application Testing
- Proxy Configuration
- Request Analysis
- Session Management
- Burp Suite Usage

## Lessons Learned

Web applications trust user-supplied data more than many people realize. Intercepting and modifying requests provides insight into how applications process authentication, sessions, and user input.

## Screenshots

- Burp Intercept
- Login Request
- Repeater Testing
- Session Cookies
- DVWA Dashboard
