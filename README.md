::: {align="center"}
# 🎬 Movie Management API

### A REST API to manage your movie collection

Built with **Node.js · Express.js · MongoDB · Mongoose**

```{=html}
<p>
```
`<img src="https://img.shields.io/badge/Node.js-18%2B-339933?style=for-the-badge&logo=node.js&logoColor=white" alt="Node.js">`{=html}
`<img src="https://img.shields.io/badge/Express.js-5.x-000000?style=for-the-badge&logo=express&logoColor=white" alt="Express.js">`{=html}
`<img src="https://img.shields.io/badge/MongoDB-Database-47A248?style=for-the-badge&logo=mongodb&logoColor=white" alt="MongoDB">`{=html}
`<img src="https://img.shields.io/badge/Mongoose-ODM-880000?style=for-the-badge" alt="Mongoose">`{=html}
`<img src="https://img.shields.io/badge/Postman-API_Testing-FF6C37?style=for-the-badge&logo=postman&logoColor=white" alt="Postman">`{=html}
```{=html}
</p>
```
**Create · Read · Update · Delete**
:::🍿 About the Project
Movie Management API is a beginner-friendly backend project built to
manage movie records through REST API endpoints. The application uses
Express.js to handle requests and MongoDB with Mongoose to
store movie data.

Each movie record contains:

  Field         Description
  🎞️ Title      Name of the movie
🏷️ Genre      Movie category
🎥 Director   Director's name

With this API, you can add new movies, view all movies, search for a
specific movie, update movie details, and delete a movie.
✨ Features
  Feature                   Endpoint         Method
  🏠 Home / API check       /              GET
➕ Add a movie            /addmovie      POST
📚 Get all movies         /getmovies     GET
🔎 Get a specific movie   /getmovie      GET
✏️ Update a movie         /updatemovie   PUT
🗑️ Delete a movie         /deletemovie   DELETE
🧰 Tech Stack
- Node.js --- JavaScript runtime
- Express.js --- Backend and API framework
- MongoDB --- NoSQL database
- Mongoose --- MongoDB object modeling
- Postman --- API testing
📁 Project Structure
PR-1/
│
├── images/
│   ├── add data.png
│   ├── delete data.png
│   ├── get all data.png
│   ├── get specific data.png
│   └── update data.png
│
├── app.js
├── package.json
├── package-lock.json
└── README.md
⚙️ Getting Started
1. Clone the repository
git clone YOUR_GITHUB_REPOSITORY_URL
2. Move into the project folder
cd PR-1
3. Install dependencies
npm install
4. Start MongoDB
Make sure your local MongoDB server is running. The application connects
to:
mongodb://127.0.0.1:27017/moviesDB
MongoDB/Mongoose creates the database and collection when the first
movie record is saved.
5. Run the application
node app.js
The API will be available at:
http://localhost:3000
When the database connection is successful, the terminal displays:
MongoDB Connected
🚀 API Documentation
Base URL: http://localhost:3000

All endpoints can be tested using Postman.
1. 🏠 Home
GET /

Checks whether the API server is running.
2. ➕ Add a Movie
POST /addmovie

In Postman, select Body → raw → JSON and send:
{
  "title": "3 Idiots",
  "genre": "Comedy Drama",
  "director": "Rajkumar Hirani"
}
<details>
<summary>
<b>{=html}📸 View Add Movie Screenshot`</b>`{=html}
</summary>
<br>{=html}

</details>
3. 📚 Get All Movies
GET /getmovies

Returns all movie records stored in the MongoDB database.
<details>
<summary>
<b>{=html}📸 View Get All Movies Screenshot`</b>`{=html}
</summary>
<br>{=html}

</details>
4. 🔎 Get a Specific Movie
GET /getmovie

The current app.js implementation reads the search criteria from
req.body. To match the current code, send a JSON body such as:
{
  "title": "3 Idiots"
}
Note: GET requests with a body are not consistently supported by
all clients and servers. A conventional alternative is to use a query
parameter, such as /getmovie?title=3%20Idiots, and read it using
req.query in the route.

<details>
<summary>
<b>{=html}📸 View Get Specific Movie Screenshot`</b>`{=html}
</summary>
<br>{=html}

</details>
5. ✏️ Update a Movie
PUT /updatemovie

Send the movie's MongoDB _id and the updated values:
{
  "id": "PASTE_MONGODB_MOVIE_ID",
  "newData": {
    "title": "3 Idiots",
    "genre": "Comedy",
    "director": "Rajkumar Hirani"
  }
}
Replace PASTE_MONGODB_MOVIE_ID with the actual _id of the movie.
<details>
<summary>
<b>{=html}📸 View Update Movie Screenshot`</b>`{=html}
</summary>
<br>{=html}

</details>
6. 🗑️ Delete a Movie
DELETE /deletemovie

Send the movie's MongoDB _id:
{
  "id": "PASTE_MONGODB_MOVIE_ID"
}
<details>
<summary>
<b>{=html}📸 View Delete Movie Screenshot`</b>`{=html}
</summary>
<br>{=html}

</details>
🎥 Project Demo Video
::: {align="center"}

### ▶️ Watch my project video link
("https://drive.google.com/drive/folders/1n_no5yyzs-z_Mi8t-ObRKainylmjdsw9?usp=sharing")

**Click the button above to watch the complete project demonstration.**
:::🧪 Testing with Postman
Follow these steps to test the API:
1. Start your MongoDB server.
2. Run the application using node app.js.
3. Open Postman.
4. Select the required HTTP method.
5. Enter the endpoint URL.
6. For POST, PUT, and DELETE requests, select Body → raw → JSON and
   enter the required data.
7. Click Send to view the response.
💡 What I Learned
- Creating a backend server using Express.js
- Connecting Node.js with MongoDB using Mongoose
- Creating schemas and models
- Performing CRUD operations
- Handling JSON request data
- Testing REST API endpoints using Postman
🔮 Future Improvements
- Add input validation and better error handling
- Improve movie search using query or route parameters
- Add pagination and search filters
- Use environment variables for database configuration
👩‍💻 Developer
Made with 💚 and lots of learning.

Movie Management API --- a hands-on backend project using Node.js,
Express.js, MongoDB, and Mongoose.
::: {align="center"}
### ⭐ If you like this project, give the repository a star!

**Thanks for visiting! Happy coding. 🚀**
:::
