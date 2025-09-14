# 🖥️ SuperTool Server - Express.js Backend

Robust Express.js backend for the SuperTool application, featuring AI integration, file processing, and secure authentication.

## 🚀 Quick Start

### Prerequisites
- Node.js (v18 or higher)
- npm or yarn
- PostgreSQL database (Neon recommended)
- API keys for external services

### Installation
```bash
npm install
```

### Development
```bash
npm run server
# Uses nodemon for auto-restart
```

### Production
```bash
npm start
```

## 🛠️ Tech Stack

- **Express.js 5** - Modern web framework
- **Node.js** - JavaScript runtime
- **Neon Database** - Serverless PostgreSQL
- **Clerk Express** - Authentication middleware
- **OpenAI API** - AI content generation
- **Clipdrop API** - Image generation
- **Cloudinary** - Cloud image storage
- **Multer** - File upload handling
- **Axios** - HTTP client
- **PDF Parse** - PDF processing
- **CORS** - Cross-origin resource sharing

## 📁 Project Structure

```
server/
├── controllers/         # Business logic
│   └── aiController.js  # AI-related operations
├── routes/             # API route definitions
│   ├── aiRoutes.js     # AI endpoints
│   └── userRoutes.js   # User endpoints
├── middlewares/        # Custom middleware
│   └── auth.js         # Authentication middleware
├── configs/            # Configuration files
│   ├── multer.js       # File upload config
│   ├── cloudinary.js   # Cloud storage config
│   └── db.js           # Database config
├── server.js           # Main server file
└── package.json
```

## 🔧 Environment Variables

Create a `.env` file in the server directory:

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

## 🚀 API Endpoints

### AI Routes (`/api/ai`)

#### Content Generation
- `POST /generate-article`
  - Generate articles using OpenAI GPT
  - Requires: `prompt`, `publish` (optional)
  - Returns: Generated article content

- `POST /generate-blog-title`
  - Generate blog titles
  - Requires: `prompt`
  - Returns: Array of blog titles

#### Image Processing
- `POST /generate-image`
  - Generate images using Clipdrop API
  - Requires: `prompt`, `publish` (optional)
  - Premium feature only
  - Returns: Generated image URL

- `POST /remove-image-background`
  - Remove background from uploaded image
  - Requires: `image` file upload
  - Returns: Processed image URL

- `POST /remove-image-object`
  - Remove objects from uploaded image
  - Requires: `image` file upload
  - Returns: Processed image URL

#### Document Analysis
- `POST /resume-review`
  - Analyze uploaded resume PDF
  - Requires: `resume` file upload
  - Returns: Analysis results

### User Routes (`/api/user`)

- `GET /get-user-creations`
  - Get user's personal creations
  - Returns: Array of user creations

- `GET /get-published-creations`
  - Get published community creations
  - Returns: Array of published creations

- `POST /toggle-like-creation`
  - Like/unlike a creation
  - Requires: `id`
  - Returns: Success status

## 🔐 Authentication & Security

### Clerk Integration
- **Middleware**: `clerkMiddleware()` for route protection
- **Auth Check**: `requireAuth()` for authenticated routes
- **User Context**: Access to user ID and plan information

### Security Features
- **CORS**: Cross-origin resource sharing
- **File Upload**: Secure file handling with Multer
- **API Keys**: Secure external service integration
- **Environment Variables**: Secure configuration

## 🗄️ Database Schema

### Creations Table
```sql
CREATE TABLE creations (
  id SERIAL PRIMARY KEY,
  user_id VARCHAR NOT NULL,
  prompt TEXT,
  content TEXT NOT NULL,
  type VARCHAR NOT NULL,
  publish BOOLEAN DEFAULT FALSE,
  created_at TIMESTAMP DEFAULT NOW()
);
```

## 🔄 File Processing

### Image Upload
- **Multer**: Handles multipart/form-data
- **Cloudinary**: Cloud storage and processing
- **Format Support**: JPG, PNG, GIF, WebP
- **Size Limits**: Configurable file size limits

### PDF Processing
- **PDF Parse**: Extract text from PDF files
- **Text Analysis**: AI-powered content analysis
- **Error Handling**: Graceful error management

## 🤖 AI Integration

### OpenAI GPT
- **Article Generation**: Long-form content creation
- **Blog Titles**: Creative title generation
- **Resume Analysis**: Document analysis and feedback

### Clipdrop API
- **Image Generation**: Text-to-image conversion
- **Background Removal**: AI-powered background removal
- **Object Removal**: Intelligent object removal

## 🚀 Deployment

### Vercel Deployment
```bash
vercel --prod
```

### Environment Setup
1. Set environment variables in Vercel dashboard
2. Configure database connection
3. Set up external API keys

### Database Migration
```sql
-- Run database migrations
-- Create tables and indexes
```

## 🔍 Error Handling

### Global Error Handler
- **Try-Catch**: Comprehensive error catching
- **Logging**: Detailed error logging
- **User-Friendly**: Meaningful error messages
- **Status Codes**: Proper HTTP status codes

### API Error Responses
```json
{
  "success": false,
  "message": "Error description"
}
```

## 📊 Performance

### Optimization
- **Connection Pooling**: Database connection management
- **Caching**: Response caching where appropriate
- **Compression**: Response compression
- **Rate Limiting**: API rate limiting

### Monitoring
- **Logging**: Comprehensive request/response logging
- **Error Tracking**: Error monitoring and alerting
- **Performance Metrics**: Response time tracking

## 🧪 Testing

### API Testing
```bash
# Test endpoints with curl or Postman
curl -X POST http://localhost:3000/api/ai/generate-article \
  -H "Authorization: Bearer YOUR_TOKEN" \
  -H "Content-Type: application/json" \
  -d '{"prompt": "Write about AI"}'
```

## 🐛 Troubleshooting

### Common Issues

1. **Database Connection**: Check DATABASE_URL
2. **API Keys**: Verify all external API keys
3. **File Upload**: Check Multer configuration
4. **CORS**: Verify CORS settings for frontend

### Debug Mode
```bash
# Enable debug logging
DEBUG=* npm run server
```

## 📈 Scaling

### Production Considerations
- **Load Balancing**: Multiple server instances
- **Database Scaling**: Read replicas
- **CDN**: Content delivery network
- **Monitoring**: Application performance monitoring

---

**Built with ❤️ using Express.js and Node.js**
