# GoExploree - Real Estate Mobile App

GoExploree is a comprehensive real estate mobile application built with Ionic Angular that allows users to browse, search, and book property viewings. This app provides a seamless experience for users looking to explore property listings, save favorites, book viewings, and interact with property owners.

## Project Overview

This mobile application was built using Ionic Angular and Capacitor, making it a fully-functional cross-platform app with a focus on the Android platform. The app connects to both Firebase and PostgreSQL databases for data storage and retrieval, and incorporates Google Maps for location services.

## Features

- User authentication with Firebase
- Property browsing and search functionality
- Property details with map integration
- Booking system for property viewings
- User profile management
- Favorite properties
- Real-time notifications
- Mobile-optimized UI/UX
- PostgreSQL database integration with Drizzle ORM
- Email notifications for bookings and new properties

## Project Structure

- `src/app/` - Main application code
  - `services/` - API services, authentication, data handling
  - `models/` - Data models
  - `guards/` - Authentication guards
  - Feature modules (home, login, property-details, etc.)
- `shared/` - Shared code including database schema
- `server/` - Server-side code for API and database operations
- `android/` - Android platform-specific files

## Mobile App Packages

Two packages are included with this submission:
1. `GoExploree.apk` - Ready-to-install Android application package
2. `goexploree-source.zip` - Complete source code for the Ionic Angular project

### Installation Instructions

#### Option 1: Direct Installation (Recommended)
1. Transfer the `GoExploree.apk` file to your Android device
2. On your device, navigate to the APK file and tap it
3. If prompted, enable "Install from Unknown Sources" in your device settings
4. Follow the on-screen installation instructions
5. Once installed, launch the app from your home screen or app drawer

#### Option 2: Build from Source
If you wish to customize the app before installation, use the source code package:
```
goexploree-source.zip
```
This package contains all application code, documentation, and build scripts. Follow the build instructions below to create your own APK.

## Building the APK

### Prerequisites
- Node.js 16+
- Android Studio
- Java Development Kit (JDK) 11+
- Android SDK

### Steps to build the APK

1. Extract the project source
2. Install dependencies:
   ```
   npm install
   ```
3. Build the project:
   ```
   npx ionic build --prod
   ```
4. Add Android platform (if not already added):
   ```
   npx ionic cap add android
   ```
5. Sync the project:
   ```
   npx ionic cap sync android
   ```
6. Open in Android Studio:
   ```
   npx ionic cap open android
   ```
7. From Android Studio, go to Build > Build Bundle(s) / APK(s) > Build APK(s)

## Environment Setup

The app requires the following environment variables:

- Firebase configuration:
  - `VITE_FIREBASE_API_KEY`
  - `VITE_FIREBASE_PROJECT_ID`
  - `VITE_FIREBASE_APP_ID`
- Google Maps API:
  - `GOOGLE_MAPS_API_KEY`
- Database connection:
  - `DATABASE_URL`
- SendGrid (optional for email notifications):
  - `SENDGRID_API_KEY`

## Development Server

Run the Ionic server with:
```
ionic serve --external --port 5000 --disable-host-check
```

## Mobile-Specific Optimizations

The app includes mobile-specific optimizations:
- Adaptive UI for different screen sizes
- Touch-friendly controls
- Offline storage capabilities
- Native device integrations via Capacitor
- Optimized back button handling for Android
- App lifecycle management for better performance

## API Integration

The app integrates with:
- Firebase Authentication
- Google Maps API for location services
- PostgreSQL database for data persistence
- SendGrid for email notifications

## User Guide

### Getting Started
1. Launch the GoExploree app
2. Register a new account or log in using Google authentication
3. Browse through the available properties on the home screen
4. Use the search function to find properties by location

### Viewing Properties
1. Tap on any property card to view detailed information
2. Explore property images, features, and the location map
3. Save properties to your favorites by tapping the heart icon
4. Contact property owners or book viewings directly through the app

### Managing Your Account
1. Access your profile through the menu
2. View your booking history and upcoming viewings
3. Manage your favorite properties
4. Update your profile information as needed

## Technical Achievements

- **Hybrid Database Architecture**: Implemented a dual database system with PostgreSQL (via Drizzle ORM) as the primary database and Firebase as a fallback
- **Offline Functionality**: Added local caching for properties and user sessions to maintain functionality when offline
- **Mobile-Native Features**: Integrated Capacitor plugins for a true native mobile experience
- **Real-time Data Updates**: Implemented real-time property updates and booking notifications
- **Responsive UI**: Created a fully responsive design that works across all device sizes

## Future Enhancements

- In-app messaging between users and property owners
- Virtual property tours using 360° images
- Machine learning for personalized property recommendations
- Advanced filtering options for property search
- Integration with payment gateways for booking deposits

## Contact and Support

For any issues or questions, please contact the development team at support@goexploree.com