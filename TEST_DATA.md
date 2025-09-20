# Test Data & Testing Scenarios
## Naomi's Kuhingira Launch Website

This document provides comprehensive test data and testing scenarios for all functionality of the website.

## 📅 Event Test Data

### Primary Event Information
```
Event Name: Naomi's Kuhingira Launch
Event Type: Pre-wedding celebration
Date: October 4, 2025
Time: 3:00 PM (15:00 local time)
Duration: 3 hours (3:00 PM - 6:00 PM)
Venue: Afrique Suites Hotel
Address: Mutungu Gardens, Ring Road
City: [Location City]
Country: [Country]
Hashtag: #UNFORGETABLEMEMORIES
```

### Calendar Integration Test Data

#### Google Calendar URL Parameters
```
Base URL: https://www.google.com/calendar/render
Parameters:
- action=TEMPLATE
- text=Naomi's%20Kuhingira%20Launch
- dates=20251004T120000Z/20251004T150000Z
- details=Join%20us%20to%20celebrate%20with%20Naomi%20before%20her%20Kuhingira!%20Come%20laugh,%20eat,%20dine,%20mingle%20and%20contribute.%20Your%20presence%20will%20be%20highly%20appreciated.%20%23UNFORGETABLEMEMORIES
- location=Afrique%20Suites%20Hotel,%20Mutungu%20Gardens,%20Ring%20Road
```

#### ICS File Content (Apple/Outlook)
```
BEGIN:VCALENDAR
VERSION:2.0
PRODID:-//krapht256//Naomi Kuhingira Launch//EN
BEGIN:VEVENT
UID:naomi-kuhingira-launch-2025@krapht256.com
DTSTAMP:20241201T000000Z
ORGANIZER;CN=Naomi:MAILTO:naomi@krapht256.com
SUMMARY:Naomi's Kuhingira Launch
DTSTART:20251004T120000Z
DTEND:20251004T150000Z
LOCATION:Afrique Suites Hotel, Mutungu Gardens, Ring Road
DESCRIPTION:Join us to celebrate with Naomi before her Kuhingira! Come laugh, eat, dine, mingle and contribute. Your presence will be highly appreciated. #UNFORGETABLEMEMORIES
STATUS:CONFIRMED
SEQUENCE:0
END:VEVENT
END:VCALENDAR
```

## 🧪 Functional Testing Scenarios

### 1. Countdown Timer Testing

#### Test Case 1.1: Initial Load
- **Objective**: Verify countdown displays correctly on page load
- **Steps**:
  1. Open index.html in browser
  2. Observe countdown section
  3. Wait 5 seconds
- **Expected Results**:
  - Countdown shows days, hours, minutes, seconds
  - Numbers update every second
  - Format is zero-padded (e.g., "05" not "5")
  - Loading animation disappears after first update

#### Test Case 1.2: Countdown Accuracy
- **Objective**: Verify countdown calculates time correctly
- **Test Data**: 
  - Target: October 4, 2025, 3:00 PM
  - Test Date: December 1, 2024, 12:00 PM
- **Expected Calculation**:
  - Days: ~307 days (varies by test date)
  - Hours: Should decrease by 1 every hour
  - Minutes: Should reset to 59 every hour
  - Seconds: Should reset to 59 every minute

#### Test Case 1.3: Event Day Behavior
- **Objective**: Test countdown when event date arrives
- **Steps**:
  1. Temporarily change countdown date to current time + 5 seconds
  2. Wait for countdown to reach zero
- **Expected Results**:
  - Countdown stops at zero
  - Message displays: "The celebration has begun! 🎉"

### 2. Calendar Integration Testing

#### Test Case 2.1: Google Calendar Button
- **Objective**: Verify Google Calendar integration works
- **Steps**:
  1. Click "Google Calendar" button
  2. Verify new tab/window opens
  3. Check Google Calendar interface loads
  4. Verify event details are pre-filled
