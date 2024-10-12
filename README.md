# URL Shortener Microservice

This is a full-stack JavaScript URL shortener application that allows users to shorten long URLs and redirect to the original URL using the shortened version. It's built with Node.js, Express.js, and MongoDB.

**This project was inspired by the "URL Shortener Microservice" challenge on freeCodeCamp.**

## Features

*   **Shorten URLs:**
    *   Takes a long URL as input and generates a unique short code.
    *   Stores the original URL and short code in a database.
    *   Returns a JSON response with the original URL and the shortened URL.
*   **Redirect to Original URL:**
    *   Redirects users to the original URL when they visit the shortened URL.

## API Endpoints

*   **POST /api/shorturl:** Shorten a URL.
    *   Request body: `{ url: "your_long_url" }`
    *   Response: `{ original_url: "your_long_url", short_url: "short_code" }`
*   **GET /api/shorturl/:short_code:** Redirect to the original URL.
    *   Redirects the user to the original URL associated with the `short_code`.
*   **GET /api/shorturl?short_url=:short_code:** (Alternative to the above)
    *   Redirects the user to the original URL associated with the `short_code` passed as a query parameter.

## Project Structure

*   `index.js`: Main server file.
*   `public/`: Static files (HTML, CSS, JavaScript for the frontend).
*   `views/`: HTML templates.
*   `.env`: Environment variables (MongoDB connection string, etc.).

## Installation and Setup

1.  Clone the repository: `git clone <repository_url>`
2.  Install dependencies: `npm install`
3.  Create a `.env` file and add your MongoDB connection string as `MONGO_URI`.
4.  Start the server: `npm start`

## Usage

1.  Access the app in your web browser.
2.  Use the provided form to submit a long URL.
3.  The shortened URL will be displayed.
4.  You can also enter a short code in the second form to retrieve and redirect to the original URL.

## Example Usage

**Shorten a URL:**
POST /api/shorturl
**Redirect to the original URL:**
GET /api/shorturl/short_code
or

GET /api/shorturl?short_url=short_code


## Technologies Used

*   Node.js
*   Express.js
*   MongoDB
*   Mongoose
*   HTML
*   CSS
*   JavaScript

## Contributing

Contributions are welcome! Feel free to open issues or pull requests.
