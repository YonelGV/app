# WhatsApp AI
## Features

- Automated conversation flows for WhatsApp
- Integration with OpenAI's assistant API
- Agnostic to WhatsApp provider
- Automated responses to frequently asked questions
- Real-time message receiving and responding
- Interaction tracking with customers
- Expandable functionality through triggers

## Getting Started

1. Clone this repository
2. Install dependencies:
   ```
   pnpm install
   ```
3. Set up your environment variables in a `.env` file:
   ```
   PORT=3008
   ASSISTANT_ID=your_openai_assistant_id
   ```
4. Run the development server:
   ```
   pnpm run dev
   ```

### Using Docker (Recommended)

This project includes a Dockerfile for easy deployment and consistent environments. To use Docker:

1. Build the Docker image:
   ```
   docker build -t whatsapp-ai-assistant .
   ```
2. Run the container:
   ```
   docker run -p 3008:3008 --env-file .env whatsapp-ai-assistant
   ```

This method ensures that the application runs in a consistent environment across different systems.

## Usage

The bot is configured in the `src/app.ts` file. It uses the BuilderBot library to create flows and handle messages. The main welcome flow integrates with the OpenAI assistant to generate responses.

## Documentation