- **Expected Results**:
  - Google Calendar opens in new tab
  - Event title: "Naomi's Kuhingira Launch"
  - Date: October 4, 2025
  - Time: 12:00 PM - 3:00 PM UTC
  - Location: "Afrique Suites Hotel, Mutungu Gardens, Ring Road"
  - Description includes hashtag and event details

#### Test Case 2.2: Apple/Outlook Calendar Button
- **Objective**: Verify .ics file download and import
- **Steps**:
  1. Click "Apple & Outlook" button
  2. Verify file downloads
  3. Open downloaded .ics file
  4. Check calendar app opens with event
- **Expected Results**:
  - File "naomi-kuhingira-launch.ics" downloads
  - File size: ~500-800 bytes
  - Calendar app opens with event details
  - All event information matches test data

#### Test Case 2.3: Mobile Calendar Integration
- **Platform**: iOS Safari
- **Steps**:
  1. Open website on iPhone
  2. Tap "Apple & Outlook" button
  3. Choose "Add to Calendar" when prompted
- **Expected Results**:
  - iOS Calendar app opens
  - Event is added to default calendar
  - All details are correct

- **Platform**: Android Chrome
- **Steps**:
  1. Open website on Android device
  2. Tap "Google Calendar" button
  3. Sign in if required
- **Expected Results**:
  - Google Calendar app opens
  - Event creation screen appears
  - All details are pre-filled

### 3. Responsive Design Testing

#### Test Case 3.1: Mobile Portrait (320px - 480px)
- **Devices**: iPhone SE, iPhone 12 Mini
- **Test Points**:
  - Header text is readable
  - Countdown numbers are appropriately sized
  - Calendar buttons stack vertically
  - Touch targets are minimum 48px
  - No horizontal scrolling

#### Test Case 3.2: Mobile Landscape (480px - 768px)
- **Devices**: iPhone 12, Samsung Galaxy S21
- **Test Points**:
  - Layout adapts to landscape orientation
  - Content remains centered
  - Calendar buttons may display side-by-side
  - Text remains readable

#### Test Case 3.3: Tablet (768px - 1024px)
- **Devices**: iPad, Android tablets
- **Test Points**:
  - Two-column story layout appears
  - Event details display in 3-column grid
  - Calendar buttons display side-by-side
  - Proper spacing and typography

#### Test Case 3.4: Desktop (1024px+)
- **Devices**: Laptops, desktop computers
- **Test Points**:
  - Full layout with optimal spacing
  - Hover effects work on calendar buttons
  - Typography is crisp and readable
  - Maximum width constraint (max-w-4xl) is respected

### 4. Cross-Browser Testing

#### Test Case 4.1: Chrome (Latest)
- **Features to Test**:
  - CSS Grid and Flexbox layouts
  - Custom fonts loading
  - JavaScript countdown functionality
  - Calendar integration

#### Test Case 4.2: Firefox (Latest)
- **Features to Test**:
  - CSS compatibility
  - Font rendering
  - JavaScript execution
  - Download functionality for .ics files

#### Test Case 4.3: Safari (Latest)
- **Features to Test**:
  - WebKit-specific CSS properties
  - Font loading and rendering
  - Touch events on mobile
  - Calendar integration with iOS

#### Test Case 4.4: Edge (Latest)
- **Features to Test**:
  - Chromium-based compatibility
  - Windows-specific behaviors
  - Outlook calendar integration

### 5. Performance Testing

#### Test Case 5.1: Page Load Speed
- **Metrics to Measure**:
  - First Contentful Paint (FCP): < 1.5s
  - Largest Contentful Paint (LCP): < 2.5s
  - Cumulative Layout Shift (CLS): < 0.1
  - First Input Delay (FID): < 100ms

#### Test Case 5.2: Mobile Performance
- **Test Conditions**:
  - Slow 3G network simulation
  - Low-end mobile device simulation
- **Expected Results**:
  - Page loads within 3 seconds
  - Countdown starts within 2 seconds
  - No layout shifts during loading

