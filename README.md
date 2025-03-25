# QanDu Chat Configuration

A working configuration for LibreChat with QanDu integration, including speech services and RAG capabilities.

## Quick Start

1. Clone this repository:
```bash
git clone https://github.com/bashhh89/qanduchat-config.git
cd qanduchat-config
```

2. Copy the environment template and fill in your API keys:
```bash
cp .env.example .env
```

3. Edit the `.env` file and add your API keys:
- `GOOGLE_GENERATIVE_AI_API_KEY`: Your Google API key for Gemini models
- `RAG_OPENAI_API_KEY`: Your OpenAI API key for embeddings
- `JWT_SECRET`: A secure random string
- `ENCRYPTION_KEY`: A 32-character random string

4. Start the containers:
```bash
docker-compose up -d
```

5. Access the application:
- Main interface: http://localhost:3080
- API documentation: http://localhost:3080/api/docs

## Features

- LibreChat with QanDu integration
- Speech-to-Text and Text-to-Speech capabilities
- RAG (Retrieval-Augmented Generation) support
- Code execution capabilities
- File search and management
- Artifact handling
- Agent capabilities

## Prerequisites

- Docker and Docker Compose installed
- Ports 3080, 3005, and 80 available on your system
- OpenAI API key for speech services and RAG
- Google API key for Gemini models

## Troubleshooting

If you encounter any issues:

1. Check if all required ports are available:
```bash
netstat -ano | findstr :3080
netstat -ano | findstr :3005
netstat -ano | findstr :80
```

2. Ensure all environment variables are properly set in `.env`

3. Try rebuilding the containers:
```bash
docker-compose down
docker-compose up -d --build
```

## Maintenance

To update the containers:
```bash
docker-compose pull
docker-compose up -d
```

## Security Notes

- Never commit your `.env` file with real API keys
- Keep your API keys secure and rotate them regularly
- Monitor your API usage to avoid unexpected charges

## License

This project is licensed under the MIT License.
