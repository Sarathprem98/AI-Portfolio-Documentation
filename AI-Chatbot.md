# 🤖 AI Chatbot Setup Guide

This guide explains how to configure the AI chatbot included in this portfolio.

The chatbot is designed to answer **only portfolio-related questions** such as your experience, projects, skills, certifications, and contact details.

---

# Supported AI Providers

This template supports:

- ✅ Groq (Recommended)
- ✅ OpenAI
- ✅ Google Gemini

Choose any one provider based on your preference.

---

# Project Structure

```
app/
└── api/
    └── chat/
        └── route.ts
```

The chatbot backend is implemented in the API route above.

---

# Step 1 - Get an API Key

## Groq

1. Visit https://console.groq.com
2. Create an account.
3. Generate an API Key.
4. Copy the key.

---

## OpenAI

1. Visit https://platform.openai.com
2. Create an API Key.
3. Add billing if required.

---

## Gemini

1. Visit https://aistudio.google.com
2. Generate an API Key.

---

# Step 2 - Configure Environment Variables

Create a file named

```
.env.local
```

### Groq

```env
GROQ_API_KEY=your_api_key
GROQ_MODEL=llama-3.3-70b-versatile
```

### OpenAI

```env
OPENAI_API_KEY=your_api_key
OPENAI_MODEL=gpt-5.5
```

### Gemini

```env
GEMINI_API_KEY=your_api_key
GEMINI_MODEL=gemini-2.5-flash
```

Restart the development server after updating the file.

---

# Step 3 - Install Required Package

Example (Groq/OpenAI SDK)

```bash
npm install openai
```

For Gemini

```bash
npm install @google/genai
```

---

# Step 4 - Configure the API Route

Open

```
app/api/chat/route.ts
```

Replace the provider configuration if switching between Groq, OpenAI, or Gemini.

---

# Step 5 - Restrict the Chatbot

The chatbot should answer only portfolio-related questions.

Example topics:

- About Me
- Skills
- Experience
- Projects
- Certifications
- Resume
- Contact Information

If a visitor asks unrelated questions, the chatbot should politely respond that it only answers questions about your portfolio.

---

# Step 6 - Suggested Questions

You can display quick suggestion buttons such as:

- Tell me about yourself
- What projects have you worked on?
- What are your technical skills?
- Tell me about your experience.
- Show your certifications.
- How can I contact you?
- Where can I download your resume?

---

# Step 7 - Change the Chatbot Name

Locate the chatbot component and replace the default title.

Example:

```
Sarath AI
```

or

```
Portfolio Assistant
```

or

```
Ask Sarath
```

---

# Step 8 - Change the Chatbot Icon

Locate the floating chatbot button.

Example:

```tsx
<Sparkles />

<Bot />

<MessageCircle />

<Brain />

<UserRound />
```

You can also use icons from **react-icons** or your own SVG image.

---

# Step 9 - Testing

Start the development server.

```bash
npm run dev
```

Test questions like:

- Tell me about yourself.
- What projects have you completed?
- What technologies do you use?
- Show your experience.

Also verify that unrelated questions are rejected correctly.

---

# Troubleshooting

## Chatbot says API Key is missing

- Verify `.env.local`
- Restart the server
- Check environment variable names

---

## Chatbot returns 400 or 500

- Verify the API model name.
- Check the API route.
- Confirm your API key is valid.

---

## API quota exceeded

Free providers have daily or monthly limits.

Options:

- Upgrade your plan.
- Switch to another provider.
- Reduce unnecessary API calls.

---

# Recommended Provider

For this project, **Groq** is recommended because it offers:

- Fast responses
- Free tier
- Easy setup
- Good support for Llama models
- Excellent developer experience

---

Happy Coding! 🚀
