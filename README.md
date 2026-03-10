# Landmark-Agency

A small Node.js service for capturing leads and sending SMS messages via Twilio.

## Setup

1. Copy `.env.example` to `.env` and fill in your Twilio credentials.
2. Install dependencies:

   ```bash
   npm install
   ```

3. Start the server:

   ```bash
   npm start
   ```

## API

- `GET /` – health check
- `POST /send-sms` – send an SMS using Twilio

### `POST /send-sms` payload

```json
{
  "to": "+15551234567",
  "body": "Hello from Landmark-Agency!"
}
```

> Ensure `TWILIO_ACCOUNT_SID`, `TWILIO_AUTH_TOKEN`, and `TWILIO_FROM_NUMBER` are set in your `.env`.
