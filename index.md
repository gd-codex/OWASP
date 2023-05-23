# OWASP TOP 10


Open Worldwide Application Security Project (OWASP)is a non-profit foundation that works to improve the security of software

Their mission:
> No more insecure software


Based on research, OWASP has formulated an awareness document that illustrates critical security risks to web applications, also known as the ***OWASP Top 10***


It has derived and categorized the vulnerabilities based on two sources of data:
- Data submitted by participating organisations, security vendors, consultancies and bug bounties
- Community survey with application security and development experts exploring essential weaknesses that the data may not show yet


## 1. Broken Access Control

### What is Access Control
Access control is a security mechanism to control user access to resources in computing environment.

### What is Broken Access Control
  - Ability to access something without authentication
  - Ability to access something without authorization

### Examples
  - Imagine a web application wherein modifying the URL elevates user role and could possible lead to a data breach or misuse
  ```
     http://xyz.com/user1

     http://xyz.com/admin
  ```

  - Having access to production database when you are entitled to only have access to non-production databases


### Prevention
- Least privelege principle, deny by default(Become a "No Man")
- Design access control schemes upfront and periodically review them
- Logging, monitoring and alerting any access control failures
- Good testing


## 2. Cryptographic Errors
### What is meant by Cryptography
Protecting information(data) and communications by the use of encryption so that only authorized uses of the information could access it.

### What are Cryptographic Error
Insufficient protection of sensitive data resulting in its exposure to unauthorized, potentially dangerous audience with malicious intent. This can happen to both data at rest or data in transit.

### Examples
- You are connected to an unsecured network which has been hacked
  - You can connect to a HTTP website and enter your credentails
  - The hacker can access your information because its unencrypted
  - If you share credentials across different websites, the hacker can easily gain access to those websites to steal sensitive information

- Storing or retrieving passwords in plain text

### Prevention
- For web applications,use HTTPS instead of HTTP so that no third part has access to a communication
- Encrypt all sensitive data at rest
- Using authenticated encryption which creates a Message Authentication Code(MAC) to ensure authenticity of data
- Do not store sensitive data unless it is absolutely necessary
- Work towards better Logging and alerting capabilities






## 3. Injection
### What is meant by Injection
Injection is adding a malicious code to trick the interpreter in a computing environment to execute unintended commands or revealing sensitive information. It can happen through various means but the commonly ones are SQL, No SQL, OS command, Object Relational Mapping(ORM), LDAP and Expression Language (EL) or Object Graph Navigation Library (OGNL) injection

## 4. Insecure Design
### Description
### Mitigation

## 5. Security Misconfiguration
### Description
### Mitigation

## 6. Vulnerable and Outdated Components
### Description

### Mitigation:
  - Software Composition Analysis tools to check what components are used, which have vulnerabilities and outdated
  - SCA Can be added to build pipelines
  - Respond quickly to when new vulnerabilities are exposed

## 7. Identification and Authentication Failures
### Description
### Mitigation

## 8. Software and Data Integrity Failures
### Description
### Mitigation

## 9. Secure Logging and Monitoring Failures
### Description
### Mitigation

## 10. Service-Side Request Forgery
### Description
### Mitigation

## References
- https://owasp.org/www-project-top-ten/
