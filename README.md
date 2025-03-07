# AI Content Generator

## Overview
The AI Content Generator is a Node.js-based application that leverages Google Gemini API to generate high-quality AI-driven content. This application integrates **Express.js**, **Socket.io**, and environment-based configurations for seamless real-time operations.

## Features
- **AI-Powered Content Generation**: Uses the Gemini API to generate intelligent and engaging content.
- **Real-Time Communication**: WebSocket support for live interactions.
- **Secure API Handling**: Manages API keys using environment variables.
- **Easy Deployment**: Lightweight and quick setup with Node.js.

## Prerequisites
Ensure you have the following installed before proceeding:
- **Git**: [Download & Install Git](https://git-scm.com/)
- **Node.js**: [Download & Install Node.js](https://nodejs.org/)
- **npm (Node Package Manager)**: Comes with Node.js installation

## Setup Instructions

### Step 1: Clone the Repository
```sh
git clone <repository-url>
cd <project-folder-name>
```

### Step 2: Initialize the Project
```sh
npm init -y
```
This will generate a `package.json` file with default settings.

### Step 3: Install Dependencies
```sh
npm install
npm install express socket.io body-parser path dotenv
```
This installs all necessary packages:
- **Express**: Web framework for handling requests.
- **Socket.io**: Enables real-time communication.
- **Body-parser**: Parses incoming JSON requests.
- **Path**: Helps manage file paths.
- **Dotenv**: Loads environment variables from a `.env` file.

### Step 4: Configure API Key
Create a `.env` file in the root directory and add:
```
GEMINI_API_KEY="****"
```
#### 🔍 How to Get a Gemini API Key
1. Go to [Google AI Gemini](https://ai.google.com/gemini/).
2. Sign in with your Google account.
3. Navigate to API access settings.
4. Generate a new API key and copy it.
5. Paste it into your `.env` file as shown above.

### Step 5: Run the Server
```sh
nodemon app.js
```
This starts the server with **Nodemon**, ensuring automatic restarts on file updates.

## API Endpoints
### 🔹 Generate AI Content
**POST** `/generate`
**Request Body:**
```json
{
  "prompt": "Write a blog post about AI advancements."
}
```
**Response:**
```json
{
  "content": "AI has revolutionized various industries..."
}
```

## WebSocket Implementation
- Clients connect via WebSockets to receive real-time AI-generated content.
- The server sends responses instantly upon processing requests.

## Contributing
Contributions are welcome! Fork the repository, create a branch, and submit a pull request.

🚀 **Build smarter AI-driven content today!**

