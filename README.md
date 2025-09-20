# Naomi's Kuhingira Launch - Save the Date Website

A beautiful, responsive "Save the Date" website for Naomi's Kuhingira Launch celebration, featuring elegant design, real-time countdown, and seamless calendar integration.

## 🎉 Event Details

- **Event**: Naomi's Kuhingira Launch
- **Date**: October 4, 2025
- **Time**: 2:00 PM
- **Venue**: Afrique Suites Hotel, Mutungu Gardens
- **Hashtag**: #UNFORGETABLEMEMORIES

## ✨ Features

### 🎨 Design & User Experience
- **Elegant Typography**: Combination of Great Vibes (script), Playfair Display (serif), and Inter (sans-serif)
- **Warm Color Palette**: Cream, beige, and brown tones for a timeless, sophisticated look
- **Responsive Design**: Optimized for all devices from mobile phones to desktop computers
- **Magazine-Style Layout**: Professional, editorial-inspired design

### ⏰ Interactive Elements
- **Real-Time Countdown Timer**: Live countdown to the event with days, hours, minutes, and seconds
- **Smooth Animations**: Hover effects and transitions for enhanced user experience
- **Loading States**: Visual feedback while content loads

### 📅 Calendar Integration
- **Google Calendar**: Direct integration with pre-filled event details using official Google branding
- **Apple Calendar**: .ics file download for Apple Calendar, Outlook, and other calendar apps with official Apple styling
- **Brand-Accurate Logos**: Authentic Google and Apple calendar logos for professional appearance
- **Mobile Optimized**: Specific instructions for different mobile platforms
- **Accessibility**: Proper ARIA labels and keyboard navigation support

### 📱 Mobile Optimization
- **Touch-Friendly**: Minimum 48px touch targets for all interactive elements
- **Responsive Layout**: Adapts seamlessly from mobile to desktop
- **Fast Loading**: Optimized for mobile networks
- **Cross-Platform**: Works on iOS, Android, and all modern browsers

## 🛠 Technical Stack

### Frontend Technologies
- **HTML5**: Semantic markup with proper meta tags
- **CSS3**: Custom styles with Flexbox and Grid layouts
- **JavaScript (ES6+)**: Modern JavaScript for interactive features
- **Tailwind CSS**: Utility-first CSS framework for rapid styling

### External Dependencies
- **Google Fonts**: Great Vibes, Playfair Display, Inter, and Merriweather
- **Tailwind CSS CDN**: For responsive design utilities

### Browser Support
- ✅ Chrome (latest)
- ✅ Firefox (latest)
- ✅ Safari (latest)
- ✅ Edge (latest)
- ✅ Mobile browsers (iOS Safari, Chrome Mobile)

## 📁 Project Structure

```
naomi_savedate/
├── index.html          # Main HTML file with complete website
├── assets/             # Static assets directory
│   ├── google-calendar-logo.svg  # Official Google Calendar logo
│   └── apple-calendar-logo.svg   # Official Apple Calendar logo
├── README.md           # Project documentation (this file)
├── .gitignore         # Git ignore rules
├── TEST_DATA.md       # Comprehensive testing documentation
└── .qodo/             # Development tools directory
```

## 🚀 Getting Started

### Prerequisites
- A modern web browser
- Basic understanding of HTML/CSS/JavaScript (for customization)

### Installation & Setup

1. **Clone or Download the Repository**
   ```bash
   git clone <repository-url>
   cd naomi_savedate
   ```

2. **Open the Website**
   - Simply open `index.html` in any modern web browser
   - Or serve it using a local web server:
   ```bash
   # Using Python 3
   python -m http.server 8000
   
   # Using Node.js (if you have http-server installed)
   npx http-server
   
   # Using PHP
   php -S localhost:8000
   ```

3. **View the Website**
   - Open your browser and navigate to the file or local server
   - The website will be fully functional immediately

## 🧪 Testing Guide

### Functionality Testing

#### 1. Countdown Timer Testing
- **Test Case**: Verify countdown displays correctly
- **Steps**: 
  1. Open the website
  2. Check that countdown shows days, hours, minutes, seconds
  3. Wait 1 minute to verify seconds are updating
- **Expected Result**: Timer updates every second with correct values

#### 2. Google Calendar Integration Testing
- **Test Case**: Google Calendar button works on all devices
- **Steps**:
  1. Click "Google Calendar" button
  2. Verify it opens Google Calendar with pre-filled event details
  3. Check event title: "Naomi's Kuhingira Launch"
  4. Verify date: October 4, 2025
  5. Verify time: 12:00 PM - 3:00 PM UTC (3:00 PM - 6:00 PM local)
- **Expected Result**: Google Calendar opens with correct event details