### 6. Accessibility Testing

#### Test Case 6.1: Screen Reader Compatibility
- **Tools**: NVDA, JAWS, VoiceOver
- **Test Points**:
  - All content is readable by screen readers
  - Calendar buttons have proper ARIA labels
  - Heading hierarchy is logical (h1 → h2 → h3 → h4)
  - Images have appropriate alt text

#### Test Case 6.2: Keyboard Navigation
- **Test Points**:
  - Tab order is logical
  - Calendar buttons are focusable
  - Enter/Space keys activate buttons
  - Focus indicators are visible

#### Test Case 6.3: Color Contrast
- **Test Points**:
  - Text meets WCAG AA standards (4.5:1 ratio)
  - Interactive elements have sufficient contrast
  - Color is not the only way to convey information

### 7. Error Handling Testing

#### Test Case 7.1: Network Connectivity
- **Scenario**: Poor or no internet connection
- **Steps**:
  1. Load page with slow connection
  2. Disconnect internet after page loads
- **Expected Results**:
  - Page loads gracefully with slow connection
  - Countdown continues to work offline
  - Calendar buttons show appropriate error messages

#### Test Case 7.2: JavaScript Disabled
- **Steps**:
  1. Disable JavaScript in browser
  2. Reload page
- **Expected Results**:
  - Static content displays correctly
  - Calendar links still work (basic functionality)
  - Countdown shows placeholder text

## 📊 Test Data Validation

### Valid Input Data
```
Date Format: YYYY-MM-DD
Time Format: HH:MM (24-hour)
URL Encoding: Proper percent encoding for special characters
ICS Format: Valid iCalendar format (RFC 5545)
```

### Edge Cases to Test
```
- Leap year calculations (2024, 2028)
- Daylight saving time transitions
- Different time zones
- Very long event descriptions
- Special characters in event details
- Unicode characters in names/locations
```

### Browser-Specific Test Data
```
Chrome: Test with latest stable and beta versions
Firefox: Test with ESR and latest versions
Safari: Test on macOS and iOS versions
Edge: Test on Windows 10 and 11
```

## 🔍 Manual Testing Checklist

### Pre-Testing Setup
- [ ] Clear browser cache
- [ ] Disable browser extensions
- [ ] Set system date/time correctly
- [ ] Ensure stable internet connection

### Visual Testing
- [ ] All fonts load correctly
- [ ] Colors match design specifications
- [ ] Images and icons display properly
- [ ] Layout is consistent across sections
- [ ] No text overflow or truncation

### Functional Testing
- [ ] Countdown timer updates every second
- [ ] Google Calendar button opens correct URL
- [ ] Apple Calendar button downloads .ics file
- [ ] Mobile instructions are clear and accurate
- [ ] All links open in appropriate targets

### Responsive Testing
- [ ] Test on actual mobile devices
- [ ] Verify touch interactions work
- [ ] Check orientation changes
- [ ] Validate on different screen sizes
- [ ] Ensure no horizontal scrolling

### Final Validation
- [ ] All event details are accurate
- [ ] Contact information is correct
- [ ] Hashtag is properly formatted
- [ ] No broken links or missing resources
- [ ] Performance is acceptable on all devices

## 📝 Test Results Documentation

### Test Report Template
```
Test Date: [Date]
Tester: [Name]
Browser: [Browser and Version]
Device: [Device/OS]
Test Case: [Test Case Number]
Result: [Pass/Fail]
Notes: [Any observations or issues]
Screenshots: [If applicable]
```

### Issue Tracking
```
Issue ID: [Unique identifier]
Severity: [Critical/High/Medium/Low]
Description: [Detailed description]
Steps to Reproduce: [Step-by-step instructions]
Expected Result: [What should happen]
Actual Result: [What actually happened]
Browser/Device: [Where the issue occurs]
Status: [Open/In Progress/Resolved/Closed]
```

---

**Note**: This test data document should be updated whenever the website functionality changes or new features are added.