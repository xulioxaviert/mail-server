# Email Server

This project consists of a backend server developed with Node.js and Express that provides a service for sending emails using Gmail as the SMTP provider.

## Description

The system allows sending customized emails using HTML templates and Handlebars for dynamic data substitution. It is primarily designed to send purchase confirmations with details of acquired products.

## Prerequisites

- Node.js (recommended version: 14.x or higher)
- npm (Node.js package manager)
- Gmail account for sending emails

## Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd mail-server
```

2. Install the dependencies:
```bash
npm install
```

3. Set up environment variables:
Create a `.env` file in the root directory and add the following variables:
```
GMAIL_USER=<your-gmail-address>
GMAIL_PASS=<your-gmail-password>
```

## Usage

1. Start the server:
```bash
npm start
```

2. Send a POST request to `/send-email` with the following JSON payload:
```json
{
  "to": "recipient@example.com",
  "subject": "Your Subject",
  "template": "template-name",
  "context": {
    "key": "value"
  }
}
```

## Project Structure

- `server.js`: Entry point of the application.
- `routes/`: Contains the route definitions.
- `controllers/`: Contains the logic for handling requests.
- `services/`: Contains the email sending logic.
- `templates/`: Contains the HTML email templates.

## Dependencies

- `express`: Web framework for Node.js.
- `nodemailer`: Module for sending emails.
- `handlebars`: Templating engine for dynamic content.
- `dotenv`: Module for loading environment variables.

## Contributing

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes.
4. Commit your changes (`git commit -am 'Add new feature'`).
5. Push to the branch (`git push origin feature-branch`).
6. Create a new Pull Request.

## License

This project is licensed under the MIT License.