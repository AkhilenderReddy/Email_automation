# Email Processing Automation

This project is an automated email processing system designed to streamline and enhance email management. The system integrates with Gmail to fetch unread emails, categorizes them using the Groq SDK with LLM (Llama), generates automated replies, and sends responses via Nodemailer. The purpose of this project is to reduce the manual effort required in handling emails by providing a robust, efficient, and reliable solution for email automation. By automating email responses, it ensures timely replies, improves productivity, and enhances communication efficiency.

## Requirements

- Node.js (version 14.x or later)
- npm (version 6.x or later)
- Google API credentials (CLIENT_ID, CLIENT_SECRET, REFRESH_TOKEN)
- Groq SDK API key
- A Gmail account for testing

## Installation

1. **Clone the Repository**

   ```sh
   git clone https://github.com/AkhilenderReddy/Email_Automation.git
   cd Email_Automation

2. **Install Dependencies**

   Install the project dependencies using npm:

   ```sh
   npm install googleapis nodemailer axios express body-parser groq-sdk dotenv
   ```

   This command installs the necessary Node.js packages:

   - `googleapis`: Official Node.js client library for Google APIs (including Gmail API).
   - `nodemailer`: Module for sending emails using Node.js.
   - `axios`: Promise-based HTTP client for making HTTP requests.
   - `express`: Web framework for Node.js used to create the API server.
   - `body-parser`: Middleware to parse incoming request bodies in Express.
   - `groq-sdk`: SDK for using Groq API, including LLM (Llama), for natural language processing.
   - `dotenv`: Module to load environment variables from a `.env` file into `process.env`.

## Setup

1. **Create a `.env` File**

   Create a `.env` file in the root directory of your project and add the following environment variables:

   ```sh
   CLIENT_ID=your-google-client-id
   CLIENT_SECRET=your-google-client-secret
   REDIRECT_URI=https://developers.google.com/oauthplayground
   REFRESH_TOKEN=your-google-refresh-token
   apiKey=your-groq-api-key
   PORT=3000
   ```

   Replace `your-google-client-id`, `your-google-client-secret`, `your-google-refresh-token`, and `your-groq-api-key` with your actual credentials and API key obtained from Google and Groq SDK.

2. **Configure Google API Credentials**

   Follow [Google's guide](https://developers.google.com/gmail/api/quickstart/nodejs) to obtain your CLIENT_ID, CLIENT_SECRET, and REFRESH_TOKEN. These credentials are necessary for accessing the Gmail API.

3. **Start the Backend Server**

   The backend server is responsible for fetching unread emails, categorizing them, generating replies, and sending responses.

   ```sh
   node backend.js
   ```

4. **Start the Express API Server**

   The Express API server processes emails, extracts details, and generates replies using the Groq SDK.

   ```sh
   node analysis.js
   ```

---
