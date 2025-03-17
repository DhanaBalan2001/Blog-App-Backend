Backend
The backend is a RESTful API built with Node.js, Express, and MongoDB.

Features
User authentication and authorization
Post creation, editing, and deletion
Comment functionality with replies
Like/unlike posts and comments
Follow/unfollow users
Bookmark posts
Search functionality
Tag-based filtering
Tech Stack
Node.js - JavaScript runtime
Express.js - Web framework
MongoDB - Database
Mongoose - MongoDB object modeling
JWT - Authentication
API Endpoints
The API includes endpoints for:

User Management: Registration, login, profile management, follow/unfollow
Post Management: CRUD operations, likes, bookmarks, search, filtering
Comment Management: Adding, editing, deleting comments, replies
Getting Started
Clone the repository
Navigate to the server directory:
cd server

Install dependencies:
npm install

Create a .env file with the following variables:
PORT=5000
MONGODB=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret

Start the server:
npm start

The API documentation is available at /api/docs when the server is running.
