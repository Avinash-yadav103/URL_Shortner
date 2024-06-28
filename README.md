# URL Shortener Service

This URL Shortener service takes a valid URL and returns a shorter URL, redirecting the user to the original URL. It also keeps track of data such as the number of clicks made and the date and time of each click.

## Features

- **URL Shortening**: Generates a shorter URL for a given valid URL.
- **Redirection**: Redirects users from the shortened URL to the original URL.
- **Analytics**: Tracks the number of clicks and provides analytics data for each shortened URL.

## API Endpoints

### 1. Generate Short URL

**Endpoint**: `POST /url`

Generates a new short URL and returns the shortened URL in the format `example.com/random-id`.

**Request**:
```json
{
  "originalUrl": "https://example.com"
}
```

### 2. Redirect to Original URL

**Endpoint**: `GET /:id`

Redirects the user to the original URL corresponding to the given short ID.

**Example**:

This will redirect the user to the original URL associated with `abc123`.

### 3. Get URL Analytics

**Endpoint**: `GET /url/analytics/:id`

Returns the number of clicks and the date and time of each click for the provided short ID.

**Example**:
GET /url/analytics/abc123

**Response**:
```json
{
  "clicks": 42,
  "data": [
    {
      "date": "2024-01-01",
      "time": "12:34:56"
    },
    ...
  ]
}
```

# Technologies Used
Node.js: JavaScript runtime environment.
Express.js: Web framework for Node.js.
MongoDB: NoSQL database for storing URLs and analytics data.

# Contributing
Contributions are welcome! Please fork the repository and submit a pull request.




