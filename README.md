# Ransomware Simulation & Defense Toolkit (RSDT) - Frontend

A professional, secure, and responsive frontend application for the Ransomware Simulation & Defense Toolkit. This application provides a comprehensive dashboard for managing ransomware simulations, monitoring security alerts, and analyzing defense effectiveness.

## 🚀 Features

### Core Functionality
- **Security Dashboard**: Real-time overview of security posture with key metrics and visualizations
- **Simulation Management**: Create, monitor, and control ransomware attack simulations
- **Alert System**: Comprehensive security alert monitoring and incident response
- **System Monitoring**: Real-time system health and performance metrics
- **Reports & Analytics**: Security reporting and data visualization
- **Training Center**: Cybersecurity training modules and exercises
- **User Management**: User account and permission management
- **Settings**: System configuration and preferences

### Security Features
- **Input Validation & Sanitization**: All user inputs are validated and sanitized to prevent XSS and injection attacks
- **Content Security Policy (CSP)**: Strict CSP implementation to mitigate security risks
- **Rate Limiting**: Client-side rate limiting to prevent abuse
- **Secure Storage**: Encrypted local storage with TTL for sensitive data
- **HTTPS Enforcement**: Application designed to work only over HTTPS in production
- **Security Headers**: Implementation of security best practices and headers

### UI/UX Features
- **Responsive Design**: Optimized for desktop, tablet, and mobile devices
- **Professional Interface**: Modern, clean design with cybersecurity aesthetics
- **Interactive Charts**: Real-time data visualization using Recharts
- **Dark Theme**: Professional dark sidebar with light content areas
- **Accessibility**: WCAG compliant design with proper ARIA attributes
- **Smooth Animations**: Micro-interactions and transitions for better UX

## 🛠 Technology Stack

- **React 18**: Modern React with hooks and functional components
- **Vite**: Fast build tool and development server
- **Tailwind CSS**: Utility-first CSS framework for styling
- **shadcn/ui**: High-quality, accessible UI components
- **Lucide Icons**: Beautiful, customizable icons
- **Recharts**: Composable charting library for React
- **JavaScript (ES6+)**: Modern JavaScript features

## 📁 Project Structure

```
rsdt-frontend/
├── public/                 # Static assets
├── src/
│   ├── assets/            # Images, logos, and static files
│   ├── components/        # React components
│   │   ├── ui/           # shadcn/ui components
│   │   ├── Sidebar.jsx   # Navigation sidebar
│   │   ├── Header.jsx    # Top header with search and notifications
│   │   ├── Dashboard.jsx # Main dashboard component
│   │   ├── Simulations.jsx # Simulation management
│   │   ├── Alerts.jsx    # Security alerts interface
│   │   └── SecurityWrapper.jsx # Security enhancement wrapper
│   ├── utils/
│   │   └── security.js   # Security utility functions
│   ├── App.jsx           # Main application component
│   ├── App.css           # Application styles
│   └── main.jsx          # Application entry point
├── components.json        # shadcn/ui configuration
├── package.json          # Dependencies and scripts
└── README.md            # This file
```

## 🚦 Getting Started

### Prerequisites
- Node.js 18+ 
- npm or pnpm

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd rsdt-frontend
   ```

2. **Install dependencies**
   ```bash
   npm install
   # or
   pnpm install
   ```

3. **Start development server**
   ```bash
   npm run dev
   # or
   pnpm run dev
   ```

4. **Open in browser**
   Navigate to `http://localhost:5173`

### Build for Production

```bash
npm run build
# or
pnpm run build
```

The built files will be in the `dist/` directory.

## 🔒 Security Implementation

### Frontend Security Measures

1. **Input Validation**
   - All user inputs are validated and sanitized
   - XSS prevention through HTML escaping
   - SQL injection prevention for search inputs

2. **Content Security Policy**
   - Strict CSP headers to prevent code injection
   - Whitelisted sources for scripts, styles, and images

3. **Rate Limiting**
   - Client-side rate limiting for forms and actions
   - Configurable limits based on action type

4. **Secure Storage**
   - Encrypted local storage with TTL
   - No sensitive data stored in browser storage

5. **Error Handling**
   - Graceful error handling without information disclosure
   - Secure error messages for users

### Security Best Practices

