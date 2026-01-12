# Members Only

A full-stack web application that creates an exclusive clubhouse experience. Users can sign up and log in, but only members who know the secret passcode can fully participate by creating messages and seeing who wrote what.

This project is part of The Odin Project curriculum, demonstrating authentication, session management, and database interactions using Node.js and PostgreSQL.

## Features

- **User Authentication**: Secure Sign Up, Login, and Logout functionality.
- **Membership Level**: Users can upgrade their status to "Member" by solving a riddle or entering a secret passcode.
- **Anonymous vs. Member Views**: 
  - **Guests/Non-Members**: Can only view messages but not the authors or creation dates. Use the site anonymously.
  - **Members**: Can create new messages and see full details (author and timestamp) of all posts.
- **Message Board**: A shared space for members to post thoughts and messages.

## Tech Stack

- **Backend**: Node.js, Express.js
- **Database**: PostgreSQL
- **Templating**: EJS (Embedded JavaScript)
- **Authentication**: Passport.js (Local Strategy), Express Session
- **Styling**: Review custom CSS/Styles in `public/`
- **Environment Management**: dotenv

## Prerequisites

Before you begin, ensure you have met the following requirements:
- **Node.js**: Installed on your machine.
- **PostgreSQL**: Installed and running locally.

## Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/Mridul-Dev123/Members-Only.git
cd Members-Only
```

### 2. Install Dependencies

```bash
npm install
```

### 3. Configure Environment Variables

Create a `.env` file in the root directory and add your PostgreSQL database credentials:

```env
PG_HOST=localhost
PG_USER=your_postgres_username
PG_DATABASE=your_database_name
PG_PASSWORD=your_postgres_password
PG_PORT=5432
```

> **Note**: Make sure to create the database mentioned in `PG_DATABASE` in your PostgreSQL instance before running the app.

### 4. Database Setup

Populate the database with the initial schema and data:

```bash
npm run populate
```

### 5. Run the Application

Start the development server:

```bash
npm run dev
```

The application will be available at [http://localhost:3000](http://localhost:3000).

## Usage

1.  **Sign Up**: Create a new account.
2.  **Join the Club**: Navigate to the "Join Club" page and enter the secret passcode to become a member.
    - *Hint: Check the source code or controller logic if you don't know the secret!*
3.  **Post Messages**: Once you are a member, you can create new messages on the board.

## Logic & Structure

- **`app.js` / `index.js`**: Application entry point and server configuration.
- **`routes/`**: Defines the application routing logic (`user.router.js`, `message.router.js`).
- **`controllers/`**: Handles the business logic for users and messages.
- **`views/`**: Contains EJS templates for the frontend UI.
- **`middleware/`**: Custom middleware for authentication checks (`authenticated.middleware.js`, `passport.config.js`).

## License

This project is licensed under the ISC License.
