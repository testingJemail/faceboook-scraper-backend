# Facebook-scraper-nodejs

![facebook scraper demo](imgs/template.gif)

This is a tool that uses browser automation to scrape data from facebook. This one in particular is made for scraping data from groups and pages that exist on facebook. Happy Scraping People

# Pre-requisites

- Install [Node.js](https://nodejs.org/en/) version 8.0.0 or up

# Getting started

- Clone the repository

```
git clone repo
```

- Install dependencies

```
cd <project_name>
npm install
create a credentials.txt file with the first line your email and second line your password
```

- Specify Targets

```
Add the http link of the groups you want scraped on target.txt. Each line holding a new link for a group. **make sure to use mobile version of facebook links**.
For example: https://m.facebook.com/cnn
```

- Build and run the scraper

```
node creadteDb.js
```

- Build and run the sever

```
node index.js
```

Navigate to `http://localhost:3551`

## API Document endpoints

Functional APIs that can be used:

| Functionaity                                   | APIs                                                                                |
| ---------------------------------------------- | ----------------------------------------------------------------------------------- |
| **GET-- all the scraped data**                 | http://localhost:3551/api/pages/:full                                               |
| **GET-- Search By The name of Group**          | http://localhost:3551/api/pages/:groupName                                          |
| **GET-- Single Comment from a specific group** | http://localhost:3551/api/pages/comment/:document_id/:group_id/:post_id/:comment_id |
| **GET-- Single Post from a specific group**    | http://localhost:3551/api/pages/post/:document_id/:group_id/:post_id                |
| **GET-- Single Group from a all groups**       | http://localhost:3551/api/pages/group/:document_id/:group_id                        |
| **GET-- All Posts from a specific group**      | http://localhost:3551/api/pages/posts/:document_id/:group_id                        |
| **GET-- All Comment from a specific post**     | http://localhost:3551/api/pages/comment/:document_id/:group_id/:post_id/            |
| **GET-- All posts that contain search Item**   | http://localhost:3551/api/pages/search/:searchItem                                  |
| **GET-- All dates of all scraped dates**       | http://localhost:3551/api/pages/dates                                               |
| **GET-- All keywords for sentiment analysis**  | http://localhost:3551/api/keyword                                                   |
| **POST-- Add keywords for sentiment analysis** | http://localhost:3551/api/keyword                                                   |
| **Get-- All sentiment for a post**             | http://localhost:3551/api/sentiement                                                |

## Project Structure

The folder structure of this app is explained below:

| Name                 | Description                                                            |
| -------------------- | ---------------------------------------------------------------------- |
| **node_modules**     | Contains all npm dependencies                                          |
| **src**              | Contains source code that will be compiled to the dist dir             |
| **src/index.js**     | Scraper starter for the given groups and pages                         |
| **src/core-scraper** | Controllers define functions to serve various express routes.          |
| **src/lib**          | Common libraries to be used across your app.                           |
| **src/middlewares**  | middlewares that inhance functionallity                                |
| **src/routes**       | Contain all express routes, separated by module/area of application    |
| **src/models**       | Models define schemas that will be used in storing and retrieving data |
| **src/db**           | Contains all the get query info from db                                |
| **src/index.js**     | Entry point to the express server                                      |
| **package.json**     | Contains npm dependencies as well as [build scripts]                   |
