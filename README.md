# datasecurity
a readme to hold all my research on database vulnerabilities


Cross Site Scripting (XSS)
Specifically, how is this type of attack conducted?
- injection, malicious scripts are put into trusted websites through a web application that sends malicious code to a different end user

What are the biggest risks from this type of attack?
- executing unknown code/script from a website you believe was trusted

How can this type of attack be defended against?
-framework security; understanding where it has gaps (output encoding HTML sanitization)
- example: escape hatches used to manipulate DOM
- React's setInnerHTML without sanitising the HTML
- angular bypass Security Trust as
- template injection
-out of date framework plugins and components

- ensure all variables go through validation = perfect injection resistance

-output encoding
- dispaly data as a user typed it

Are there notable examples of this type of attack in the news?
wordpress plugin, used by over 200,000 websites (anti-malware security and brute-force firewall are plugins) failure to restrstrict (sanitize) what is being uploaded, someone uploaded a script and reflected it back through the site (Reflected xss)
- 2 weeks ago


----

Specifically, how is this type of attack conducted?
-code injection occurs when a user inputs sql statement that steals data from your database

What are the biggest risks from this type of attack?
- input areas for user id / passwords

How can this type of attack be defended against?
-use sql parameters, values that are added to a query at execution time in a controlled manner.
- sql engine checks each parameter to ensure that it is correct for the column and treated literally, not part of the sql to be executed

Are there notable examples of this type of attack in the news?
- accellion attack, creator of a file transfer appliance
-epic games in 2016
----
Cyber Security Acitivty:

2016 Election
1) What type of attack was this?
The hacking incident during the 2016 presidential race between Donald Trump and Hillary Clinton began with a phishing email that through some chance and human error became legitimized when a staffer mistyped illegitimate as legitimate. The recipient of the email, John Podesta (Hiliary Clinton's campaign chairman) made his email vulnerable and was compromised when he followed the directions in the email to change his password. The hacker(s) then forwarded over 30 emails to the rest of the team to a document that lead to a website owned by the hackers which ran scripts on the computers stealing thousands of emails from the staffers. This is a form of cross site scripting, which used the legitimacy of John Podesta's email to secure vulnerable information.

2) How was the vulnerability discovered?
The FBI suspected this might happen months ago and the vulnerability was discovered after the attack happened.

3) How were the attackers able to exploit the vulnerability?
By proxying their script through a legimiate email.

4) Were there security measures that could have been taken in order to prevent this attack?
This requires staffers to suspect and double/triple check or improve their protocols before accessing suspect email links, or by having their communication software monitor when links like this are being sent.

----
Broadvoice Data Breach

1) What type of attack was this?
A cluster of databases that contained sensitive customer records including names, phone numbers, and other personal information was left open and unprotected without a password required to access it. Over 350million users were affected.

2) How was the vulnerability discovered?
A security expert Bob Diachenko uncovered the database on October 1, 2020.

3) How were the attackers able to exploit the vulnerability?
With an unprotected cluster of databases, hackers can gain access to sensitive information and potentially inflict malicious attacks or impersonate others for financial gain. Criminals can pose as Broadvoice clients or even broadvoice staff themselves to gain even more financial or account information.

4) Were there security measures that could have been taken in order to prevent this attack?
Data exposure such as this is easily avoidable by protecting your database. The company announced that the database was secured on October 4, 2020.
