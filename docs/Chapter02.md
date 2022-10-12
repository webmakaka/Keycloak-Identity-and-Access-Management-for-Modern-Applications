# Keycloak - Identity and Access Management for Modern Applications

## Chapter 02. Securing Your First Application

<br/>

**Requirements:**

• Keycloak up and running  
• A realm named: myrealm  
• A global role (Realm Roles): myrole  
• A user with the preceding role. User -> Role mapping -> Assign role -> myrole

<br/>

Clients -> Create

Fill in the form with the following values:

• Client type: openid-connect  
• Client ID: myclient  
• Root URL: http://localhost:8000

- Valid redirect URIs: http://localhost:8000/\*
- Web origins: \*

<br/>

![Application](/img/ch-02-pic-01.png?raw=true)

<br/>

```
$ cd Keycloak-Identity-and-Access-Management-for-ModernApplications/ch02/frontend/
$ npm install
$ npm start
```

<br/>

```
$ cd Keycloak-Identity-and-Access-Management-for-ModernApplications/ch02/backend/
$ npm install
$ npm start
```

<br/>

http://localhost:8000

<br/>

![Application](/img/ch-02-pic-02.png?raw=true)

<br/>

![Application](/img/ch-02-pic-03.png?raw=true)
