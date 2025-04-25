# Care Mate - NDIS AI Assistant

This repository contains the code for Care Mate, an AI assistant designed to help NDIS participants, carers, and support coordinators in Australia.

## Project Structure

- `app.js` - Backend Node.js server that integrates with OpenAI API
- `index.html` - Simple frontend chat interface
- `netlify.toml` - Netlify configuration for deployment and redirects

## Setup Instructions

### Local Development

1. Clone this repository
2. Install dependencies:
   ```
   npm install
   ```
3. Create a `.env` file with your OpenAI API key:
   ```
   OPENAI_API_KEY=your_openai_api_key_here
   ```
4. Start the development server:
   ```
   npm run dev
   ```

### Netlify Deployment

1. Push this repository to GitHub
2. Connect your GitHub repository to Netlify
3. Configure the build settings:
   - Build command: `npm run build`
   - Publish directory: `.` (root directory)
4. Add your OpenAI API key as an environment variable in Netlify:
   - Key: `OPENAI_API_KEY`
   - Value: Your OpenAI API key

## Integration with Webflow

To integrate the Care Mate chat interface with Webflow:

1. Add an embed element to your Webflow page
2. Use the following HTML code in the embed element:

```html
<iframe src="https://your-netlify-site.netlify.app" width="100%" height="600px" frameborder="0"></iframe>
```

3. Adjust the width and height as needed to fit your design

## Mobile App Development

The mobile app version is planned to be developed using React Native. More details will be added as development progresses.

## API Endpoints

- `GET /` - Health check endpoint
- `POST /chat` - Send a message to the AI assistant
  - Request body: `{ "message": "Your message here" }`
  - Response: `{ "reply": "AI assistant response" }`

## License

This project is proprietary and confidential.
