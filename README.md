# VibeCV - Professional CV Website

A modern, dynamic CV website that securely fetches content from external sources without exposing URLs to clients.

## Features

- 🔒 **Secure Content Proxy**: Fetches dynamic content server-side, keeping external URLs hidden
- 🎨 **Modern UI**: Beautiful gradient design with smooth animations
- 🚀 **Fast Loading**: Optimized content delivery
- 📱 **Responsive**: Works perfectly on all devices
- 🧹 **Clean Content**: Automatically removes branding and unwanted elements

## Tech Stack

- **Backend**: Node.js + Express
- **Frontend**: Vanilla JavaScript + CSS3
- **HTTP Client**: Axios
- **Styling**: Custom CSS with modern gradients and animations

## Installation

1. Install dependencies:
```bash
npm install
```

2. Create environment file:
```bash
cp .env.example .env
```

3. Start the development server:
```bash
npm run dev
```

4. Start the production server:
```bash
npm start
```

## Project Structure

```
VibeCV/
├── server.js              # Express server with content proxy
├── package.json           # Dependencies and scripts
├── .env.example          # Environment variables template
├── public/               # Static files
│   ├── index.html       # Main HTML page
│   ├── styles.css       # CSS styling
│   └── app.js           # Client-side JavaScript
└── README.md            # This file
```

## API Endpoints

- `GET /` - Main page
- `GET /api/content` - Fetch dynamic content (server-side only)
- `GET /api/health` - Health check

## How It Works

1. **Client requests page** → Server serves `index.html`
2. **JavaScript loads** → Calls `/api/content` endpoint
3. **Server fetches** → Retrieves content from external source (URL hidden)
4. **Content cleaned** → Removes branding and unwanted elements
5. **Client displays** → Renders clean content dynamically

## Security

- External URLs are stored only on the server
- Content is sanitized before being sent to client
- No API keys or sensitive data exposed
- CORS enabled for controlled access

## Development

```bash
# Install dependencies
npm install

# Run in development mode with auto-reload
npm run dev

# Run in production mode
npm start
```

## Customization

### Update Content Source
Edit `server.js` and change the `GEMINI_URL` constant (server-side only):
```javascript
const GEMINI_URL = 'your-new-url-here';
```

### Modify Styling
Edit `public/styles.css` to customize colors, fonts, and layout.

### Change Content Cleaning Rules
Edit the content cleaning logic in `server.js` or `public/app.js`.

## License

MIT

## Author

Duong Cao Nhan - Azure AI Engineer
