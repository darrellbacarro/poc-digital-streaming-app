<center><img src="https://res.cloudinary.com/dlevukpcc/image/upload/v1668517160/POC%20Screenshots/logo_bxzzzc.png" width="120" /></center>
<h1 align=center>Digital Streaming System</h1>

> "Without the Streaming"

![System Screenshot](https://res.cloudinary.com/dlevukpcc/image/upload/v1668514175/POC%20Screenshots/Screenshot_2022-11-15_at_8.09.23_PM_ps3lnw.png)

This lets guests and regular users to browse and search for their favorite movies and actors. The system also has the content management functionality available to administrators.

This system is developed mainly with the following libraries and database:

* [**React**](https://reactjs.org) - A JavaScript library for building user interfaces.
* [**Loopback 4**](https://loopback.io/doc/en/lb4/) - LoopBack is an award-winning, highly extensible, open-source Node.js and TypeScript framework based on Express. It enables you to quickly create APIs and microservices composed from backend systems such as databases and SOAP or REST services.
* [**MongoDB**](https://www.mongodb.com) - MongoDB is a source-available cross-platform document-oriented database program.

## Setup
---
Clone the repo with the following command:

```bash
git clone --recurse-submodules -j8 https://github.com/darrellbacarro/poc-digital-streaming-app.git
```
> `-j8` is an optional performance optimization that became available in version 2.8, and fetches up to 8 submodules at a time in parallel

### Backend
---

1. Make sure the `poc-digital-streaming-be` folder is updated and checked out at the `main` branch.
2. Install the dependencies: `yarn` or `npm install`
3. Create a `.env` file in the project root folder if not existing. The file should contain the following environment variables:
> * `MONGODB_HOST`

Firebase Environment Variables

> * `CLIENT_EMAIL`
> * `PRIVATE_KEY`
> * `PROJECT_ID`
4. Run the app using `yarn start` or `npm start`.

### Frontend
---
1. Make sure the `poc-digital-streaming-fe` folder is updated and checked out at the `main` branch.
2. Install the dependencies: `yarn` or `npm install`
3. Create a `.env` file in the project root folder if not existing. Specify the host and port of the backend API in the `REACT_APP_API_URL` environment variable.
4. Run the app using `yarn start` or `npm start`.

**Note:**

> The repo comes with a `Dockerfile` that may be used to deploy the app in a docker container. Use the following command to do so:

```bash
docker run -it $(docker build -q .)
```

## Features
---

* **Browse & Search**. Search any movie titles and actor names. The system will any movie or actor that matches the search keyword or phrase.

![Browse & Search](https://res.cloudinary.com/dlevukpcc/image/upload/v1668516509/POC%20Screenshots/Screenshot_2022-11-15_at_8.48.16_PM_toexxj.png)

* **Favorites & Reviews**. Registered users may save any movie to their favorites list. They may also write movie reviews and view ratings.

![Favorites & Reviews](https://res.cloudinary.com/dlevukpcc/image/upload/v1668517000/POC%20Screenshots/Screenshot_2022-11-15_at_8.55.57_PM_ke8hmk.png)

* **Content Management**. Administrators have the ability to manage the contents of the public website. Manage users, reviews, movies, actors and genres.

![Content Management](https://res.cloudinary.com/dlevukpcc/image/upload/v1668517134/POC%20Screenshots/Screenshot_2022-11-15_at_8.57.55_PM_mxpmsd.png)

## Test Coverage (>= 60%)
---

### Frontend
Frontend tests are written with `@testing-library/react` and `jest`. The following shows the results from the SonarQube scan:

![fe-sonar](https://res.cloudinary.com/dlevukpcc/image/upload/v1668517947/POC%20Screenshots/Screenshot_2022-11-15_at_9.12.12_PM_qhshli.png)

### Backend
Backend tests are written with `@loopback/testlab` with `sinon` and `mocha` integrated. The following show the results from the SonarQube scan:

![be-sonar](https://res.cloudinary.com/dlevukpcc/image/upload/v1668517979/POC%20Screenshots/Screenshot_2022-11-15_at_9.12.53_PM_bzeymd.png)

---