# Overview
I assessed the session management and persistent login functionality of a web application. During testing, I identified a vulnerability in the stay-logged-in cookie, which used a predictable base64(username:md5(password)) format. By brute-forcing the hashed password and reconstructing the cookie, I was able to impersonate users and gain unauthorized access. This project highlights how weak cryptographic practices and predictable session tokens can be exploited to compromise authentication and user account integrity.

# Methodology

Step 1: Analyzed the stay-logged-in cookie structure and decoded it to understand the username and MD5 hash format.

Step 2: Brute-forced the password using a wordlist and reconstructed the cookie with the victim’s username.

Step 3: Replaced the cookie in HTTP requests and confirmed successful account takeover by inspecting authenticated page elements.

# Conclusion

This assessment demonstrated a high-severity session management flaw, emphasizing the need for secure, random session tokens and strong cryptographic handling of authentication data to prevent unauthorized account access.
