# VueTube RESTful API - YouTube Clone

> VueTube is a YouTube clone built with nodejs, expressjs & mongodb.

## Features

> CRUD (Create, Read, Update And Delete)

- Authentication with JWT (Reset Password with email)
  - Login (User/Admin)
  - Register
  - Forgot Password
- Pagination and search where necessary
- API Security (NoSQL Injections, XSS Attacks, http param pollution etc)
- Video (CRUD)
  - Upload video
  - Upload video thumbnail
  - Watch video
  - Increase Views
  - Like and dislike video
  - Download video
  - Comment & reply for video
  - Update video details
  - Delete video
- Subscribe to a channel
- View liked videos
- Trending
- Subscriptions
- History (CRUD)
  - Watch history
  - Search history
- Settings
  - Modify channel name and email
  - Change password
  - Upload channel avatar

## Frontend Repo

Frontend was developed with vue js and vuetify 

## API Documentation

Hosted on netlify: [Coming Soon]()

Extensive and testing documentation with postman: 

## Database Model

Though the diagram uses sql data type, this diagram is to show you the various collections in the mongo database.

![Screenshot](screenshots/vue_tube_ERD.jpg)

## Requirement

- NodeJS
- MongoDB

## Configuration File

Rename the config/.env.example to .env, then modify to your environment variables, mongodb uri, set your JWT_SECRET and SMTP variables

```ENV
NODE_ENV=development
PORT=3001

MONGO_URI=YOUR_URL

JWT_SECRET=YOUR_SECRET
JWT_EXPIRE=30d
JWT_COOKIE_EXPIRE=30

FILE_UPLOAD_PATH = ./public/uploads
MAX_FILE_UPLOAD = 1000000

SMTP_HOST=smtp.mailtrap.io
SMTP_PORT=2525
SMTP_EMAIL=
SMTP_PASSWORD=
FROM_EMAIL=noreply@quizapp.com
FROM_NAME=QuizzApp
```

Email testing: use mailtrap for email testing, it's easy no stress.

## Installation

Install all npm dependecies

```console
npm install
```

Install nodemon globally

```console
npm install -g nodemon
```

### Note

Make sure you run the seeder to get categories in your database or Create a user with the role admin, then add category with the category endpoint.

Run database seeder

- Seeder folder is \_data/
- Edit the seeder file if you want to

```console
node seeder -i
```

Delete all data

```console
node seeder -d
```

## Start web server

```console
node run dev
```

## License

This project is licensed under the MIT License

## Developed by Satyam Kumar
