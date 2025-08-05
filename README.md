SWAPP Chatbot Backend
<div align="center"> <img src="https://img.shields.io/badge/NestJS-E0234E?style=for-the-badge&logo=nestjs&logoColor=white" alt="NestJS"> <img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript"> <img src="https://img.shields.io/badge/Wit.ai-000000?style=for-the-badge&logo=wit.ai&logoColor=white" alt="Wit.ai"> <img src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=node.js&logoColor=white" alt="Node.js"> </div>
Description
A backend service for the SWAPP project's customer support chatbot. It uses NestJS and the free NLP API from Wit.ai to handle natural language interactions and provide automated support responses.

Project Objective
This backend service aims to:

Provide smart, automated responses to user queries using AI (via Wit.ai)

Serve as an API endpoint for frontend chat interface integration

Help users with frequently asked questions about the SWAPP system

Offer a scalable and secure structure for future enhancements

Technical Architecture
Technologies Used
NestJS – Scalable Node.js framework

TypeScript – Type-safe development

Wit.ai – Free NLP engine to process natural language

Axios – For API requests to Wit.ai

Node.js – Runtime environment

File Structure
bash
Copier
Modifier
/swapp-chatbot-backend/
│
├── src/
│   ├── chatbot/
│   │   ├── chatbot.controller.ts     # API endpoints
│   │   ├── chatbot.service.ts        # Business logic
│   │   └── chatbot.module.ts         # Module definition
│   ├── app.module.ts                 # Main app module
│   └── main.ts                       # App entry point
│
├── .env                              # Environment variables (WIT_API_TOKEN)
├── package.json
└── README.md
Architecture Diagrams
System Overview
<img width="1000" alt="System Diagram" src="https://github.com/user-attachments/assets/27fd40dc-7121-47cb-b435-72e9e94dbd82" />
Installation
Prerequisites
Node.js (v18+ recommended)

npm or yarn

A Wit.ai account and app (for your NLP integration)

Local Installation
bash
Copier
Modifier
# Clone the project
git clone https://github.com/Yan739/swapp-chatbot-backend.git

# Navigate to the folder
cd swapp-chatbot-backend

# Install dependencies
npm install

# Run the application
npm run start:dev
Configuration
Environment Variables
Create a .env file at the root of the project and add your Wit.ai Server Access Token:

env
Copier
Modifier
WIT_API_TOKEN=Bearer YOUR_WIT_AI_TOKEN_HERE
Update chatbot.service.ts to use this token dynamically if needed.

Features
Current
API endpoint to query chatbot: GET /chatbot/ask?q=your_question

Integration with Wit.ai for intent recognition

Predefined responses based on top-level intents

Upcoming
Integration with SWAPP user data

Save conversation history

User authentication & rate limiting

Admin dashboard to monitor and train intents

Usage
Start the server: npm run start:dev

Send a GET request to the chatbot API:

bash
Copier
Modifier
GET http://localhost:3000/chatbot/ask?q=Bonjour
Receive a JSON response:

json
Copier
Modifier
{
  "response": "Bonjour ! Comment puis-je vous aider ?"
}
Development
Recommended Tools
VS Code with NestJS & ESLint extensions

Postman for testing API requests

Wit.ai dashboard to manage your NLP intents

Scripts
bash
Copier
Modifier
npm run start:dev     # Run in dev mode
npm run build         # Build for production
npm run start         # Start compiled code
Compatibility
Node.js 18+

NestJS 10+

Compatible with most frontend clients (React, Vue, Angular, etc.)

Contributing
Contributions are welcome! Here's how:

Fork the repository

Create a branch (git checkout -b feature/NewFeature)

Commit your changes (git commit -m 'Add NewFeature')

Push to the branch (git push origin feature/NewFeature)

Create a Pull Request

Author
Yann NGATEU

Project developed as part of the SWAPP project – an intelligent solution for support and product management.

Useful Links
NestJS Documentation

Wit.ai Documentation

TypeScript Handbook

Postman

<div align="center"> Made with ❤️ by Yann NGATEU for the SWAPP Project </div>
