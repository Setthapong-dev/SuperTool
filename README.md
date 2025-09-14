# 🚀 SuperTool - Full Stack AI Application

A comprehensive AI-powered web application built with React and Express.js, featuring content generation, image processing, and community features.

## 🌐 Live Demo

**🚀 [Try SuperTool Live](https://super-tool-wine.vercel.app/)**

Experience all the AI-powered features including article generation, image creation, and community interactions.

## ✨ Features

### 🤖 AI Content Generation
- **Article Writing**: Generate articles from prompts using OpenAI GPT
- **Blog Titles**: Create engaging blog titles
- **Image Generation**: Create images from text using Clipdrop API

### 🖼️ Image Processing
- **Background Removal**: Remove backgrounds from images
- **Object Removal**: Remove unwanted objects from photos
- **Cloud Storage**: Secure image storage with Cloudinary

### 📄 Document Analysis
- **Resume Review**: AI-powered resume analysis and feedback

### 👥 Community Features
- **Share Creations**: Publish and share your AI-generated content
- **Like System**: Like and interact with community creations
- **User Dashboard**: Track your creations and activity

### 🔐 Authentication & Security
- **Clerk Authentication**: Secure user authentication
- **Premium Plans**: Tiered access to AI features
- **Protected Routes**: Secure API endpoints

## 🛠️ Tech Stack

### Frontend (Client)
- **React 19** - Modern UI library
- **Vite** - Fast build tool and dev server
- **Tailwind CSS** - Utility-first CSS framework
- **React Router** - Client-side routing
- **Clerk React** - Authentication
- **Axios** - HTTP client
- **Lucide React** - Icon library
- **React Hot Toast** - Notifications

### Backend (Server)
- **Express.js** - Web framework
- **Node.js** - JavaScript runtime
- **Neon Database** - PostgreSQL database
- **Cloudinary** - Cloud image storage
- **OpenAI API** - AI content generation
- **Clipdrop API** - Image generation
- **Multer** - File upload handling
- **Clerk Express** - Server-side authentication

## 🚀 Quick Start

### 🌐 Try It Live First
**Want to see SuperTool in action?** Visit our live demo at [https://super-tool-wine.vercel.app/](https://super-tool-wine.vercel.app/) to experience all features without any setup!

### Prerequisites
- Node.js (v18 or higher)
- npm or yarn
- Clerk account for authentication
- OpenAI API key
- Clipdrop API key
- Cloudinary account
- Neon Database account

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd SuperTool-Full-Stack
   ```

2. **Install dependencies**
   ```bash
   # Install server dependencies
   cd server
   npm install
   
   # Install client dependencies
   cd ../client
   npm install
   ```

3. **Environment Setup**

   **Server (.env in server folder):**
   ```env
   PORT=3000
   CLERK_SECRET_KEY=your_clerk_secret_key
   OPENAI_API_KEY=your_openai_api_key
   CLIPDROP_API_KEY=your_clipdrop_api_key
   CLOUDINARY_CLOUD_NAME=your_cloudinary_cloud_name
   CLOUDINARY_API_KEY=your_cloudinary_api_key
   CLOUDINARY_API_SECRET=your_cloudinary_api_secret
   DATABASE_URL=your_neon_database_url
   ```

   **Client (.env in client folder):**
   ```env
   VITE_CLERK_PUBLISHABLE_KEY=your_clerk_publishable_key
   VITE_BASE_URL=http://localhost:3000
   ```

4. **Run the application**
   ```bash
   # Terminal 1 - Start server
   cd server
   npm run server
   
   # Terminal 2 - Start client
   cd client
   npm run dev
   ```

5. **Access the application**
   - **Live Demo**: [https://super-tool-wine.vercel.app/](https://super-tool-wine.vercel.app/)
   - Local Frontend: http://localhost:5173
   - Local Backend API: http://localhost:3000

## 📁 Project Structure

```
SuperTool-Full-Stack/
├── client/                 # React frontend
│   ├── src/
│   │   ├── components/     # Reusable components
│   │   ├── pages/         # Page components
│   │   ├── assets/        # Static assets
│   │   └── App.jsx        # Main app component
│   ├── public/            # Public assets
│   └── package.json
├── server/                 # Express backend
│   ├── controllers/       # Route controllers
│   ├── routes/           # API routes
│   ├── middlewares/      # Custom middlewares
│   ├── configs/          # Configuration files
│   └── server.js         # Main server file
└── README.md
```

## 🔧 API Endpoints

### AI Routes (`/api/ai`)
- `POST /generate-article` - Generate articles
- `POST /generate-blog-title` - Generate blog titles
- `POST /generate-image` - Generate images
- `POST /remove-image-background` - Remove image backgrounds
- `POST /remove-image-object` - Remove objects from images
- `POST /resume-review` - Review resumes

### User Routes (`/api/user`)
- `GET /get-user-creations` - Get user's creations
- `GET /get-published-creations` - Get published creations
- `POST /toggle-like-creation` - Like/unlike creations

## 🎨 UI Components

- **Dashboard**: User overview and recent creations
- **Write Article**: AI article generation interface
- **Generate Images**: Image creation with prompts
- **Community**: Browse and interact with shared content
- **Remove Background**: Image background removal tool
- **Remove Object**: Object removal from images
- **Review Resume**: Resume analysis tool

## 🔐 Authentication Flow

1. User signs up/logs in via Clerk
2. JWT tokens are managed automatically
3. Protected routes require authentication
4. Premium features require subscription

## 🚀 Deployment

### Vercel Deployment
Both client and server are configured for Vercel deployment:

```bash
# Deploy client
cd client
vercel --prod

# Deploy server
cd server
vercel --prod
```

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🆘 Support

If you encounter any issues or have questions:

1. **Try the Live Demo**: [https://super-tool-wine.vercel.app/](https://super-tool-wine.vercel.app/)
2. Check the [Issues](https://github.com/your-repo/issues) page
3. Create a new issue with detailed description
4. Contact the development team

## 🙏 Acknowledgments

- [OpenAI](https://openai.com/) for AI content generation
- [Clipdrop](https://clipdrop.co/) for image generation
- [Clerk](https://clerk.com/) for authentication
- [Cloudinary](https://cloudinary.com/) for image storage
- [Neon](https://neon.tech/) for database hosting

---

**Made with ❤️ by the SuperTool Team**
