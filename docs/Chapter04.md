# Keycloak - Identity and Access Management for Modern Applications

## Chapter 04. Securing Your First Application

<br/>

**Requirements:**

• A realm named myrealm  
• A global role named myrole  
• A user with the preceding role

Client with the following configuration:

• Client type: OpenID Connect 
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


<br/>



```
$ export ENDPOINT_URL=http://localhost:8080/realms/myrealm/protocol/openid-connect/userinfo

$ export AUTH_TOKEN=eyJhbGciOiJSUzI1NiIsInR5cCIgOiAiSldUIiwia2lkIiA6ICJHYlI3VEMzaUhZT3NIUEJ6cnFTWEdEOUlxUnd3c19CLW5EbmVqc1gyR3ZNIn0.eyJleHAiOjE2NzY0NTg5NDUsImlhdCI6MTY3NjQ1ODY0NSwiYXV0aF90aW1lIjoxNjc2NDU3OTcwLCJqdGkiOiJlMWJkOGE3YS1kM2E1LTQwZDAtYTc5ZC02NWY3M2ViNTJmNjciLCJpc3MiOiJodHRwOi8vbG9jYWxob3N0OjgwODAvcmVhbG1zL215cmVhbG0iLCJhdWQiOiJhY2NvdW50Iiwic3ViIjoiOTg1M2Y0MzMtM2JiYy00NDY4LWJlZDktOTg3OGY5MWE1NDYxIiwidHlwIjoiQmVhcmVyIiwiYXpwIjoib2lkYy1wbGF5Z3JvdW5kIiwic2Vzc2lvbl9zdGF0ZSI6IjEzMWE4ODY0LWJkNWQtNDEwMy1hY2MyLTJlMjA5ZTdiYjY2OCIsImFjciI6IjAiLCJhbGxvd2VkLW9yaWdpbnMiOlsiaHR0cDovL2xvY2FsaG9zdDo4MDAwIl0sInJlYWxtX2FjY2VzcyI6eyJyb2xlcyI6WyJkZWZhdWx0LXJvbGVzLW15cmVhbG0iLCJvZmZsaW5lX2FjY2VzcyIsInVtYV9hdXRob3JpemF0aW9uIiwibXlyb2xlIl19LCJyZXNvdXJjZV9hY2Nlc3MiOnsiYWNjb3VudCI6eyJyb2xlcyI6WyJtYW5hZ2UtYWNjb3VudCIsIm1hbmFnZS1hY2NvdW50LWxpbmtzIiwidmlldy1wcm9maWxlIl19fSwic2NvcGUiOiJvcGVuaWQgZW1haWwgcHJvZmlsZSIsInNpZCI6IjEzMWE4ODY0LWJkNWQtNDEwMy1hY2MyLTJlMjA5ZTdiYjY2OCIsImVtYWlsX3ZlcmlmaWVkIjp0cnVlLCJwcmVmZXJyZWRfdXNlcm5hbWUiOiJtYXJsZXkiLCJnaXZlbl9uYW1lIjoiIiwiZmFtaWx5X25hbWUiOiIifQ.n6szYPKT177Oqe1IRhGCii4vIrQUNJdo6uWu6IBCAhLGqGNCdcFN2a2VPDHlm1IFzwqPCR9-PJtmKFTy1N69Ix_lx3xxMZG2i9SQX8gdf9MoBmMTp5YAiSpFhFDTpFOgFPnCesw59tr4uO20e6L-8ESzyXNR2bZjUopZ4Q5EPCRRBWWFsVDVjhnTZrS8w0O2atc6SQt-uC74QYWQTDZfOOBB9NAuPFStpAtMX8fBVu2xoQfCnq_xvQvIv5gRKh8I8kJmq7E69rp_6zmJApg4PiYaQG3d_1X6cRDQVDCGJEAmjTiticam-L6DhSH9-lqyFAYI8i194fWjm40i8VOA-Q
    

$ curl \
    --header "Content-Type: application/json" \
    --header "Authorization: Bearer ${AUTH_TOKEN}" \
    --request GET \
    --url "${ENDPOINT_URL}" \
    | jq
```

**response**

```
{
  "sub": "9853f433-3bbc-4468-bed9-9878f91a5461",
  "email_verified": true,
  "preferred_username": "marley",
  "given_name": "",
  "family_name": ""
}
```
