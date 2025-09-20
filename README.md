# Barter - Hyperlocal Skill Sharing Platform

<div align="center">
  <img src="public/image.png" alt="Powered by Bolt.new" width="100" height="100">
  
  **Built for Everyone**
  
  
  [![React](https://img.shields.io/badge/React-18.3.1-blue?style=for-the-badge&logo=react)](https://reactjs.org/)
  [![TypeScript](https://img.shields.io/badge/TypeScript-5.5.3-blue?style=for-the-badge&logo=typescript)](https://www.typescriptlang.org/)
  [![Supabase](https://img.shields.io/badge/Supabase-Backend-green?style=for-the-badge&logo=supabase)](https://supabase.com/)
  [![Tailwind CSS](https://img.shields.io/badge/Tailwind-3.4.1-blue?style=for-the-badge&logo=tailwindcss)](https://tailwindcss.com/)
  [![associated by Bolt.new](https://img.shields.io/badge/Powered%20by-Bolt.new-purple?style=for-the-badge)](https://bolt.new/)
</div>

## 🌟 Overview

Barter is a hyperlocal skill-sharing platform that connects neighbors to exchange skills, learn new talents, and build stronger communities. Whether you're offering guitar lessons or need help with gardening, Barter helps you find the right people in your immediate area.

### ✨ Key Features

- 🗺️ **Interactive Maps** - Discover skills visually on an interactive map
- 💬 **Real-time Messaging** - Chat instantly with skill providers and learners
- 📍 **Location-Based Discovery** - Find skills and people near you
- 🎯 **Smart Categorization** - Organized skill categories for easy browsing
- 🌙 **Dark/Light Theme** - Customizable user interface
- 📱 **Responsive Design** - Works seamlessly on all devices
- 🔒 **Secure Authentication** - Safe and secure user accounts
- ⚡ **Real-time Updates** - Live notifications and updates

## 🚀 Live Demo

Visit the live application: [https://golden-kulfi-db249d.netlify.app](https://golden-kulfi-db249d.netlify.app)

### Demo Credentials
- **Regular User**: Sign up with any email
- **Admin Access**: Contact developers for admin credentials

## 🛠️ Tech Stack

### Frontend
- **React 18.3.1** - Modern React with hooks
- **TypeScript** - Type-safe development
- **Vite** - Fast build tool and dev server
- **Tailwind CSS** - Utility-first styling
- **React Router** - Client-side routing
- **React Hook Form** - Form handling and validation
- **Lucide React** - Beautiful icons

### Backend & Database
- **Supabase** - Backend-as-a-Service
  - PostgreSQL database
  - Real-time subscriptions
  - Authentication & authorization
  - Row Level Security (RLS)

### Maps & Location
- **Leaflet** - Interactive maps
- **React Leaflet** - React map components
- **OpenStreetMap** - Map data
- **Nominatim API** - Geocoding service

## 📋 Prerequisites

Before you begin, ensure you have the following installed:
- **Node.js** (version 18.0 or higher)
- **npm** (version 8.0 or higher)
- **Git** for version control

## 🔧 Installation & Setup

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/barter-skill-sharing.git
cd barter-skill-sharing
```

### 2. Install Dependencies
```bash
npm install
```

### 3. Environment Configuration

Create a `.env` file in the root directory:
```bash
cp .env.example .env
```

Update the `.env` file with your Supabase credentials:
```env
VITE_SUPABASE_URL=your_supabase_project_url
VITE_SUPABASE_ANON_KEY=your_supabase_anon_key
```

### 4. Supabase Setup

1. **Create a Supabase Project**
   - Go to [supabase.com](https://supabase.com)
   - Create a new project
   - Note your project URL and anon key

2. **Database Setup**
   - The application will automatically create the necessary tables
   - Or run the migration files in `supabase/migrations/`

3. **Authentication Setup**
   - Enable email authentication in Supabase dashboard
   - Disable email confirmation for faster development

### 5. Start Development Server
```bash
npm run dev
```

The application will be available at `http://localhost:5173` or your respective local server

## 📁 Project Structure

```
barter-skill-sharing/
├── public/                 # Static assets
├── src/
│   ├── components/        # Reusable UI components
│   │   ├── BarterLogo.tsx
│   │   ├── Layout.tsx
│   │   ├── LocationSelector.tsx
│   │   ├── Navigation.tsx
│   │   ├── ProtectedRoute.tsx
│   │   └── SkillMap.tsx
│   ├── contexts/          # React Context providers
│   │   ├── AuthContext.tsx
│   │   └── ThemeContext.tsx
│   ├── lib/              # Utilities and configurations
│   │   └── supabase.ts
│   ├── pages/            # Route components
│   │   ├── Conversation.tsx
│   │   ├── Dashboard.tsx
│   │   ├── Landing.tsx
│   │   ├── Login.tsx
│   │   ├── Messages.tsx
│   │   ├── PostSkill.tsx
│   │   ├── Profile.tsx
│   │   ├── PublicProfile.tsx
│   │   ├── SearchSkills.tsx
│   │   ├── Signup.tsx
│   │   └── SkillDetail.tsx
│   ├── App.tsx           # Main app component
│   ├── main.tsx          # Entry point
│   └── index.css         # Global styles
├── supabase/
│   └── migrations/       # Database migrations
├── .env.example          # Environment variables template
├── package.json          # Dependencies and scripts
├── tailwind.config.js    # Tailwind configuration
├── tsconfig.json         # TypeScript configuration
├── vite.config.ts        # Vite configuration
├── README.md             # This file
└── STRUCTURE.md          # Detailed tech stack documentation
```

## 🎯 Available Scripts

```bash
# Start development server
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview

# Run linting
npm run lint
```

## 🗄️ Database Schema

### Core Tables
- **profiles** - User profile information
- **skills** - Skill offerings and requests
- **messages** - User communications

### Key Features
- Row Level Security (RLS) enabled on all tables
- Real-time subscriptions for live updates
- Geospatial data for location-based features
- Automatic profile creation on user signup

## 🔐 Authentication

The application uses Supabase authentication with:
- Email/password authentication
- Automatic profile creation
- Protected routes
- Admin user system
- Row-level security

### Admin Access
The application includes an admin system for testing and management purposes. Admin users have view-only access to demonstrate the platform's capabilities.

## 🗺️ Maps & Location

### Features
- Interactive maps using Leaflet
- Location-based skill discovery
- GPS integration for current location
- Address search with geocoding
- Privacy-focused approximate locations

### APIs Used
- **OpenStreetMap** - Map tiles and data
- **Nominatim** - Geocoding and reverse geocoding
- **Browser Geolocation API** - User location access

## 💬 Real-time Features

### Messaging System
- Real-time chat between users
- Message read receipts
- Conversation threading
- Skill-specific messaging context

### Live Updates
- New skill notifications
- Message delivery
- User status updates
- Real-time map updates

## 🎨 Theming

The application supports both light and dark themes:
- System preference detection
- Manual theme switching
- Persistent theme selection
- Tailwind CSS dark mode classes

## 📱 Responsive Design

- Mobile-first approach
- Tablet and desktop optimizations
- Touch-friendly interactions
- Accessible navigation patterns

## 🚀 Deployment

### Netlify Deployment
The application is configured for easy deployment to Netlify:

1. **Build Command**: `npm run build`
2. **Publish Directory**: `dist`
3. **Environment Variables**: Set in Netlify dashboard

### Manual Deployment
```bash
# Build the application
npm run build

# Deploy the dist/ folder to your hosting provider
```

## 🔧 Configuration

### Environment Variables
- `VITE_SUPABASE_URL` - Your Supabase project URL
- `VITE_SUPABASE_ANON_KEY` - Your Supabase anonymous key

### Supabase Configuration
- Enable email authentication
- Set up Row Level Security policies
- Configure real-time subscriptions
- Set up database triggers (optional)

## 🤝 Contributing

We welcome contributions! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Development Guidelines
- Follow TypeScript best practices
- Use Tailwind CSS for styling
- Write meaningful commit messages
- Test your changes thoroughly
- Update documentation as needed

## 🐛 Troubleshooting

### Common Issues

**1. Supabase Connection Issues**
- Verify your environment variables
- Check Supabase project status
- Ensure RLS policies are configured

**2. Map Not Loading**
- Check internet connection
- Verify Leaflet CSS is imported
- Check browser console for errors

**3. Location Access Denied**
- Enable location services in browser
- Use HTTPS for production
- Provide fallback location options

**4. Build Errors**
- Clear node_modules and reinstall
- Check TypeScript errors
- Verify all dependencies are installed

### Getting Help
- Check the [Issues](https://github.com/SimpleMan05/Barter/issues) page
- Review the [STRUCTURE.md](STRUCTURE.md) for technical details
- Contact the development team

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](GNU LICENSE) file for details.

## 🙏 Acknowledgments

- **Bolt.new** - For providing the development platform
- **Supabase** - For the backend infrastructure
- **OpenStreetMap** - For map data and services
- **Tailwind CSS** - For the utility-first CSS framework
- **React Community** - For the amazing ecosystem

## 📞 Contact

- **Project Link**: [https://github.com/SimpleMan05/Barter](GitHub Link)
- **Live Demo**: [https://golden-kulfi-db249d.netlify.app](https://golden-kulfi-db249d.netlify.app)
- **Built with**: [Bolt.new](https://bolt.new/)

---

<div align="center">
  <p>Built with ❤️ for the Bolt Hackathon</p>
  <p>
    <a href="https://bolt.new/">
      <img src="public/image.png" alt="Powered by Bolt.new" width="50" height="50">
    </a>
  </p>
</div>