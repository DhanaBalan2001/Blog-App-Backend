# Blog App - Backend

A robust backend API for a social media application that handles user authentication, posts, comments, likes, follows, and more.

## Features

- **User Authentication**: Secure registration and login system
- **User Profiles**: Create and manage user profiles with profile pictures
- **Post Management**: Create, read, update, and delete posts
- **Social Interactions**: Like posts, bookmark content, follow users
- **Comments System**: Comment on posts with nested replies
- **Search Functionality**: Search for posts and filter by tags
- **User Connections**: Follow/unfollow users, view followers and following

## Tech Stack

- **Node.js**: JavaScript runtime
- **Express.js**: Web application framework
- **MongoDB**: NoSQL database
- **JWT**: Authentication mechanism
- **Mongoose**: MongoDB object modeling

## API Documentation

API documentation is available at `/api/docs` endpoint when the server is running.

## Getting Started

### Prerequisites

- Node.js (v14 or higher)
- MongoDB (local or Atlas)
  
## Installation

1. Clone the repository
   ```bash
   git clone <repository-url>
   cd financial-management-backend
   ```

2. Install dependencies
   ```bash
   npm install
   ```

3. Create a `.env` file in the root directory with the following variables:
   ```
   PORT=5000
   MONGODB_URI=<your-mongodb-connection-string>
   JWT_SECRET=<your-jwt-secret>
   NODE_ENV=development
   ```

4. Start the server
   ```bash
   npm start
   ```

   For development with auto-restart:
   ```bash
   npm run dev
   ```

## API Endpoints

## User Management

- `POST /api/users/register` - Register a new user
- `POST /api/users/login` - Login a user
- `GET /api/users/me` - Get current user profile (requires authentication)
- `GET /api/users/:id` - Get user profile by ID
- `PUT /api/users/me` - Update user profile (requires authentication)
- `POST /api/users/profile-picture` - Update profile picture URL (requires authentication)
- `PUT /api/users/follow/:id` - Follow a user (requires authentication)
- `PUT /api/users/unfollow/:id` - Unfollow a user (requires authentication)
- `GET /api/users/:id/followers` - Get user followers
- `GET /api/users/:id/following` - Get users that a user is following

## Post Management

- `POST /api/posts` - Create a new post (requires authentication)
- `PUT /api/posts/posts/:id` - Update a post (requires authentication)
- `DELETE /api/posts/posts/:id` - Delete a post (requires authentication)
- `GET /api/posts` - Get all posts
- `GET /api/posts/user/:userId` - Get posts by user
- `GET /api/posts/search` - Search posts
- `GET /api/posts/:id` - Get post by ID
- `PUT /api/posts/like/:id` - Like/unlike a post (requires authentication)
- `PUT /api/posts/bookmark/:id` - Bookmark/unbookmark a post (requires authentication)
- `GET /api/posts/tag/:tag` - Get posts by tag
  
## Comment Management

- `POST /api/comments/:postId` - Add comment to post (requires authentication)
- `GET /api/comments/:postId` - Get comments for a post
- `DELETE /api/comments/:id` - Delete a comment (requires authentication)
- `PUT /api/comments/:id` - Edit a comment (requires authentication)
- `PUT /api/comments/like/:id` - Like/unlike a comment (requires authentication)
- `POST /api/comments/reply/:id` - Add reply to a comment (requires authentication)
- `GET /api/comments/replies/:id` - Get replies for a comment
  
## System

- `GET /health` - Health check endpoint
- `GET /api/docs` - API documentation

## Deployment

The backend is deployed on Render:
https://blog-app-backend-u840.onrender.com

## License

This project is licensed under the MIT License.
