# 🎨 SuperTool Client - React Frontend

Modern React frontend for the SuperTool application, built with Vite and Tailwind CSS.

## 🚀 Quick Start

### Prerequisites
- Node.js (v18 or higher)
- npm or yarn

### Installation
```bash
npm install
```

### Development
```bash
npm run dev
```

### Build
```bash
npm run build
```

### Preview
```bash
npm run preview
```

## 🛠️ Tech Stack

- **React 19** - Modern UI library with latest features
- **Vite 7** - Lightning-fast build tool
- **Tailwind CSS 4** - Utility-first CSS framework
- **React Router DOM** - Client-side routing
- **Clerk React** - Authentication and user management
- **Axios** - HTTP client for API calls
- **Lucide React** - Beautiful icon library
- **React Hot Toast** - Toast notifications
- **React Markdown** - Markdown rendering

## 📁 Project Structure

```
src/
├── components/          # Reusable UI components
│   └── CreationItem.jsx
├── pages/              # Page components
│   ├── Home.jsx        # Landing page
│   ├── Dashboard.jsx   # User dashboard
│   ├── WriteArticle.jsx # Article generation
│   ├── GenerateImages.jsx # Image generation
│   ├── Community.jsx   # Community feed
│   └── Layout.jsx      # Main layout wrapper
├── assets/             # Static assets and data
├── App.jsx             # Main app component
└── main.jsx            # App entry point
```

## 🎯 Key Features

### Authentication
- Secure login/signup with Clerk
- Protected routes
- User session management

### AI Features
- **Article Generation**: Create articles from prompts
- **Image Generation**: Generate images using AI
- **Blog Titles**: Generate engaging blog titles
- **Resume Review**: AI-powered resume analysis

### Image Processing
- **Background Removal**: Remove backgrounds from images
- **Object Removal**: Remove unwanted objects
- **Image Upload**: Secure file upload with preview

### Community
- **Share Creations**: Publish AI-generated content
- **Like System**: Like and interact with posts
- **User Dashboard**: Track personal creations

## 🔧 Environment Variables

Create a `.env` file in the client directory:

```env
VITE_CLERK_PUBLISHABLE_KEY=your_clerk_publishable_key
VITE_BASE_URL=http://localhost:3000
```

## 🎨 UI Components

### Pages
- **Home**: Landing page with feature overview
- **Dashboard**: User's personal dashboard
- **Write Article**: AI article generation interface
- **Generate Images**: Image creation with prompts
- **Community**: Browse shared creations
- **Remove Background**: Background removal tool
- **Remove Object**: Object removal tool
- **Review Resume**: Resume analysis interface

### Components
- **CreationItem**: Displays user creations
- **Layout**: Main app layout with navigation

## 🔄 State Management

- **React Hooks**: useState, useEffect for local state
- **Clerk Hooks**: useAuth, useUser for authentication
- **API State**: Axios for server communication

## 🎨 Styling

- **Tailwind CSS**: Utility-first styling
- **Responsive Design**: Mobile-first approach
- **Custom Components**: Reusable styled components
- **Icons**: Lucide React icon library

## 🚀 Build & Deployment

### Development
```bash
npm run dev
# Runs on http://localhost:5173
```

### Production Build
```bash
npm run build
# Creates optimized build in dist/
```

### Preview Production Build
```bash
npm run preview
# Preview the production build locally
```

### Vercel Deployment
```bash
vercel --prod
```

## 🔍 Code Quality

- **ESLint**: Code linting and formatting
- **React Hooks**: Modern React patterns
- **TypeScript Ready**: Prepared for TypeScript migration

## 📱 Responsive Design

- **Mobile First**: Optimized for mobile devices
- **Tablet Support**: Responsive for tablet screens
- **Desktop**: Full desktop experience
- **Touch Friendly**: Touch-optimized interactions

## 🔐 Security

- **Clerk Authentication**: Secure user management
- **Protected Routes**: Route-level protection
- **API Security**: Secure API communication
- **Environment Variables**: Secure configuration

## 🚀 Performance

- **Vite**: Lightning-fast development and builds
- **Code Splitting**: Automatic code splitting
- **Tree Shaking**: Dead code elimination
- **Optimized Assets**: Compressed images and assets

## 🐛 Troubleshooting

### Common Issues

1. **White Screen**: Check environment variables
2. **Authentication Errors**: Verify Clerk keys
3. **API Errors**: Check server connection
4. **Build Errors**: Clear node_modules and reinstall

### Debug Mode
```bash
# Enable debug logging
DEBUG=true npm run dev
```

---

**Built with ❤️ using React and Vite**