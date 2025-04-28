# Password Policy Compliance Activity
>https://app.pluralsight.com/labs/detail/cae8d517-5b65-4b2d-a762-d72a8e8401e6/toc

## Activity Introduction
"You are a compliance assessor at Globomantics and your task is to determine whether Globomantics complies with its own password policies and also the relevant requirements in the Payment Card Industry (PCI) Data Security Standard (DSS).

You will meet with four Globomantics colleagues who will show you the evidence you need to form an opinion of whether the policies and requirements are being met.

At the end of the lab you'll be asked to provide your compliance assessments. You can compare these with the lab assessor's answers."

## Task Overview

![](Images/overview.png)
## Key Information

Before the meetings begin, there is an overview of the relevant information to do this task correctly. This includes the company **Information Security Policy**, and the Payment Card Industry (**PCI**) Data Security Standard (**DSS**).

![](Images/securitypolicy.png)

### Payment Card Industry Data Security Standard (PCI DSS) Requirements
> Requirement 8.3

_This is an extract of the relevant PCI DSS requirements that you are assessing in this lab_
**Requirement 8.3: Strong authentication for users and administrators is established and managed.**
**8.3.1** All user access to system components for users and administrators is authenticated via at least one of the following authentication factors:

- Something you know, such as a password or passphrase.
- Something you have, such as a token device or smart card.
- Something you are, such as a biometric element

**8.3.2** Strong cryptography is used to render all authentication factors unreadable during transmission and storage on all system components.
**8.3.3** User identity is verified before modifying any authentication factor.
**8.3.4** Invalid authentication attempts are limited by:

- Locking out the user ID after not more than 10 attempts.
- Setting the lockout duration to a minimum of 30 minutes or until the user’s identity is confirmed.

**8.3.5** If passwords/passphrases are used as authentication factors to meet Requirement 8.3.1, they are set and reset for each user as follows:

- Set to a unique value for first-time use and upon reset.
- Forced to be changed immediately after the first use. 

**8.3.6** If passwords/passphrases are used as authentication factors to meet Requirement 8.3.1, they meet the following minimum level of complexity:

- A minimum length of 12 characters (or IF the system does not support 12 characters, a minimum length of eight characters)
- Contain both numeric and alphabetic characters. 

**8.3.7** Individuals are not allowed to submit a new password/passphrase that is the same as any of the last four passwords/passphrases used.
**8.3.8** Authentication policies and procedures are documented and communicated to all users including:

- Guidance on selecting strong authentication factors.
- Guidance for how users should protect their authentication factors.
- Instructions not to reuse previously used passwords/passphrases.
- Instructions to change passwords/passphrases if there is any suspicion or knowledge that the password/passphrases have been compromised and how to report the incident.


**8.3.9** If passwords/passphrases are used as the only authentication factor for user access (i.e., in any single-factor authentication implementation) then either:

- Passwords/passphrases are changed at least once every 90 days, or
- The security posture of accounts is dynamically analysed, and real-time access to resources is automatically determined accordingly. 


---

### Task Begin

![](Images/assessmentplan.png)

First meeting is George, the Active Directory Administrator. He shows that the company has correct complexity requirements for passwords, as well as correct requirements for maximum password age.

![](Images/yesplease.png)
![](Images/complexity.png)
![](Images/strike.png)
![](Images/ithinkso.png)
![](Images/enabled.png)
![](Images/inthebin.png)
![](Images/donegeorge.png)
The meeting with George also proved that MFA (Multi-Factor-Authentication) is enabled for every user in the company, users get locked out after three attempts and their account must be re-enabled by the service desk manually. It also shows that new passwords must be changed at first logon. This is all in compliance with the companies internal Information Security policy, but it is **not in compliance** with the Payment Card Industry (PCI) Data Security Standard (DSS) **section 8.3.6**. This is because the PCI DSS document states a minimum length of 12 characters for a password, whereas the policy in place is only 8.

Before the meeting with Tasneem, there is an opportunity to get coffee at the canteen, where another conversation is heard about passwords.

![](Images/read.png)
![](Images/comeonjohn.png)

This conversation is alarming because it shows a dismissive attitude towards the security measures in place, and even more alarming is that it's mentioned that procedures have been modified to accommodate this compliance assessment.

After getting a coffee, and one for Tasneem, the next meeting can begin.

![](Images/waiting.png)
![](Images/hash.png)

Tasneem explains that all encryption standards are met easily by using Microsoft's Active Directory, which automatically encrypts all passwords securely at rest and transit.

The next meeting is with David the Helpdesk Agent.

![](Images/passreset.png)
![](Images/procedure.png)
![](Images/verify.png)
![](Images/call.png)
![](Images/watchdavid.png)

When questioning David about the process of a password reset, he mentions that they often use Password1 when resetting the passwords because they get many of these type of calls and using Password1 makes the process easier for the user. 
Whilst there is a policy in place to make sure this password gets changed upon logon, this is still technically in breach of the Payment Card Industry (PCI) Data Security Standard (DSS) because the reset password is not unique. This is specified in **section 8.3.5 of the PCI DSS document.**

![](Images/heyarnlond.png)
![](Images/badpolicy.png)
![](Images/notunusual.png)
![](Images/review.png)

During the meeting with Arnold, the Acceptable Use Policy can be viewed. Upon reading the policy it is clear that there is not sufficient detail and advice in order for it to be compliant with the **PCI DSS section 8.3.8**, because it does not instruct employees to never use the same password twice for the same system, and it does not explain what an employee should do if they lose their smart card. Therefore the company cannot be compliant with **PCI DSS section 8.3.8**

![](Images/confirm.png)

>[Overview of the training](Your-Role-in-Protecting-the-Company.md)
### Compliance Assessment

![](Images/yourassessment.png)
![](Images/answers.png)
![](Images/answers2.png)

### Non Compliance:

#### 8.3.5
In the PCI DSS document, it is stated that when a password gets reset, it must be set to a unique value. However in the interview with david, it is mentioned that passwords are often reset to "password1".
#### 8.3.6
In the PCI DSS document, it is stated that if a password or passphrase is used to authenticate a login, it must be at least 12 characters. But when George showed us the enforced password rules, it was shown to be only 8.
#### 8.6.8
This section specifies in detail what information should be instructions should be given to employees regarding devices and security. It states that all users must be informed to never use the same password twice on the same system, and that all users must be provided with clear instructions on what to do if they believe an authorisation method of theirs has been compromised. These two things are not included in the Acceptable Use Policy that the company issues to its employees, and therefore it is in breach of this section of the PCI DSS. 


### Result:
![](Images/okay.png)
![](Images/what.png)
> This seems to be a bug in the Pluralsight system, I chose "compliant" for this option as seen in the screenshots included earlier. 

## Notes

- The first time I did this activity, I got 17/20 correct answers. I missed the AUP violations and password reset compliance breach because I didn't read the documents carefully enough. Doing the lab several times is also how I know that one of the answers is bugged rather than being user error.
	**Lessons Learned**:
	- When evaluating policy compliance within organisations, it is crucial to be as thorough as possible. You have to be patient and take time to carefully review both the compliance frameworks, and the internal policy documentation, documenting exact requirements so you can cross-reference them to identify any discrepancies or potential breaches.

