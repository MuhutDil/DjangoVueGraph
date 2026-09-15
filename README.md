# Django Vue GraphQL Blog

A full-stack blog application built with Django (backend), Vue.js (frontend), and GraphQL as the communication layer. This project demonstrates the integration of these technologies following a RealPython tutorial.

## Overview

An application where users can write posts. Posts can have many tags. The backend is implemented with Django, and the frontend is built with Vue.js, using GraphQL to communicate between them.

This is a training project based on an article from [RealPython](https://realpython.com/python-django-blog/).

## Project Structure

```
.
├── back_end/             # Django backend
│   ├── blog/            # Blog app with models and GraphQL schema
│   ├── back_end/        # Django project settings
│   ├── manage.py        # Django management script
│   └── requirements.txt # Python dependencies
├── front_end/           # Vue.js frontend
│   ├── src/
│   │   ├── components/  # Vue components
│   │   ├── views/       # Vue views/pages
│   │   ├── router/      # Vue Router configuration
│   │   ├── graphql/     # GraphQL queries
│   │   └── main.js      # Vue app entry point
│   ├── package.json     # Node.js dependencies
│   └── vite.config.js   # Vite configuration
└── README.md            # This file
```

## Features

### Backend (Django + GraphQL)
- Profile, Tag, and Post models
- GraphQL API with Graphene-Django
- CORS support for frontend communication
- Queries for retrieving posts, authors, and tags

### Frontend (Vue.js + Apollo Client)
- Vue 3 with Composition API
- Apollo Client for GraphQL queries
- Vue Router for navigation
- Views for:
  - All posts
  - Individual post details
  - Author pages
  - Tag-filtered posts

## Prerequisites

- Python 3.8+
- Node.js 16+
- npm or yarn

## Installation

### Backend Setup

1. Navigate to the backend directory:
   ```bash
   cd back_end/
   ```

2. Install dependencies:
   ```bash
   python -m pip install -r requirements.txt
   ```

3. Run migrations:
   ```bash
   python manage.py migrate
   ```

4. Start the development server:
   ```bash
   python manage.py runserver
   ```

The GraphQL API will be available at `http://localhost:8000/graphql/`

### Frontend Setup

1. Navigate to the frontend directory:
   ```bash
   cd front_end/
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Start the development server:
   ```bash
   npm run dev
   ```

The frontend will be available at `http://localhost:5173`

## Usage

1. Start both the backend and frontend servers
2. Open your browser and navigate to `http://localhost:5173`
3. Browse posts, view author pages, and filter by tags

## GraphQL API

The backend provides the following GraphQL queries:

- `posts`: Get all posts
- `post(id)`: Get a specific post by ID
- `authors`: Get all authors
- `author(id)`: Get a specific author by ID
- `tags`: Get all tags
- `tag(id)`: Get a specific tag by ID

## Technologies Used

### Backend
- Django 5.0.2
- Graphene-Django 3.2.0
- django-cors-headers 4.3.1

### Frontend
- Vue 3.4.21
- Vite 5.2.8
- Apollo Client 3.9.9
- Vue Router 4.3.0

## License

This project is created for educational purposes following a RealPython tutorial.
