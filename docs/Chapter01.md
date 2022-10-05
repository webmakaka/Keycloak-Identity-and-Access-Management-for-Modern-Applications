# Keycloak - Identity and Access Management for Modern Applications

## Chapter 1. Getting Started with Keycloak

<br/>

### Running Keycloak on Docker

```
$ docker run -p 8080:8080 -e KEYCLOAK_ADMIN=admin -e KEYCLOAK_ADMIN_PASSWORD=admin quay.io/keycloak/keycloak:19.0.2 start-dev
```

<br/>

http://localhost:8080

<br/>

### Installing and running Keycloak with OpenJDK

```
$ sudo dnf install java-latest-openjdk
```

<br/>

https://www.keycloak.org/downloads

<br/>

**Installing Keycloak**

```
$ cd ~/kc-book
$ unzip ~/Downloads/keycloak-11.0.1.zip
$ cd keycloak-11.0.1
$ export KC_HOME=~/kc-book/keycloak-11.0.1
```

<br/>

**Creating an admin account**

```
$ cd $KC_HOME
$ bin/add-user-keycloak.sh -u admin -p admin
```

<br/>

**Starting Keycloak**

```
$ cd $KC_HOME
$ bin/standalone.sh
```

<br/>

http://localhost:8080

<br/>

```
Create realm: myrealm
Creating a user: marley
```
