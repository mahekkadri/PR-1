::: {align="center"}
# 🎬 Movie Management API

### A simple REST API built with **Node.js · Express.js · MongoDB · Mongoose**

```{=html}
<p>
```
`<img src="https://img.shields.io/badge/Node.js-18%2B-339933?style=for-the-badge&logo=node.js&logoColor=white" alt="Node.js">`{=html}
`<img src="https://img.shields.io/badge/Express.js-5.x-000000?style=for-the-badge&logo=express&logoColor=white" alt="Express.js">`{=html}
`<img src="https://img.shields.io/badge/MongoDB-Database-47A248?style=for-the-badge&logo=mongodb&logoColor=white" alt="MongoDB">`{=html}
`<img src="https://img.shields.io/badge/Mongoose-ODM-880000?style=for-the-badge" alt="Mongoose">`{=html}
```{=html}
</p>
```
**Create · Read · Update · Delete your movie collection**
:::

------------------------------------------------------------------------

## 🍿 About the Project

Movie Management API is a beginner-friendly backend project that lets
you manage movie records using REST API endpoints. It is built with
**Express.js** and stores movie data in a local **MongoDB** database
through **Mongoose**.

Each movie contains: - 🎞️ **Title** --- movie name - 🏷️ **Genre** ---
movie category - 🎥 **Director** --- director's name

The API supports adding movies, viewing all movies, finding a specific
movie, updating a movie, and deleting a movie.

## ✨ Features

  Feature                Endpoint         Method
  ---------------------- ---------------- ----------
  Home / API check       `/`              `GET`
  Add a movie            `/addmovie`      `POST`
  Get all movies         `/getmovies`     `GET`
  Get a specific movie   `/getmovie`      `GET`
  Update a movie         `/updatemovie`   `PUT`
  Delete a movie         `/deletemovie`   `DELETE`

## 🧰 Tech Stack

-   **Node.js** --- JavaScript runtime
-   **Express.js** --- API and server framework
-   **MongoDB** --- NoSQL database
-   **Mongoose** --- MongoDB object modeling
-   **Postman** --- API testing

## 📁 Project Structure

``` text
PR-1/
│
├── images/
│   ├── add data.png
│   ├── delete data.png
│   ├── get all data.png
│   ├── get specific data.png
│   └── update data.png
│
├── node_modules/
├── app.js
├── package.json
├── package-lock.json
└── README.md
```

## ⚙️ Getting Started

### 1. Clone the project

``` bash
git clone YOUR_GITHUB_REPOSITORY_URL
```

### 2. Open the project folder

``` bash
cd PR-1
```

### 3. Install dependencies

``` bash
npm install
```

If Express or Mongoose is not already listed in your dependencies,
install them:

``` bash
npm install express mongoose
```

### 4. Start MongoDB

Make sure your local MongoDB server is running. This project connects
to:

``` text
mongodb://127.0.0.1:27017/moviesDB
```

The database `moviesDB` and its collection are created by
MongoDB/Mongoose when data is first saved.

### 5. Run the server

``` bash
node app.js
```

The API runs at:

``` text
http://localhost:3000
```

When the database connection succeeds, the terminal should show:

``` text
MongoDB Connected
```

## 🚀 API Usage --- Test with Postman

Base URL:

``` text
http://localhost:3000
```

### 1. 🏠 Home

**GET** `/`

Returns a simple API welcome response.

### 2. ➕ Add a Movie

**POST** `/addmovie`

In Postman, choose **Body → raw → JSON** and send:

``` json
{
  "title": "3 Idiots",
  "genre": "Comedy Drama",
  "director": "Rajkumar Hirani"
}
```

```{=html}
<details>
```
```{=html}
<summary>
```
📸 View Add Movie screenshot
```{=html}
</summary>
```
![Add Movie](images/add%20data.png)

```{=html}
</details>
```
### 3. 📚 Get All Movies

**GET** `/getmovies`

Returns all movie documents stored in the database.

```{=html}
<details>
```
```{=html}
<summary>
```
📸 View Get All Movies screenshot
```{=html}
</summary>
```
![Get All Movies](images/get%20all%20data.png)

```{=html}
</details>
```
### 4. 🔎 Get a Specific Movie

**GET** `/getmovie`

The current `app.js` implementation reads the search criteria from
`req.body`. To match the current code, send a JSON body such as:

``` json
{
  "title": "3 Idiots"
}
```

> Note: GET requests with a body are not consistently supported by all
> clients and servers. A more conventional approach is to use query
> parameters (for example, `/getmovie?title=3%20Idiots`) and read
> `req.query` in the route.

```{=html}
<details>
```
```{=html}
<summary>
```
📸 View Get Specific Movie screenshot
```{=html}
</summary>
```
![Get Specific Movie](images/get%20specific%20data.png)

```{=html}
</details>
```
### 5. ✏️ Update a Movie

**PUT** `/updatemovie`

Send the movie's MongoDB `_id` and the new values:

``` json
{
  "id": "PASTE_MONGODB_MOVIE_ID",
  "newData": {
    "title": "3 Idiots",
    "genre": "Comedy",
    "director": "Rajkumar Hirani"
  }
}
```

Replace `PASTE_MONGODB_MOVIE_ID` with the actual `_id` returned when you
add or fetch a movie.

```{=html}
<details>
```
```{=html}
<summary>
```
📸 View Update Movie screenshot
```{=html}
</summary>
```
![Update Movie](images/update%20data.png)

```{=html}
</details>
```
### 6. 🗑️ Delete a Movie

**DELETE** `/deletemovie`

Send the movie's MongoDB `_id`:

``` json
{
  "id": "PASTE_MONGODB_MOVIE_ID"
}
```

```{=html}
<details>
```
```{=html}
<summary>
```
📸 View Delete Movie screenshot
```{=html}
</summary>
```
![Delete Movie](images/delete%20data.png)

```{=html}
</details>
```
## 🎥 Project Demo Video

▶️ **Watch the project demo:** [Add your YouTube video link
here](https://www.youtube.com/)

> Replace the link above with your own uploaded project-demo video URL.

## 🧪 Testing

You can test every endpoint using **Postman**: 1. Start MongoDB. 2. Run
`node app.js`. 3. Open Postman. 4. Select the required HTTP method. 5.
Enter the endpoint URL. 6. For POST, PUT, and DELETE, choose **Body →
raw → JSON** and enter the sample data. 7. Click **Send** and check the
response.

## 💡 What I Learned

-   Creating a server with Express.js
-   Connecting Node.js to MongoDB using Mongoose
-   Creating schemas and models
-   Performing CRUD operations
-   Sending and receiving JSON data
-   Testing REST APIs with Postman

## 🔮 Future Improvements

-   Add input validation and proper error handling
-   Use query parameters or route parameters for searching a movie
-   Return the updated document after an update
-   Add unique IDs, pagination, and search filters
-   Add environment variables for database configuration

## 👩‍💻 Developer

**Made with 💚 and lots of learning.**

*Movie Management API --- my hands-on practice project with Node.js,
Express.js and MongoDB.*

------------------------------------------------------------------------

::: {align="center"}
### ⭐ If you like this project, give the repository a star!

**Thanks for visiting! Happy coding. 🚀**
:::