#### 3. Apple/Outlook Calendar Testing
- **Test Case**: .ics file download works correctly
- **Steps**:
  1. Click "Apple & Outlook" button
  2. Verify .ics file downloads
  3. Open file with calendar application
  4. Check all event details are correct
- **Expected Result**: Calendar app opens with event details

#### 4. Mobile Responsiveness Testing
- **Test Case**: Website works on mobile devices
- **Steps**:
  1. Open website on mobile device or use browser dev tools
  2. Test portrait and landscape orientations
  3. Verify all text is readable
  4. Check that buttons are easily tappable
  5. Test calendar integration on mobile
- **Expected Result**: Website is fully functional and visually appealing on mobile

#### 5. Cross-Browser Testing
- **Test Case**: Website works across different browsers
- **Browsers to Test**: Chrome, Firefox, Safari, Edge
- **Steps**:
  1. Open website in each browser
  2. Test all functionality
  3. Verify visual consistency
- **Expected Result**: Consistent experience across all browsers

### Test Data & Scenarios

#### Sample Event Details for Testing
```
Event Name: Naomi's Kuhingira Launch
Date: October 4, 2025
Time: 3:00 PM (15:00)
Duration: 3 hours
Location: Afrique Suites Hotel, Mutungu Gardens, Ring Road
Description: Join us to celebrate with Naomi before her Kuhingira! Come laugh, eat, dine, mingle and contribute. Your presence will be highly appreciated. #UNFORGETABLEMEMORIES
```

#### Calendar Integration Test URLs
- **Google Calendar**: Verify URL contains proper encoding of event details
- **ICS File**: Verify downloaded file contains all required VEVENT properties

## 📱 Mobile Optimization Features

### Touch Interactions
- **Minimum Touch Target Size**: 48px for all interactive elements
- **Touch Feedback**: Visual feedback on button presses
- **Gesture Support**: Proper handling of touch events

### Performance Optimizations
- **Optimized Images**: Efficient SVG icons for fast loading
- **Minimal Dependencies**: Only essential external resources
- **Compressed Assets**: Optimized for mobile networks

### Mobile-Specific Features
- **Viewport Meta Tag**: Proper mobile viewport configuration
- **Touch-Friendly Navigation**: Easy-to-use interface on small screens
- **Platform-Specific Instructions**: Tailored guidance for iOS and Android users

## 🎨 Customization Guide

### Changing Event Details

1. **Update Event Information**
   - Edit the event details in the HTML (date, time, venue)
   - Update the countdown target date in JavaScript
   - Modify calendar integration URLs with new details

2. **Customize Colors**
   - Modify CSS custom properties for brand colors
   - Update Tailwind classes for consistent theming

3. **Change Fonts**
   - Replace Google Fonts links in the `<head>` section
   - Update CSS font-family declarations

### Adding New Features

1. **RSVP Functionality**
   - Add form elements for guest responses
   - Integrate with backend service or email

2. **Photo Gallery**
   - Add image gallery section
   - Implement lightbox functionality

3. **Social Media Integration**
   - Add social sharing buttons
   - Integrate with social media APIs

## 🔧 Development Notes

### Code Organization
- **HTML**: Semantic structure with comprehensive comments
- **CSS**: Organized by sections with clear naming conventions
- **JavaScript**: Modular functions with error handling

### Performance Considerations
- **Lazy Loading**: Images and non-critical resources
- **Minification**: Consider minifying CSS/JS for production
- **CDN Usage**: External resources loaded from CDNs

### Accessibility Features
- **ARIA Labels**: Proper labeling for screen readers
- **Keyboard Navigation**: Full keyboard accessibility
- **Color Contrast**: WCAG compliant color combinations
- **Semantic HTML**: Proper heading hierarchy and structure

## 🚀 Deployment Options

### Static Hosting Services
- **Netlify**: Drag and drop deployment
- **Vercel**: Git-based deployment
- **GitHub Pages**: Free hosting for public repositories
- **Firebase Hosting**: Google's hosting platform

### Traditional Web Hosting
- Upload files to any web server
- Ensure HTTPS is enabled for security
- Configure proper MIME types for .ics files

## 📞 Support & Contact

### Event Organizers
- **Team**: krapht256
- **Contact**: [Add contact information]

### Technical Support
- **Issues**: Report bugs or feature requests
- **Documentation**: Refer to this README for guidance
- **Updates**: Check for updates and improvements

## 📄 License

This project is created for Naomi's Kuhingira Launch event. Please respect the personal nature of this content and use responsibly.

## 🙏 Acknowledgments

- **Design Inspiration**: Magazine-style layouts and elegant typography
- **Technical Stack**: Tailwind CSS, Google Fonts, and modern web standards
- **Testing**: Cross-platform and cross-browser compatibility
- **Accessibility**: WCAG guidelines and best practices

---

**Made with ❤️ for Naomi's special day**

*Last updated: December 2024*