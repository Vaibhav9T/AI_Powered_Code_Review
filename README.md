# AI-Powered Code Review

An intelligent code review application that leverages Google's Gemini 2.5 Flash model to provide professional code analysis and suggestions. Write or paste your code, get instant feedback from an AI reviewer with 7+ years of simulated development experience.

<img width="2869" height="1629" alt="image" src="https://github.com/user-attachments/assets/6ec1e017-b2f2-44b8-9393-ad21e3c0cc44" />


## Features

- 🤖 **AI-Powered Reviews**: Utilizes Google Gemini 2.5 Flash for intelligent code analysis
- 💻 **Live Code Editor**: Syntax-highlighted code editor with support for multiple languages
- 📊 **Detailed Feedback**: Receive comprehensive feedback on:
  - Code quality and best practices
  - Performance optimization opportunities
  - Security vulnerabilities
  - Design patterns and maintainability
  - Error detection and bug prevention
- 🎨 **Modern UI**: Clean, responsive interface with split-view design
- ⚡ **Real-time Analysis**: Get instant code review results
- 📝 **Markdown Rendering**: Beautiful formatting for review results with syntax highlighting

## Tech Stack

### Frontend
- **React 19.1.1** - UI library
- **Vite 7.1.7** - Build tool and dev server
- **Axios** - HTTP client
- **Prism.js** - Syntax highlighting for code editor
- **React Simple Code Editor** - Code editing component
- **React Markdown** - Markdown rendering
- **Rehype Highlight** - Code syntax highlighting in markdown

### Backend
- **Node.js** - Runtime environment
- **Express 5.1.0** - Web framework
- **Google Generative AI** - Gemini 2.5 Flash model integration
- **CORS** - Cross-origin resource sharing
- **dotenv** - Environment variable management

## Project Structure

```
.
├── Frontend/
│   ├── src/
│   │   ├── App.jsx           # Main application component
│   │   ├── App.css           # Application styles
│   │   ├── main.jsx          # Application entry point
│   │   └── index.css         # Global styles
│   ├── public/               # Static assets
│   ├── index.html            # HTML template
│   ├── package.json          # Frontend dependencies
│   ├── vite.config.js        # Vite configuration
│   └── eslint.config.js      # ESLint configuration
│
└── Backend/
    ├── src/
    │   ├── app.js                      # Express app setup
    │   ├── controllers/
    │   │   └── ai.controller.js        # AI controller logic
    │   ├── routes/
    │   │   └── ai.routes.js            # API routes
    │   └── services/
    │       └── ai.service.js           # Gemini AI integration
    ├── server.js                       # Server entry point
    └── package.json                    # Backend dependencies
```

## Getting Started

### Prerequisites

- Node.js (v16 or higher)
- npm or yarn
- Google Gemini API Key ([Get one here](https://makersuite.google.com/app/apikey))

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/Vaibhav9T/AI_Powered_Code_Review.git
   cd AI_Powered_Code_Review
   ```

2. **Setup Backend**
   ```bash
   cd Backend
   npm install
   ```

3. **Configure Environment Variables**
   
   Create a `.env` file in the `Backend` directory:
   ```env
   GOOGLE_GEMINI_KEY=your_gemini_api_key_here
   ```

4. **Setup Frontend**
   ```bash
   cd ../Frontend
   npm install
   ```

### Running the Application

1. **Start the Backend Server**
   ```bash
   cd Backend
   node server.js
   ```
   Server will run on `http://localhost:3000`

2. **Start the Frontend Development Server**
   ```bash
   cd Frontend
   npm run dev
   ```
   Application will be available at `http://localhost:5173`

### Building for Production

**Frontend:**
```bash
cd Frontend
npm run build
npm run preview
```

**Backend:**
```bash
cd Backend
# Set NODE_ENV=production in your .env file
node server.js
```

## API Endpoints

### POST `/ai/get-review`

Reviews the provided code and returns AI-generated feedback.

**Request Body:**
```json
{
  "code": "your code here"
}
```

**Response:**
```
Markdown-formatted code review with suggestions
```

## Usage

1. Open the application in your browser
2. Enter or paste your code in the left editor panel
3. Click the **Review** button
4. View the AI-generated review in the right panel
5. Use the **Clear** button to reset both panels

## Features in Detail

### AI Review Capabilities

The AI reviewer analyzes code for:

- ✅ **Code Quality**: Clean, maintainable, and well-structured code
- ✅ **Best Practices**: Industry-standard coding practices
- ✅ **Performance**: Optimization opportunities and bottlenecks
- ✅ **Security**: Vulnerability detection (SQL injection, XSS, CSRF)
- ✅ **Error Detection**: Potential bugs and logical flaws
- ✅ **Scalability**: Adaptability for future growth
- ✅ **Readability**: Code clarity and maintainability
- ✅ **DRY & SOLID Principles**: Code duplication and modular design
- ✅ **Test Coverage**: Unit/integration test suggestions
- ✅ **Documentation**: Comment and docstring recommendations

## Environment Variables

### Backend (.env)

```env
GOOGLE_GEMINI_KEY=your_google_gemini_api_key
```

## Technologies & Libraries

### Frontend Dependencies
```json
{
  "axios": "^1.13.2",
  "prismjs": "^1.30.0",
  "react": "^19.1.1",
  "react-dom": "^19.1.1",
  "react-markdown": "^10.1.0",
  "react-simple-code-editor": "^0.14.1",
  "rehype-highlight": "^7.0.2"
}
```

### Backend Dependencies
```json
{
  "@google/generative-ai": "^0.24.1",
  "cors": "^2.8.5",
  "dotenv": "^17.2.3",
  "express": "^5.1.0"
}
```

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## Future Enhancements

- [ ] Support for multiple programming languages
- [ ] User authentication and saved reviews
- [ ] Code diff comparison
- [ ] Export reviews as PDF
- [ ] Integration with GitHub/GitLab
- [ ] Custom review templates
- [ ] Team collaboration features

## Troubleshooting

### Common Issues

**Issue: "API Key not found"**
- Solution: Ensure you've created a `.env` file in the Backend directory with `GOOGLE_GEMINI_KEY`

**Issue: "CORS Error"**
- Solution: The backend includes CORS middleware. Ensure the backend is running on port 3000

**Issue: "Module not found"**
- Solution: Run `npm install` in both Frontend and Backend directories

## License

This project is licensed under the ISC License.

## Acknowledgments

- Google Gemini AI for powering the code review engine
- React and Vite communities for excellent tooling
- Prism.js for syntax highlighting capabilities
- The open-source community for various libraries used in this project

## Contact & Support

- **Project Link**: [https://github.com/Vaibhav9T/AI_Powered_Code_Review](https://github.com/Vaibhav9T/AI_Powered_Code_Review)
- **Issues**: [Report a bug or request a feature](https://github.com/Vaibhav9T/AI_Powered_Code_Review/issues)

---

**Note**: This application requires an active internet connection and a valid Google Gemini API key to function properly. The AI model is hosted by Google and requires API credits for usage.

## Demo

🚀 **Live Demo**: [AI-Powered Code Review](https://ai-powered-code-review-iota.vercel.app/)

---

Made with ❤️ by [Vaibhav9T](https://github.com/Vaibhav9T)