- HTTPS-only operation in production
- Regular dependency updates and vulnerability scanning
- Minimal attack surface with only necessary scripts
- Secure authentication token handling
- Protection against common web vulnerabilities

## 🎨 Design System

### Color Palette
- **Primary**: Dark blues and grays for professional appearance
- **Accent**: Emerald green for positive actions and success states
- **Alert Colors**: Red (critical), Orange (high), Yellow (medium), Blue (info)
- **Background**: Light gray (#f8fafc) for main content areas

### Typography
- **Font Family**: System fonts with fallbacks for optimal performance
- **Hierarchy**: Clear heading structure with consistent sizing
- **Readability**: High contrast ratios for accessibility

### Components
- **Cards**: Clean, bordered containers for content sections
- **Buttons**: Consistent styling with hover states and variants
- **Forms**: Accessible form controls with validation feedback
- **Charts**: Professional data visualization with consistent theming

## 📊 Dashboard Features

### Key Metrics
- Active Simulations count with trend indicators
- Critical Alerts with severity breakdown
- System Health percentage and status
- Defense Score with improvement tracking

### Visualizations
- **Threat Detection Trends**: Line chart showing threats over time
- **Simulation Types Distribution**: Pie chart of attack types
- **System Status**: Progress bars for resource usage
- **Recent Alerts**: Real-time alert feed with severity indicators

### Interactive Elements
- Clickable navigation with active state indicators
- Searchable and filterable data tables
- Expandable alert details with recommended actions
- Real-time updates and progress tracking

## 🔧 Configuration

### Environment Variables
```env
NODE_ENV=production          # Environment mode
VITE_API_BASE_URL=          # Backend API URL
VITE_ENABLE_SECURITY=true   # Enable security features
```

### Security Configuration
The application includes configurable security settings in `src/utils/security.js`:
- Rate limiting thresholds
- Input validation rules
- Storage encryption settings
- CSP policy definitions

## 🧪 Testing

### Manual Testing Checklist
- [ ] Navigation between all sections works correctly
- [ ] Responsive design on different screen sizes
- [ ] Form validation and error handling
- [ ] Chart rendering and data visualization
- [ ] Search and filter functionality
- [ ] Security features (rate limiting, input validation)

### Browser Compatibility
- Chrome 90+
- Firefox 88+
- Safari 14+
- Edge 90+

## 🚀 Deployment

### Production Deployment
1. Build the application: `npm run build`
2. Deploy the `dist/` folder to your web server
3. Configure HTTPS and security headers
4. Set up proper CSP headers on the server
5. Configure backend API endpoints

### Security Considerations for Production
- Ensure HTTPS is enforced
- Configure proper security headers on the server
- Set up monitoring and logging
- Regular security updates and dependency scanning
- Implement proper authentication and authorization

## 📈 Performance

### Optimization Features
- Code splitting and lazy loading
- Optimized bundle size with tree shaking
- Efficient re-rendering with React optimization
- Compressed assets and images
- CDN-ready static assets

### Performance Metrics
- First Contentful Paint: < 1.5s
- Largest Contentful Paint: < 2.5s
- Cumulative Layout Shift: < 0.1
- First Input Delay: < 100ms

## 🤝 Contributing

### Development Guidelines
1. Follow React best practices and hooks patterns
2. Use TypeScript for new components (if migrating)
3. Implement proper error boundaries
4. Write accessible components with ARIA attributes
5. Follow the established design system

### Code Style
- Use ESLint and Prettier for code formatting
- Follow component naming conventions
- Implement proper prop validation
- Use semantic HTML elements

## 📝 License

This project is part of the Ransomware Simulation & Defense Toolkit (RSDT) and is intended for educational and security training purposes.

## 👥 Team

- **Binyam Bharu** - Project Manager (bharubinyam@gmail.com)
- **Adisu Alke** - Backend Developer (alkeadis09@gmail.com)
- **Amanuel Nebiyu** - Frontend Developer (amanuelnebiyu00@gmail.com)
- **Niya Muhammad** - Database Administrator (niyakedir68@gmail.com)

## 📞 Support

For technical support or questions about the RSDT frontend:
- Create an issue in the project repository
- Contact the development team
- Refer to the documentation and security guidelines

---

**Note**: This application is designed for cybersecurity training and simulation purposes. Always follow your organization's security policies and guidelines when deploying and using this toolkit.

