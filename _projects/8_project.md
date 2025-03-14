---
layout: page
title: AI Phone Assistant
description: AI-powered phone assistant using LLMs and Twilio for small business calls.
img: assets/img/Phone_Assistant_Project.png
importance: 8
category: work
giscus_comments: false
---

---

## 📋 Overview

<br/>

This project implements an intelligent phone assistant that allows small businesses (such as restaurants) to offer automated assistance to their customers via phone calls. The system:

- Understands natural language using LLMs
- Processes phone calls with Twilio
- Maintains conversation context
- Provides coherent and natural responses
- Assists with information and reservations

Ideal for small businesses looking to improve accessibility without the complexity of traditional IVR systems.

---

## 🚀 Features

<br/>

- **24/7 Support**: Responds to calls even outside of business hours  
- **Natural Language Understanding**: Understands conversational language queries  
- **Context Retention**: Remembers previous information during the conversation  
- **Booking Management**: Can gather information for bookings  
- **Easy Implementation**: Minimal setup required  
- **Integration with Existing Systems**: Can connect with booking systems  
- **Enhanced Accessibility**: Especially useful for seniors or those with technological limitations  

---

## 🔧 Technologies

<br/>

- **TypeScript**: Main programming language  
- **Hono**: Lightweight and fast web framework  
- **OpenAI API**: Language models  
- **Twilio API**: Telephony integration  
- **Pino**: Logging system 

---

## ⚙️ Requirements

<br/>

- Node.js 16.x or higher
- Twilio account with a phone number
- OpenAI API key
- Stable internet connection

---

## 📥 Installation

<br/>

1. Clone the repository:
```bash
git clone https://github.com/felixsuarez0727/Telephone-Assistant.git
cd Telephone-Assistant
```

2. Install dependencies:
```bash
npm install
```

3. Create a `.env` file based on `.env.example`:
```bash
cp .env.example .env
```

4. Update the `.env` file with your credentials:

<br/>

```
# OpenAI API configuration
OPENAI_API_KEY=your_openai_api_key
OPENAI_MODEL=gpt-3.5-turbo

# Twilio configuration
TWILIO_ACCOUNT_SID=your_twilio_account_sid
TWILIO_AUTH_TOKEN=your_twilio_auth_token
TWILIO_PHONE_NUMBER=your_twilio_phone_number

# Server configuration
PORT=3000
NODE_ENV=development

# Restaurant specific configuration
RESTAURANT_NAME="Your Restaurant"
RESTAURANT_OPENING_HOURS="12:00 - 22:00"
MAX_RESERVATION_SIZE=10
```

---

## 🏃‍♂️ Execution

<br/>

### Development

```bash
npm run dev
```

### Production

```bash
npm run build
npm run start
```

---

## 🌐 Twilio Configuration

<br/>

1. Go to your [Twilio Dashboard](https://www.twilio.com/console)
2. Configure a webhook for your phone number:
   - Webhook URL:  `https://your-domain.com/api/incoming-call`
   - HTTP Method: `POST`

---

## 🔄 Project Structure

<br/>

```
phone-assistant/
│
├── src/
│   ├── index.ts              # Main server entry point
│   ├── config/
│   │   ├── openai.ts         # OpenAI client configuration
│   │   ├── twilio.ts         # Twilio configuration
│   │   └── constants.ts      # System constants and prompts
│   │
│   ├── controllers/
│   │   ├── callController.ts # Controller for handling calls
│   │   ├── reservationController.ts # Controller for reservations
│   │   └── miscController.ts # Controller for miscellaneous functions
│   │
│   ├── services/
│   │   ├── openaiService.ts  # Services for OpenAI communication
│   │   ├── twilioService.ts  # Services for generating TwiML
│   │   └── stateService.ts   # Conversation state management
│   │
│   ├── utils/
│   │   ├── logger.ts         # Logging utilities
│   │   └── helpers.ts        # Helper functions
│   │
│   ├── types/
│   │   └── index.ts          # TypeScript type definitions
│   │
│   └── routes/
│       └── index.ts          # Server route definitions
│
├── tests/
│   ├── unit/                 # Unit tests
│   └── integration/          # Integration tests
│
├── docs/                     # Documentation
│
└── public/                   # Static files
```

---

## 📊 Endpoints

<br/>

### Telephony
- `POST /api/incoming-call`: Endpoint for incoming calls
- `POST /api/respond`: Endpoint for processing user responses

<br/>

### Reservations (optional)
- `POST /api/reservations`: Create a new reservation
- `GET /api/reservations`: List existing reservations

<br/>

### System
- `GET /api/health`: Check system status
- `GET /api/stats`: Retrieve statistics
- `GET /api/config`: Retrieve current configuration
- `GET /api/echo`: Test endpoint for debugging

---

## 🧪 Testing

<br/>

### Run Tests
```bash
npm test
```

<br/>

### Unit Tests
```bash
npm run test:unit
```
<br/>

### Integration Tests
```bash
npm run test:integration
```

---

## 🔍 Monitoring

<br/>

The system includes a `/api/health` endpoint that allows checking the status of all components. You can integrate it with monitoring services such as Uptime Robot or Pingdom.

---

## 📈 Expected Results

<br/>

Based on recent studies:
- Voice comprehension: ~90% under ideal conditions
- Conversational coherence: ~80%
- Information accuracy: ~75%
- Customer satisfaction: ~70%

---

## 🛠️ Customization

<br/>

### System Prompt

To modify the assistant’s behavior, edit the system prompt in `src/config/constants.ts`:

```typescript
export const SYSTEM_PROMPT = `You are a phone assistant for...`;
```

---

## 🚧 Known Limitations

<br/>

- Cannot transfer calls to human operators (in this version)
- Speech recognition may struggle in noisy environments
- Dependent on OpenAI and Twilio service availability

---

## 🔜 Future Improvements

<br/>

- Integration with CRM systems
- Multi-language support
- Sentiment analysis
- Human operator call transfers
- Web-based admin panel

---

<!-- Button to GitHub Repo -->
<div style="text-align:left; margin-bottom: 20px;">
  <a href="https://github.com/felixsuarez0727/Telephone-Assistant" target="_blank">
    <button id="github-repo-button" style="padding: 10px 20px; color: white; border: none; border-radius: 5px; cursor: pointer;">
      View Repository on GitHub
    </button>
  </a>
</div>