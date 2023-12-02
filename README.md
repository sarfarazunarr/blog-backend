
# Blog Backend Endpoints

Welcome to the Blog Backend Endpoints project! This project provides a set of RESTful API endpoints to manage a blog system, allowing users to perform various operations like creating, updating, and deleting posts, as well as fetching posts based on different criteria such as category, titles, and author.

## Table of Contents

- [Features](#features)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [API Endpoints](#api-endpoints)
  - [Create a Post](#create-a-post)
  - [Update a Post](#update-a-post)
  - [Delete a Post](#delete-a-post)
  - [Get Posts by Category](#get-posts-by-category)
  - [Get Posts by Title](#get-posts-by-title)
  - [Get Posts by Author](#get-posts-by-author)
- [Contributing](#contributing)
- [License](#license)

## Features

- **Create Post:** Users can create new blog posts by providing necessary information such as title, content, category, and author.
- **Update Post:** Existing posts can be updated by making a request with the updated information.
- **Delete Post:** Users can delete a specific post based on its identifier.
- **Get Posts by Category:** Retrieve a list of posts based on their category.
- **Get Posts by Title:** Fetch posts matching a specific title.
- **Get Posts by Author:** Get posts authored by a specific user.

## Getting Started

### Prerequisites

Make sure you have the following installed:

- Node.js
- npm (Node Package Manager)

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/your-username/blog-backend.git
   ```

2. Navigate to the project directory:

   ```bash
   cd blog-backend
   ```

3. Install dependencies:

   ```bash
   npm install
   ```

4. Configure the database connection in `config.js` or environment variables.

5. Start the server:

   ```bash
   npm start
   ```

Now, your blog backend endpoints should be up and running!

## API Endpoints

### Create a Post

**Endpoint:** `POST /newpost`

**Request Body:**
```json
{
  "title": "Sample Post",
  "content": "This is the content of the sample post.",
  "category": "Technology",
  "author": "John Doe",
  "tags" : ["sample", "post"]
}
```

**Response:**
```json
{
 "message": "Post added successfully! Your Post Id is 12"
}
```

### Update a Post

**Endpoint:** `PUT /updatepost`

**Request Body:**
```json
{
  "title": "Updated Post",
  "content": "This is the updated content of the post.",
  "category": "Science",
  "author": "Jane Doe",
  "tags" : ["science", "post"]
}
```

**Response:**
```json
{
  "message": "Post updated successfully! Your Id is 12"
}
```

### Delete a Post

**Endpoint:** `DELETE /deletepost/:id`

**Response:**
```json
{
  "message": "Post deleted successfully! Your Post Id was 12"
}
```

### Get Posts by Category

**Endpoint:** `GET /posts-c/:category`

**Response:**
```json
[
  {
    "id": "123",
    "title": "Sample Post",
    "content": "This is the content of the sample post.",
    "author": "John Doe",
    "tags" : ["sample", "post"]
  }
]
```

### Get Posts by Title

**Endpoint:** `GET posts-title/:title`

**Response:**
```json
[
  {
    "id": "123",
    "title": "Sample Post",
    "content": "This is the content of the sample post.",
    "author": "John Doe",
    "tags" : ["sample", "post"]
  }
]
```

### Get Posts by Author

**Endpoint:** `GET /posts-author/:author`

**Response:**
```json
[
  {
    "id": "123",
    "title": "Sample Post",
    "content": "This is the content of the sample post.",
    "author": "John Doe",
    "tags" : ["sample", "post"]
  }
]
```

## Contributing

If you'd like to contribute to this project, please follow the [Contributing Guidelines](CONTRIBUTING.md).


Feel free to add or modify sections based on your project's specific requirements and structure.
