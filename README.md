This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## [Live Demo of Tinder clone app](https://tinder-clone-69e7a.web.app/)

## Process of developing intro

**Build a Tinder Clone with MERN Stack (MongoDB, Express, React, Node JS)**

- Back-End:
  - Database: MongoDB
  - Back-end JS framework: NodeJS
  - Server side: Express JS
  - Connect to MongoDB use Mongooes
- Front-End:
- `npx create-react-app tinder-clone`
- add project in firebase "tinder-clone"
- `cd tinder-clone`, then `npm start`
- del 'App.test.js', 'logo.svg', 'setupTests.js'
- Go to **material-ui**
- open new terminal install `npm install @material-ui/core` and `npm install @material-ui/icons`
- search person icon and import it in header
- `npm i react-tinder-card` after created TinderCards.js
- create Express server which connect to MongoDB, pull all data from there.
- create 'tinder-backend' in the same folder level as 'tinder-clone'
- `cd tinder-backend` then `npm init`
- 'server.js' for entry point
- in created 'package.json' backend stuff like import is ES6, to get that in node.js under "main:" add `"type": "module",`
- under "test:" add `"start": "node server.js"` then create `server.js`
- install all dependencies, `npm i express mongooes` or `npm install express mongoose`
- go to MongoDB, build a new project
- terminal `cd tinder-backend` then `npm i -g nodemon`
- `nodemon server.js`, then go to `localhost:8001`, now you have API endpoint, then connect to DB
  - Back to MongoDB -> DB Access -> Add new DB user -> create user name and pw (save yourself) -> Add User
  - Network Access -> Add IP Address to allow list -> Allow access from anywhere -> confirm
  - go Clusters -> CONNECT -> Connect your application -> you get url to connect to DB -> fill "\<pw>" and "\<db>" name
  - Create database schema -> "dbCards.js"
  - add Middlewares in `server.js`
  - `npm i cors` cors is adding headers to every request, a security prerequisite when you have things deployed online
  - added cors and `nodemon server.js` again
  - open [postman](https://www.postman.com/) (interact with servers backend stuff) in local to check our API if they are working correctly - get new "+" tab, and type the `http://localhost:8001/` and `http://localhost:8001/tinder/cards` - post `http://localhost:8001/tinder/cards` -> body -> raw -> JSON - add below:

```
    [
    {
    "name": "Elon Musk",
    "imgUrl":
    "https://www.biography.com/.image/t_share/MTY2MzU3Nzk2OTM2MjMwNTkx/elon_musk_royal_society.jpg"
    },
    {
    "name": "Jeff Bezoz",
    "imgUrl":
    "https://www.biography.com/.image/t_share/MTY2NzA3ODE3OTgwMzcyMjYw/jeff-bezos-andrew-harrer_bloomberg-via-getty-images.jpg"
    }
    ]

```

```
    [
    {
    "name": "Elizabeth Olsen",
    "imgUrl":
    "https://www.gstatic.com/tv/thumb/persons/620481/620481_v9_bb.jpg"
    },
    {
    "name": "Scarlett Johansson",
    "imgUrl":
    "https://pm1.narvii.com/6310/c0e449205abaa82b4c37b3baf0e77ab95fe13137_00.jpg"
    },
    {
    "name": "Gal Gadot",
    "imgUrl":
    "https://upload.wikimedia.org/wikipedia/commons/5/5b/Gal_Gadot_cropped_lighting_corrected_2b.jpg"
    }
    ]
```



## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.<br />
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.


