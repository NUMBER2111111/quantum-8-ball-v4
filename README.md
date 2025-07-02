# Quantum 8-Ball - AI-Powered Mystical Answers

A modern web application that provides AI-powered mystical answers to user questions, optimized for social media sharing on TikTok, Facebook, and other platforms.

## 🚀 Features

- **AI-Powered Responses**: Uses OpenAI GPT-4o exclusively to generate clever, mystical answers (no predefined responses)
- **Clarifying Questions**: AI asks up to 3 follow-up questions when more context is needed
- **Social Sharing**: Built-in sharing for Facebook, Twitter, and clipboard
- **Mobile Optimized**: Fully responsive design perfect for TikTok and social media
- **Session History**: Tracks user's previous questions in local storage
- **Cosmic UI**: Beautiful cosmic-themed interface with animations

## 🌐 Live Demo

Visit the deployed application: [Your Render URL will go here]

## 📱 Social Media Ready

This app is optimized for:
- **TikTok**: Mobile-first design with touch interactions
- **Facebook**: Open Graph meta tags for proper link previews
- **Twitter**: Twitter Card support for rich sharing
- **Mobile Web**: PWA-ready with mobile-specific optimizations

## 🛠 Tech Stack

- **Frontend**: React 18, TypeScript, Tailwind CSS, Vite
- **Backend**: Node.js, Express, TypeScript
- **AI**: OpenAI GPT-4o API
- **Storage**: In-memory storage (easily switchable to database)
- **UI Components**: shadcn/ui with Radix UI primitives

## ⚡ Quick Deploy to Render

1. **Fork this repository** to your GitHub account

2. **Connect to Render**:
   - Go to [Render.com](https://render.com)
   - Click "New +" → "Web Service"
   - Connect your GitHub account and select this repository

3. **Configure Environment Variables** in Render Dashboard:
   ```
   OPENAI_API_KEY=your_openai_api_key_here
   NODE_ENV=production
   ```

4. **Deploy Settings**:
   - Build Command: `npm ci && npm run build`
   - Start Command: `npm start`
   - Node Version: 18+

5. **Deploy**: Click "Create Web Service"

## 🔧 Local Development

### Prerequisites
- Node.js 18+
- OpenAI API Key

### Setup
1. Clone the repository:
   ```bash
   git clone <your-repo-url>
   cd quantum-8-ball
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Create environment file:
   ```bash
   cp .env.example .env
   ```

4. Add your OpenAI API key to `.env`:
   ```
   OPENAI_API_KEY=your_openai_api_key_here
   ```

5. Start development server:
   ```bash
   npm run dev
   ```

6. Open [http://localhost:5000](http://localhost:5000)

## 🏗 Project Structure

```
├── client/                 # React frontend
│   ├── src/
│   │   ├── components/     # Reusable UI components
│   │   ├── pages/         # Page components
│   │   ├── hooks/         # Custom React hooks
│   │   └── lib/           # Utility functions
│   └── public/            # Static assets
├── server/                # Express backend
│   ├── services/          # OpenAI integration
│   ├── routes.ts          # API endpoints
│   └── storage.ts         # Data storage layer
├── shared/                # Shared types and schemas
└── render.yaml           # Render deployment config
```

## 🎯 API Endpoints

- `POST /api/ask` - Ask a question to the 8-ball
- `POST /api/clarify` - Provide clarification for a question
- `GET /api/questions/:sessionId` - Get questions for a session
- `GET /api/recent-questions` - Get recent public questions

## 🎨 Customization

### Styling
- Colors and theme: `client/src/index.css`
- Component styles: Individual component files
- Cosmic effects: CSS animations in `index.css`

### AI Responses
- Modify prompts: `server/services/openai.ts`
- Fallback responses: Same file, fallback array
- Response format: Adjust JSON schema in prompts

### Social Sharing
- Update meta tags: `client/index.html`
- Modify share text: `client/src/pages/quantum-8-ball.tsx`
- Add platforms: Extend `shareToSocial` function

## 🔐 Environment Variables

| Variable | Description | Required |
|----------|-------------|----------|
| `OPENAI_API_KEY` | OpenAI API key for GPT-4o | Yes |
| `NODE_ENV` | Environment (development/production) | No |
| `PORT` | Server port (default: 5000) | No |

## 📊 Performance

- **Bundle Size**: Optimized with Vite
- **Loading Speed**: Lazy loading and code splitting
- **Mobile Performance**: Touch-optimized interactions
- **SEO**: Complete meta tags and semantic HTML

## 🐛 Troubleshooting

### Common Issues

1. **OpenAI API Errors**:
   - Check API key is valid
   - Verify account has credits
   - Check rate limits

2. **Build Failures**:
   - Run `npm ci` to clean install
   - Check Node.js version (18+)
   - Verify all environment variables

3. **Social Sharing Issues**:
   - Update meta tags with your domain
   - Test with Facebook Debugger
   - Verify image URLs are accessible

## 📝 License

MIT License - feel free to use this project for your own mystical endeavors!

## 🌟 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## 📧 Support

For issues and questions:
- Open a GitHub issue
- Check the troubleshooting section
- Review the API documentation

---

*May the cosmic forces guide your deployment journey!* ✨