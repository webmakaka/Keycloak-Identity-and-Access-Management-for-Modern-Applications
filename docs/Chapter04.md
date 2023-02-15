# Keycloak - Identity and Access Management for Modern Applications

## Chapter 04. Securing Your First Application

<br/>

**Requirements:**

• A realm named myrealm  
• A global role named myrole  
• A user with the preceding role

Client with the following configuration:

• Client ID: oidc-playground  
• Access Type: public  
• Valid Redirect URIs: http://localhost:8000/  
• Web Origins: http://localhost:8000

<br/>

```
$ cd Keycloak-Identity-and-Access-Management-for-ModernApplications/ch04/
$ npm install
$ npm start
```

<br/>

http://localhost:8000

Discovery

Issuer: http://localhost:8080/realms/myrealm

Load OpenID Provider Configuration

<br/>

![Application](/img/ch-04-pic-01.png?raw=true)
