# nestjs-login

## Simple login and auth API in NestJS

## Copy the following lines to run the server
```bash
npm i -g @nestjs/cli 
npm install --save @nestjs/passport passport passport-local 
npm install --save-dev @types/passport-local 
npm install --save @nestjs/jwt passport-jwt 
npm install --save-dev @types/passport-jwt 
```

## POST Login command (usingg curl)

```
curl -X POST http://localhost:3000/auth/login -d "{\"username\": \"ahmed\", \"password\": \"blahblah\"}" -H "Content-Type: application/json" 
```
returns `{"access_token":TOKEN}`

## GET Profile 
make sure to use previously generated `TOKEN` to get profile
```
curl http://localhost:3000/profile -H "Authorization: Bearer TOKEN"
```
returns `{"userId":1,"username":"ahmed"}`