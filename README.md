# College Cosmos Home 🚌

A modern, real-time college bus tracking and management system built with Next.js and Node.js.

## 🌟 Features

- **Real-time Bus Tracking** - Live GPS tracking of college buses
- **Multi-role Support** - Students, Parents, Drivers, and Admins
- **Smart Notifications** - Push notifications for bus arrivals and delays
- **Route Management** - Dynamic route planning and optimization
- **User Authentication** - Secure login system with role-based access
- **Responsive Design** - Works seamlessly on all devices

## 🚀 Quick Start

### Prerequisites

- Node.js 18+ 
- npm or yarn
- MongoDB (for backend)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/college-cosmos-home.git
   cd college-cosmos-home
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Set up environment variables**
   ```bash
   cp .env.example .env.local
   ```
   Fill in your environment variables in `.env.local`

4. **Run the development server**
   ```bash
   npm run dev
   ```

5. **Open your browser**
   Navigate to [http://localhost:3000](http://localhost:3000)

## 🏗️ Tech Stack

- **Frontend**: Next.js 14, React, Tailwind CSS, Framer Motion
- **Backend**: Node.js, Express.js
- **Database**: MongoDB
- **Authentication**: JWT
- **Real-time**: Socket.io
- **Maps**: Google Maps API / Mapbox
- **Notifications**: Push API

## 📱 User Roles

### 👨‍🎓 Students
- Track bus location in real-time
- Get arrival notifications
- View route schedules
- Report issues

### 👨‍👩‍👧‍👦 Parents
- Monitor child's commute
- Receive safety notifications
- View trip history
- Emergency contacts

### 🚌 Drivers
- Update bus status
- Manage passenger lists
- Report delays/issues
- Navigation assistance

### 👨‍💼 Admins
- System overview dashboard
- Manage routes and schedules
- User management
- Analytics and reports

## 🛠️ Development

### Project Structure
```
college-cosmos-home/
├── components/          # Reusable UI components
├── pages/              # Next.js pages
├── lib/                # Utility functions
├── styles/             # CSS and styling
├── public/             # Static assets
├── server/             # Backend API (if included)
└── docs/               # Documentation
```

### Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run start` - Start production server
- `npm run lint` - Run ESLint
- `npm run test` - Run tests

## 🤝 Contributing

We welcome contributions! Please see our [Contributing Guidelines](CONTRIBUTING.md) for details.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🆘 Support

- 📧 Email: support@collegecosmos.com
- 💬 Discord: [Join our community](https://discord.gg/collegecosmos)
- 📖 Documentation: [docs.collegecosmos.com](https://docs.collegecosmos.com)

## 🙏 Acknowledgments

- Thanks to all contributors who have helped shape this project
- Special thanks to the open-source community
- Icons by [Lucide React](https://lucide.dev/)

## 📊 Project Status

![Build Status](https://img.shields.io/badge/build-passing-brightgreen)
![Version](https://img.shields.io/badge/version-1.0.0-blue)
![License](https://img.shields.io/badge/license-MIT-green)
![Contributors](https://img.shields.io/badge/contributors-welcome-orange)

---

Made with ❤️ for college communities worldwide