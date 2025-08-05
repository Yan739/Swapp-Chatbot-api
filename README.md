# SWAPP Chatbot Backend

<div align="center">
  <img src="https://img.shields.io/badge/NestJS-E0234E?style=for-the-badge&logo=nestjs&logoColor=white" alt="NestJS">
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript">
  <img src="https://img.shields.io/badge/Wit.ai-000000?style=for-the-badge&logo=wit.ai&logoColor=white" alt="Wit.ai">
  <img src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=node.js&logoColor=white" alt="Node.js">
</div>

## Description

A backend service for the SWAPP project's customer support chatbot. Built with NestJS and integrated with Wit.ai's, it provides intelligent natural language processing capabilities for automated customer support responses.

## Project Objectives

This backend service is designed to:

- **Intelligent Response System**: Provide smart, AI-powered responses to user queries through Wit.ai integration
- **API Integration**: Serve as a robust API endpoint for frontend chat interface integration
- **FAQ Automation**: Handle frequently asked questions about the SWAPP system efficiently
- **Scalable Architecture**: Offer a secure and scalable foundation for future feature enhancements

## Technical Architecture

### Technologies Used

- **NestJS** – Scalable Node.js framework for building efficient server-side applications
- **TypeScript** – Type-safe development with enhanced code quality
- **Wit.ai** – Free natural language processing engine for intent recognition
- **Axios** – HTTP client for API requests to Wit.ai
- **Node.js** – JavaScript runtime environment

### Project Structure

```
/swapp-chatbot-backend/
│
├── src/
│   ├── chatbot/
│   │   ├── chatbot.controller.ts     # API endpoints and request handling
│   │   ├── chatbot.service.ts        # Business logic and Wit.ai integration
│   │   └── chatbot.module.ts         # Module configuration
│   ├── app.module.ts                 # Root application module
│   └── main.ts                       # Application entry point
│
├── .env                              # Environment variables (WIT_API_TOKEN)
├── .env.example                      # Environment variables template
├── package.json                      # Project dependencies and scripts
├── nest-cli.json                     # NestJS CLI configuration
├── tsconfig.json                     # TypeScript configuration
└── README.md                         # Project documentation
```

### System Architecture

<img width="480" height="313" alt="image" src="https://github.com/user-attachments/assets/2f33c805-a916-4c09-9a43-d65e72c52363" />


*Architecture overview showing the interaction between frontend clients, NestJS backend, and Wit.ai NLP service*

## Installation & Setup

### Prerequisites

- **Node.js** (v18 or higher recommended)
- **npm** or **yarn** package manager
- **Wit.ai account** with a configured app for NLP processing

### Local Development Setup

```bash
# Clone the repository
git clone https://github.com/Yan739/swapp-chatbot-backend.git

# Navigate to the project directory
cd swapp-chatbot-backend

# Install dependencies
npm install

# Copy environment template
cp .env.example .env

# Configure your environment variables (see Configuration section)
# Edit .env file with your Wit.ai token

# Start the development server
npm run start:dev
```

### Configuration

#### Environment Variables

Create a `.env` file in the project root and configure the following variables:

```env
# Wit.ai Configuration
WIT_API_TOKEN=Bearer YOUR_WIT_AI_SERVER_ACCESS_TOKEN

# Application Configuration
PORT=3000
NODE_ENV=development

# CORS Configuration (optional)
CORS_ORIGIN=http://localhost:3001
```

> **Important**: Never commit your `.env` file to version control. Use `.env.example` as a template.

#### Wit.ai Setup

1. Create a free account at [Wit.ai](https://wit.ai)
2. Create a new app for your chatbot
3. Train your app with intents and entities relevant to SWAPP
4. Copy your Server Access Token to the `.env` file

## API Documentation

### Endpoints

#### Chat Query
```http
GET /chatbot/ask?q={your_question}
```

**Parameters:**
- `q` (string, required): The user's question or message

**Response Format:**
```json
{
  "response": "AI-generated response based on the query",
  "confidence": 0.95,
  "intent": "greeting",
  "entities": []
}
```

**Example Usage:**
```bash
# Example request
curl "http://localhost:3000/chatbot/ask?q=Bonjour"

# Example response
{
  "response": "Bonjour ! Comment puis-je vous aider avec SWAPP aujourd'hui ?",
  "confidence": 0.98,
  "intent": "greeting"
}
```

## Features

### Current Features
- RESTful API endpoint for chatbot queries
- Wit.ai integration for natural language understanding
- Intent-based response system
- TypeScript implementation for type safety
- Environment-based configuration
- Error handling and logging

### Upcoming Features
- Integration with SWAPP user database
- Conversation history persistence
- User authentication and rate limiting
- Admin dashboard for intent management
- Multi-language support
- Analytics and conversation insights

## Development

### Recommended Development Tools
- **VS Code** with NestJS, TypeScript, and ESLint extensions
- **Postman** or **Insomnia** for API testing
- **Wit.ai Dashboard** for NLP model management

### Available Scripts

```bash
# Development
npm run start:dev          # Start in development mode with hot reload
npm run start:debug        # Start in debug mode

# Production
npm run build              # Build the application
npm run start              # Start the compiled application

# Testing
npm run test               # Run unit tests
npm run test:e2e           # Run end-to-end tests
npm run test:cov           # Run tests with coverage

# Code Quality
npm run lint               # Run ESLint
npm run format             # Format code with Prettier
```

### Testing

Run the test suite to ensure everything works correctly:

```bash
# Unit tests
npm run test

# End-to-end tests
npm run test:e2e

# Test coverage
npm run test:cov
```

## Deployment

### Production Build

```bash
# Build the application
npm run build

# Start in production mode
npm run start:prod
```

### Environment Requirements
- **Node.js** 18+
- **NestJS** 10+
- **Memory**: Minimum 512MB RAM
- **Storage**: Minimum 100MB available space

## Compatibility

- **Backend Framework**: NestJS 10+
- **Runtime**: Node.js 18+
- **Frontend Compatibility**: Works with React, Vue, Angular, and other modern frameworks
- **API Standard**: RESTful API following OpenAPI specifications

## Contributing

We welcome contributions to improve the SWAPP Chatbot Backend! Please follow these steps:

1. **Fork** the repository
2. **Create** a feature branch (`git checkout -b feature/AmazingFeature`)
3. **Commit** your changes (`git commit -m 'Add some AmazingFeature'`)
4. **Push** to the branch (`git push origin feature/AmazingFeature`)
5. **Open** a Pull Request

### Development Guidelines
- Follow TypeScript best practices
- Write unit tests for new features
- Update documentation for API changes
- Follow the existing code style and conventions

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Author

**Yann NGATEU**  
*Full Stack Developer*

Developed as part of the SWAPP project – an intelligent solution for support and product management.

## Resources & Documentation

- [NestJS Documentation](https://docs.nestjs.com/)
- [Wit.ai Developer Documentation](https://wit.ai/docs)
- [TypeScript Handbook](https://www.typescriptlang.org/docs/)
- [Postman Documentation](https://learning.postman.com/)

## Support

If you encounter any issues or have questions, please:
1. Check the [Issues](https://github.com/Yan739/swapp-chatbot-backend/issues) page
2. Create a new issue with detailed information
3. Contact the development team

---

<div align="center">
  <strong>Made with ❤️ by Yann NGATEU for the SWAPP Project</strong>
</div>
