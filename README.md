# HTML Analyzer

HTML Analyzer is a web-application that does some analysis of a web-page/URL.

## Demo
* [Live Demo](live.htmlanalyzer.cloud)

## Git History
* [html-analyzer-client git history](https://github.com/siffogh/html-analyzer-client/commits/master)
* [html-analyzer-server git history](https://github.com/siffogh/html-analyzer-server/commits/master)
* [html-analyzer-docker git history](https://github.com/siffogh/html-analyzer-client/commits/master)

## Instructions to Run

* Make sure you have Docker installed on your machine.
* The app front-end can be viewed on the browser based on the environment (production or development).
* The api can be tested by tools such as live.htmlanalyzer.cloud

### Run in Development Mode
* To run in development mode, execute the following script:
``` npm start ```
* The web app can be then accessed at ```http://localhost:6082```
* Api address: ```http://localhost:6081```


### Run in Production Mode
* To run in production mode, execute the following script:
``` npm run build ```
* The web app can be then accessed at ```http://localhost:9082```
* Api address: ```http://localhost:9081```

## Steps to Build the app
* Implement main requirements on the API with [Hapi.js](https://hapijs.com/)
* Implement corresponding main requirementso on client with [React](https://facebook.github.io/react/) and  [Redux](http://redux.js.org/).
* Build additional requirements (not required) such as authentication on both API and Client.
* Build a docker cluster with the following containers: server, client and mongodb.


## Decisions
* **Why two separate applications for server and client?**  

I chose to build separatly the front end and backend to have completly independent tiers and a more robust architecture.

* **Why React and not Angluar?** 

Although I didn't have much experience in Angular, I believe that learning it can in fact be a matter of days if we are confortable enough with JavaScript. However, to avoid any issues and bad practices, I chose to use a framework ecosystem (React & Redux) that I am much more confortable with.

* **Why Docker?**

Because I believe that Docker is Amazing. I chose to set up Docker manually because I already had experience with that. However, using a PaaS such as OpenShift (which is also Docker based) could have been easier if I was familiar with it.

## Assumptions

### Decting a login form
- The technique I used to detect a login form is very basic. I decided to detect a form in general due to the fact that login forms can be very different (some are handled by JavaScript directly, some are loaded dynamically, some have social login ...).

## :exclamation: MUST DO :exclamation:

* Both client and server should have ssl. (can be done through setting up nginx https proxies for both)..
