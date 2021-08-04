#### Authentication is the verification of *who you are* and Authorization is the verification of *what you have the right to do*.

When it comes to securing systems, there are two key concepts to be aware of: authentication and authorization. Although these terms may sound similar, they represent two very different things, and understanding the difference is key to keeping yourself, your devices, and your systems secure.

Authentication is the verification of who you are
Authorization is the verification of what you have the right to do
For example, let’s say you’ve gone to a concert. At the front door, the security guard asks to see your ticket and your ID in order to verify that the name on your ID matches the name on your ticket. This is authentication. You then give your ticket to the security guard who only allows you to pass into General Admissions (instead of the VIP section). This is authorization.

![](https://static-assets.codecademy.com/Courses/introduction-to-cybersecurity/authentication-authorization/Cybersecurity_AuthenticationvAuthorization-04-04.svg)

## Different Authentication Methods
Usually, you have to be authenticated before you can be authorized and the cyber world is no different. There are many different kinds of authentication, the most common of which is a password. However, the PIN number you enter when you withdraw money from an ATM, the fingerprint or face ID you use to unlock your phone, and personal information such as your phone number, social security number, or address are all forms of authentication.

The number of ways you need to authenticate yourself before you can access a resource is also important. As a general rule, the more forms of authentication required to access an asset, such as a bank account or a secure webpage, the more secure the asset is.

## Single-Factor Authentication
Single-Factor authentication refers to when only one form of authentication is used. For example, when you log in to a webpage using only a username and password and are granted access, that is single-factor authentication. Single-factor authentication is more common than Multi-Factor Authentication because it is the most convenient for users and involves less engineering. Users don’t have to remember or have on hand as many means of authentication, so they can more easily access resources.

Unfortunately, due to evolving threats against common methods of single-factor authentication, this method is becoming increasingly insecure.
![](https://static-assets.codecademy.com/Courses/introduction-to-cybersecurity/authentication-authorization/Cybersecurity_SingleFactorAuth.svg)


## Threats to Single-Factor Authentication
Passwords are the most common type of authentication used in Single-Factor Authentication and are vulnerable to credential stuffing, brute forcing, phishing, social engineering, and malware. In fact, with some studies suggesting that 80% of data breaches in 2019 were caused by password compromise, it’s clear that passwords are not a sufficient means of securing systems.

How about PIN codes? Well, let’s say you go to your local coffee shop to work on your Codecademy Cybersecurity course and are so focused that you don’t notice your wallet is missing. Now that they have your debit card, how hard would it be for them to guess the PIN?

Unfortunately, probably not very hard. If your PIN code is 1234, then you are one of about 11% of Americans to have used this secret number. Is your pin 1111? Then you’re one of the 6%! Maybe you thought you’d be clever and use your birthdate? Unfortunately, that’s written down on the driver’s license that’s in your wallet next to your debit card. In fact, a study of 3.4 million PIN codes showed that over a quarter of them were guessable in under 20 tries.

Ranking	PIN	Frequency
#1	1234	10.713%
#2	1111	6.016%
#3	0000	1.881%
#4	1212	1.197%
#5	7777	0.745%
#6	1004	0.616%
#7	2000	0.613%
#8	4444	0.526%
#9	2222	0.516%
#10	6969	0.512%

## Multi-Factor Authentication
![](https://static-assets.codecademy.com/Courses/introduction-to-cybersecurity/authentication-authorization/Cybersecurity_MultiFactorAuth_v2-07.svg)
#
Multi-Factor Authentication (MFA) is the use of multiple types of authentication in order to access a single resource. The most common form of Multi-Factor Authentication is Two-Factor Authentication (2FA). For example, if you log into your bank’s website with a username and password, and then receive a text message with a One-Time Passcode (OTP) that you also need to enter to gain access to your bank account. That is an example of 2FA (and MFA).

MFA can take many forms. For example, instead of sending an OTP in a text message, many organizations utilize ** app-based codes. Apps like Google Authenticator and YubiKey provide passcodes to services that partner with it through free applications on your phone. These codes regenerate every few seconds so an attacker doesn’t have time to **brute force (try every single combination of) your OTP.

![](https://static-assets.codecademy.com/Courses/introduction-to-cybersecurity/authentication-authorization/google_authenticator_screen.png)

MFA is far more secure than Single-Factor Authentication and should always be used with important accounts such as your bank. With Single-Factor Authentication, all an attacker needs is your password or PIN. But with MFA, the attacker would need both your password and access to your cell phone or email to receive a passcode, something they are far less likely to have.

Nevertheless, MFA is still vulnerable to certain kinds of attacks such as SIM Swapping, a social engineering attack in which an attacker remotely steals a victim’s telephone number to receive a text-based OTP. App-based codes are secure against sim swapping, but vulnerable to certain types of mobile malware that can infect your phone and steal these codes. Certain operating systems and phone models (particularly iOS) are more secure against mobile malware, but any form of authentication is vulnerable to being stolen.

Not all applications have MFA; it is up to each organization’s security engineering team to make it available. However, even though MFA makes it slightly less convenient for you, the user, enabling MFA on your accounts when available is one of the single biggest things you can do to protect yourself online.

## How Does a Website Give Me Access After I Log In?
Now that we’ve looked at the different ways that users authenticate themselves, we have to think about how that data is securely communicated to a service we want to use. When the user enters their username and password on a website and hits “Submit”, what happens? Your web browser submits that information to the server’s API to authenticate you. An API is the part of a server that sends and receives data. There are three main types of API authentication:

### HTTP Basic Auth
### API Keys
### OAuth
### HTTP Basic Auth
HTTP Basic Auth is the oldest (since 1999) and simplest method of authentication. It simply requires you to send your username and password every time you communicate with the web page. The reason this isn’t necessary when you use your browser is because of something called cookies. Cookies store your credentials so that you don’t need to send them every time you click on a button.

API Keys
API Keys are similar to HTTP Basic Auth except, instead of a username and password, you use something called an API token. An API token is a unique string of letters and numbers generated for each user. API Keys are frequently used by developers to authenticate their own scripts or applications when interacting with another application’s API. For example, you can use them to authenticate a script that queries a website for large amounts of data or to authenticate a bot on Discord. API Keys have the added advantage of being long and difficult to guess.

Unfortunately, API Keys are too long and complex to be practical for everyday users to use them to log in, and like the credentials used in HTTP Basic Auth, they are vulnerable to interception when they are submitted for authentication.

OAuth
Sometimes we don’t even have to create a username and password for a new account. Instead, we can sign in with Google, LinkedIn, Twitter, and more. This is possible because of OAuth. How does this work? Here’s how it looks on Codecademy:

If you go to the Codecademy sign-up screen, at the bottom you have the option to authenticate using LinkedIn, Google, Facebook, or Github. Let’s say you choose the “Sign in with GitHub” option.

![](https://static-assets.codecademy.com/Courses/introduction-to-cybersecurity/authentication-authorization/login_page.png)

![](https://static-assets.codecademy.com/Courses/introduction-to-cybersecurity/authentication-authorization/Cybersecurity_OAuth_v2-05.svg)

### Role-Based Access Control
Finally, now that we’ve talked about authentication, authorization, and the ways that APIs do this, there is an important concept called Role-Based Access Control (RBAC).

Role-based access is exactly what it sounds like: you have permissions to access certain things (authorization) based on your role/responsibilities (authentication). For example, a professor and a student may both have access to enter the same university. However, the student may have access to the dorms whereas the professor does not, and the professor may have access to the faculty offices whereas the student does not.

In an enterprise environment, role-based access is usually controlled through a system of users and roles. Each user is placed in a role and given access to all of the systems that come with that role. By ensuring that each user has only the access necessary for their role, systems become more secure while streamlining operational efficiency.

Implementation is similar in a web application. For example, in an online forum users may be forum guests, members, or administrators. Guests may only have permission to view posts, members to view and create posts, and administrators to view, create, and delete posts.