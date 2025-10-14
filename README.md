# Customer Delivery Performance Dashboard

A modern, interactive dashboard for analyzing customer delivery performance metrics across different series.

## Features

- 📊 Interactive charts and visualizations
- 📈 KPI tracking and comparison
- 🔍 Searchable data table
- 🤖 AI-powered performance insights
- 📱 Responsive design

## Deployment to Vercel

### Prerequisites

Before deploying, you need to set up your environment variables:

1. **Create a `.env.local` file** in the project root:
   ```bash
   echo "GEMINI_API_KEY=AIzaSyARnxJOsKMB5Ur3wBZR_Q_-1HemzAYIWzw" > .env.local
   ```

### Option 1: Deploy via Vercel CLI (Recommended)

1. **Install Vercel CLI** (if not already installed):
   ```bash
   npm install -g vercel
   ```

2. **Deploy your project**:
   ```bash
   cd "/Users/shadman/Documents/Vibe Coding/leads-analysis"
   vercel
   ```

3. **Follow the prompts**:
   - Login to your Vercel account (if first time)
   - Confirm the project settings
   - Your app will be deployed!

4. **Add Environment Variable to Vercel**:
   After first deployment, add your API key:
   ```bash
   vercel env add GEMINI_API_KEY
   ```
   When prompted, paste your API key: `AIzaSyARnxJOsKMB5Ur3wBZR_Q_-1HemzAYIWzw`
   Select all environments (Production, Preview, Development)

5. **Redeploy to apply environment variables**:
   ```bash
   vercel --prod
   ```

### Option 2: Deploy via Vercel Dashboard

1. **Push to GitHub**:
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin <your-github-repo-url>
   git push -u origin main
   ```

2. **Connect to Vercel**:
   - Go to [vercel.com](https://vercel.com)
   - Click "Add New" → "Project"
   - Import your GitHub repository
   - **Before deploying**, go to "Environment Variables"
   - Add: `GEMINI_API_KEY` = `AIzaSyARnxJOsKMB5Ur3wBZR_Q_-1HemzAYIWzw`
   - Click "Deploy"

### Option 3: Deploy via Drag & Drop

1. Go to [vercel.com](https://vercel.com)
2. Drag and drop your project folder directly into the Vercel dashboard
3. Your site will be deployed automatically!

## Configuration

The project includes a `vercel.json` configuration file that ensures proper routing for your single-page application.

## Usage

1. Upload your Data CSV file
2. Upload your Overview CSV file
3. Click "Generate Dashboard" to view analytics
4. Use the "Generate Summary" button for AI-powered insights

## Security

🔒 **API Key Protection**: The Gemini API key is securely stored as an environment variable and never exposed to the client. The application uses a Vercel serverless function (`/api/generate-insights.js`) to handle API calls on the backend.

### Local Development

For local testing with the AI insights feature:

1. Create a `.env.local` file in the project root
2. Add your API key:
   ```
   GEMINI_API_KEY=your_api_key_here
   ```
3. Install Vercel CLI: `npm install -g vercel`
4. Run locally: `vercel dev`
5. Open `http://localhost:3000`

## Technologies Used

- HTML5
- Tailwind CSS
- Chart.js
- Showdown (Markdown rendering)
- Google Gemini AI API

