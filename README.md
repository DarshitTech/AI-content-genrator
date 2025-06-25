

# AI Content Generator  
An intelligent, real-time content generation app powered by **Google Gemini API** and built using **Node.js**, **Express.js**, and **Socket.IO**. Create compelling content with the power of AI — instantly and securely. 🚀  

---

## 🌟 Features

- 🧠 **AI-Powered Content** – Generates high-quality text using the Gemini API.  
- ⚡ **Real-Time Response** – WebSocket-based live interaction for seamless UX.  
- 🔐 **Secure API Key Handling** – Environment-based secrets management via `.env`.  
- 🚀 **Quick Setup** – Lightweight, fast, and easy to deploy with Node.js.

---

## 🔧 Prerequisites

Make sure the following tools are installed on your system:

- [Git](https://git-scm.com/)  
- [Node.js & npm](https://nodejs.org/)

---

## 🛠️ Setup Instructions

### 1️⃣ Clone the Repository
```bash
git clone <repository-url>
cd <project-folder-name>
```

### 2️⃣ Initialize the Project
```bash
npm init -y
```

### 3️⃣ Install Required Dependencies
```bash
npm install express socket.io body-parser path dotenv
```

### 4️⃣ Configure Environment Variables
Create a `.env` file in the root directory and add your Gemini API key:
```env
GEMINI_API_KEY=your_gemini_api_key
```

> 🔍 **How to get a Gemini API Key**:
> 1. Visit [Google AI Gemini](https://ai.google.com/gemini/)  
> 2. Sign in with your Google Account  
> 3. Go to API Access → Generate a new key  
> 4. Copy & paste it into your `.env` file

---

## 🔌 Run the Server
Start the application using **Nodemon** for auto-reload on changes:
```bash
nodemon app.js
```

---

## 📡 WebSocket Integration

- Clients connect using `socket.io-client`  
- Server listens for user prompts and broadcasts generated content in real-time  

```js
// Sample: WebSocket Flow
io.on('connection', (socket) => {
  socket.on('generatePrompt', async (prompt) => {
    const content = await generateContentFromGemini(prompt);
    socket.emit('aiResponse', content);
  });
});
```

---

## 📬 API Endpoints

### 🔹 POST `/generate`
Generates AI-powered content from a user prompt.

**Request Example:**
```json
{
  "prompt": "Explain the future of AI in healthcare."
}
```

**Response Example:**
```json
{
  "content": "AI is set to revolutionize healthcare by enhancing diagnosis, personalizing treatment, and automating administrative tasks..."
}
```

---

## 🎥 Demo & Preview

- 🎬 **Video Walkthrough**: [Watch on YouTube](https://youtu.be/uPewJ1NgvgA)

---

## 🤝 Contributing

We ❤️ contributions!  
Feel free to:
- Fork the repo  
- Suggest features  
- Open PRs  
- Report bugs via [Issues](https://github.com/DarshiI2009/AI-content-genrator/issues)

---

## 📌 Tech Stack

- **Backend**: Node.js, Express.js  
- **Real-Time**: Socket.IO  
- **AI Integration**: Google Gemini API  
- **Tools**: dotenv, body-parser, path

---


