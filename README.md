# ServeEase Dashboard

A modern, responsive dashboard application for a home service marketplace platform that connects users with service providers based on location and service type.

## Table of Contents

- [Project Overview](#project-overview)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Component Architecture](#component-architecture)
- [Setup and Installation](#setup-and-installation)
- [Future Implementations](#future-implementations)

## Project Overview

ServeEase is a comprehensive platform designed to bridge the gap between customers seeking various services and qualified service providers in their area. The dashboard provides an intuitive interface for users to search, filter, and book service providers, as well as manage their bookings and profile.

## Features

- **Service Search**: Location-based service provider search with filtering options
- **User Dashboard**: Comprehensive dashboard for users to manage all aspects of their account
- **Service History**: Track past, upcoming, and completed service bookings
- **Saved Providers**: Save and manage favorite service providers
- **User Profile**: Manage personal information and preferences
- **Notifications**: Stay updated with service-related notifications

## Tech Stack

- **Frontend**: React with TypeScript
- **Styling**: Tailwind CSS for responsive design
- **Icons**: Lucide React for modern UI icons
- **State Management**: React Hooks for local state management
- **Future Backend**: Placeholder for future backend integration

## Project Structure

```
serveease-dashboard/
├── src/
│   ├── components/         # Reusable UI components
│   │   ├── Header.tsx      # Main navigation header
│   │   ├── HeroSection.tsx # Homepage hero section with search functionality
│   │   ├── ServiceProviders.tsx # Service provider listing and filtering
│   │   ├── ServiceHistory.tsx # User's service booking history
│   │   ├── SavedProviders.tsx # User's saved service providers
│   │   └── UserProfile.tsx # User profile management component
│   ├── data/               # Sample data for development
│   │   └── sampleData.ts   # Mock data structures
│   ├── pages/              # Page components 
│   │   └── UserDashboard.tsx # Main dashboard page component
│   ├── App.tsx             # Main application component
│   └── index.tsx           # Entry point
└── public/                 # Static assets
```

## Component Architecture

### App Component
The main application component (`App.tsx`) serves as the entry point and manages the application's primary state:
- Controls whether to display the landing page or user dashboard
- Maintains the selected service and user location
- Handles search functionality

### Header Component
`Header.tsx` provides the main navigation interface:
- Positioned at the top of the application
- Features the ServeEase logo on the far left
- Contains navigation buttons for My Bookings and My Reviews
- Includes a Login/Sign Up button on the far right
- Designed to be responsive across different screen sizes
- Currently contains placeholder functions for future backend integration

### HeroSection Component
`HeroSection.tsx` is the main landing interface that allows users to search for services:
- Features a prominent search bar for service and location input
- Provides auto-suggestions for services grouped by categories
- Includes location detection capability
- Displays popular service shortcuts
- Visually enhanced with subtle background patterns and gradients

### ServiceProviders Component
`ServiceProviders.tsx` displays service providers based on search criteria:
- Lists providers in a responsive grid layout
- Offers advanced filtering options (rating, cost, sorting)
- Each provider card shows essential information (name, service type, location, cost, rating)
- Includes hover effects and visual enhancements for better user experience
- Cost range slider allows users to filter by price range

### UserDashboard Component
`UserDashboard.tsx` acts as the container for all user dashboard functionality:
- Features a sidebar navigation for different dashboard sections
- Displays user information and statistics
- Manages the active tab state for different dashboard views
- Contains mock data for development and demonstration
- Dashboard sections include:
  - Main dashboard with stats and recent activity
  - User profile
  - Service history
  - Saved providers
  - Notifications

### ServiceHistory Component
`ServiceHistory.tsx` allows users to view and manage their service bookings:
- Displays bookings with filtering options
- Adapts layout for mobile and desktop views
- Uses color-coded status indicators
- Includes actions like leaving reviews or canceling bookings
- Features sorting options by date, cost, or service type

### SavedProviders Component
`SavedProviders.tsx` manages the user's saved service providers:
- Displays saved providers in a grid layout
- Allows filtering by service category
- Includes search functionality
- Shows provider details with a modern card design
- Features options to book services or remove from saved list

### UserProfile Component
`UserProfile.tsx` handles user profile information:
- Allows viewing and editing personal information
- Displays account status
- Features a clean, two-column layout
- Includes field validation and form submission logic

## Setup and Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/serveease-dashboard.git
cd serveease-dashboard
```

2. Install dependencies:
```bash
npm install
```

3. Run the development server:
```bash
npm start
```

4. Access the application at `http://localhost:3000`

## Future Implementations

The current implementation includes placeholders for several features that will be connected to a backend in the future:

1. **Authentication System**: User registration, login, and profile management
2. **Booking Management**: Complete booking flow from selection to confirmation
3. **Review System**: Allow users to leave and view reviews for service providers
4. **Notification System**: Real-time notifications for bookings and messages
5. **Payment Integration**: Secure payment processing for service bookings
6. **Provider Dashboard**: Separate dashboard for service providers to manage their services
7. **Admin Panel**: Administrative controls for platform management
8. **Analytics**: Usage statistics and performance metrics

---

The ServeEase Dashboard is designed with scalability in mind, featuring a modular component structure that makes adding new features straightforward. The use of TypeScript provides type safety and better developer experience, while Tailwind CSS ensures a responsive and visually appealing interface across all device sizes.
