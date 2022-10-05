# Keycloak - Identity and Access Management for Modern Applications

## Chapter 2. Securing Your First Application

<br/>

What you require before continuing is the following:

• Keycloak up and running
• A realm named myrealm
• A global role named myrole
• A user with the preceding role

<br/>

```
$ cd Keycloak-Identity-and-Access-Management-for-ModernApplications/ch02/frontend/
$ npm install
$ npm start
```

<br/>

```
$ cd Keycloak-Identity-and-Access-Management-for-ModernApplications/ch2/backend/
$ npm install
$ npm start
```

<br/>

http://localhost:8000

<br/>

Clients, and then click on Create

Fill in the form with the following values:
• Client ID: myclient
• Client Protocol: openid-connect
• Root URL: http://localhost:8000
