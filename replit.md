# Consultation Ifá - Online Consultation Platform

## Overview

This is a French-language web application for Ifá consultation services called "Terre des Mystères". The platform provides users with online spiritual consultations based on the traditional Yoruba Ifá divination system. The application features a clean, professional interface with spiritual/mystical styling elements including gradient backgrounds and golden accents that reflect the spiritual nature of the service.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
- **Technology Stack**: Static HTML/CSS/JavaScript with Flask backend
- **Styling Framework**: Custom CSS with comprehensive CSS variables system
- **Typography**: Google Fonts (Poppins family with weights 300-800)
- **Icons**: Font Awesome 6.4.0
- **Layout**: Single-page application with multiple static pages
- **Theme Support**: Light/dark mode toggle functionality
- **Responsive Design**: Mobile-first approach with fluid layouts

### Backend Architecture
- **Framework**: Flask (Python web framework)
- **Server**: Development server running on port 5000
- **Session Management**: Flask sessions with environment-based secret key
- **Static File Serving**: Direct file serving for HTML, CSS, and assets
- **Deployment**: Configured for host '0.0.0.0' with debug mode enabled

### Data Storage Solutions
- **Current State**: No database implementation detected
- **Architecture**: Stateless application serving static content
- **Future Consideration**: May require database integration for consultation requests, user data, or form submissions

## Key Components

### Design System
- **Color Palette**: 
  - Primary: Blue gradient (#667eea to #764ba2)
  - Accent: Gold tones (#d4af37, #f7e98e)
  - Neutral: Grays for text and backgrounds
- **Typography Scale**: Poppins font family with comprehensive weight range
- **Shadow System**: Multi-layered shadows for depth and elevation
- **Animation**: Smooth transitions with cubic-bezier easing
- **Theme System**: CSS custom properties for light/dark mode switching

### Page Structure
- **index.html**: Main consultation request page
- **about.html**: Information about Ifá divination system
- **merci.html**: Thank you page after form submission
- **Shared Styling**: Consistent design system across all pages

### User Interface Elements
- **Gradient Backgrounds**: Spiritual blue-purple gradients
- **Glass-morphism Effects**: Backdrop blur and transparency
- **Smooth Animations**: CSS transitions for interactive elements
- **Responsive Cards**: Flexible container system
- **Form Elements**: Styled input fields and buttons

## Data Flow

### Current Implementation
1. User visits main page (index.html)
2. Flask serves static HTML files directly
3. All styling and interactivity handled client-side
4. Navigation between pages via direct URL access

### Expected User Journey
1. User lands on consultation request form
2. Fills out consultation details
3. Submits form (backend processing needed)
4. Redirects to thank you page
5. Can access additional information via about page

## External Dependencies

### Frontend Dependencies
- **Google Fonts**: Poppins font family loading
- **Font Awesome**: Icon library (v6.4.0) via CDN
- **No JavaScript Frameworks**: Pure vanilla JS implementation

### Backend Dependencies
- **Flask**: Web framework for Python
- **Python Standard Library**: OS module for environment variables
- **No Database ORM**: Currently no data persistence layer

### CDN Resources
- All external resources loaded via HTTPS CDNs
- Font and icon loading optimized with display=swap

## Deployment Strategy

### Current Configuration
- **Development Setup**: Flask development server
- **Host Configuration**: Configured for 0.0.0.0 (all interfaces)
- **Port**: 5000 (standard Flask development port)
- **Debug Mode**: Enabled for development
- **Session Security**: Environment variable for secret key

### Production Considerations
- **Static Assets**: Currently served through Flask (should be CDN/static server in production)
- **Security**: Session secret should be properly configured for production
- **WSGI Server**: Will need production WSGI server (Gunicorn, uWSGI)
- **Database**: No current database dependency simplifies deployment

## Recent Changes

### July 19, 2025
- **REMOVED EMAIL SECTION COMPLETELY** from consultation form for Fiverr usage
- Cleaned up JavaScript validation code removing email-related functions
- Optimized form for Fiverr client data collection (payment handled by Fiverr platform)
- Form now collects only essential consultation information: name, birth details, location, mother's name, consultation type
- **UPDATED LOGO**: Replaced with new Eye of Horus/Ifá logo (PNG format with sacred geometric patterns)
- Enhanced logo styling with multi-layered shadows and hover effects matching the green/gold theme
- Updated all pages (index, about, merci) with new logo and improved visual integration
- Maintained professional design and all modern features (gradients, animations, multilingual support)
- Confirmed form works perfectly for micro-service platforms like Fiverr

### Missing Components for Full Functionality
- **Form Processing**: Backend logic to handle consultation requests
- **Email Integration**: To send consultation requests to terredesmysteres@gmail.com
- **Database Layer**: For storing consultation history or user data
- **Admin Panel**: For managing consultations and responses

*Note: Payment processing not needed as this form is designed for Fiverr usage where payment is handled by the platform*