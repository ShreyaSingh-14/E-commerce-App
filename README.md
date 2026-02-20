# An E-commerce💹 application📱 for Handicrafts👐🏻<br>
Author: Shivram Singh Gurjar, Shreya Singh(via account Ash1412005Fame)<br>
Exciting to work on such empowering projects✨✨✨<br>

# E-Commerce App 🛍️

A modern, cross-platform e-commerce mobile application built with Expo and React Native. This app enables users to discover, explore, and interact with businesses while managing their favorite merchants.

## 📋 Table of Contents

- [Features](#features)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Configuration](#configuration)
- [Available Scripts](#available-scripts)
- [Usage](#usage)
- [File-Based Routing](#file-based-routing)
- [Architecture](#architecture)
- [Contributing](#contributing)

## ✨ Features

### User Features
- **Business Exploration**: Browse and search businesses by categories
- **Home Dashboard**: View popular businesses and featured categories
- **Business Details**: Access detailed information about businesses including:
  - Business overview and description
  - Reviews and ratings
  - Contact and action buttons
  - Image galleries
- **Favorites Management**: Save and manage favorite businesses
- **User Profile**: Personalized user dashboard with profile management
- **Rating System**: View and submit reviews for businesses
- **Search & Filter**: Find businesses by category

### Business Management
- **Add Business**: Merchants can add and manage their business listings
- **Business Listing**: Organized display of all businesses with category filtering

### Technical Features
- **Cross-Platform Support**: iOS, Android, and Web platforms
- **Authentication**: Secure user authentication with Clerk
- **Real-time Database**: Firebase Firestore for data synchronization
- **Responsive UI**: Adaptive design for various screen sizes
- **Smooth Navigation**: Tab-based navigation with intuitive user flow

## 🛠️ Tech Stack

| Category | Technology |
|----------|-----------|
| **Framework** | [Expo](https://expo.dev) (~53.0.9) |
| **Language** | JavaScript/TypeScript with React 19.0.0 |
| **Mobile Runtime** | React Native 0.79.2 |
| **Backend** | Firebase 11.8.1 |
| **Database** | Cloud Firestore |
| **Authentication** | Clerk Expo 2.12.0 |
| **Navigation** | Expo Router 5.0.6 |
| **UI Components** | React Navigation, Expo Vector Icons |
| **Utilities** | Expo Haptics, Image Picker, Secure Store, Blur |
| **Styling** | React Native StyleSheet |
| **Code Quality** | ESLint |

## 📂 Project Structure

```
E-commerce-App/
├── app/                          # Main application routes (file-based routing)
│   ├── _layout.jsx               # Root layout configuration
│   ├── index.tsx                 # Home screen
│   ├── categories.jsx            # Categories page
│   ├── favorites.jsx             # Favorites page
│   ├── (tabs)/                   # Tab-based navigation group
│   │   ├── _layout.jsx
│   │   ├── home.jsx              # Home tab
│   │   ├── explore.jsx           # Explore tab
│   │   └── profile.jsx           # Profile tab
│   ├── business/
│   │   └── add-business.jsx      # Add new business
│   ├── businessdetail/
│   │   └── [businessid].jsx      # Dynamic business detail page
│   └── businesslist/
│       └── [category].js         # Category-based business list
├── components/                   # Reusable UI components
│   ├── LoginScreen.jsx           # Authentication component
│   ├── BusinessDetail/           # Business detail page components
│   │   ├── About.jsx
│   │   ├── ActionButton.jsx
│   │   ├── NewIntro.jsx
│   │   └── Review.jsx
│   ├── BusinessList/             # Business listing components
│   └── Explore/
│   ├── Home/                     # Home page components
│   │   ├── Category.jsx
│   │   ├── CategoryItem.jsx
│   │   ├── PopularBusiness.jsx
│   │   └── Slider.jsx
│   └── Profile/                  # User profile components
│       ├── FavoritesList.jsx
│       ├── MenuList.jsx
│       └── UserIntro.jsx
├── config/
│   └── FirebaseConfig.js         # Firebase initialization
├── constants/
│   └── Colors.js                 # Color palette constants
├── hooks/
│   ├── useFavorites.js           # Custom hook for favorites management
│   └── useWarmUpBrowser.jsx      # Browser warm-up utility
├── assets/
│   ├── fonts/                    # Custom font files
│   └── images/                   # App icons and images
├── scripts/
│   └── reset-project.js          # Project reset utility
├── package.json
├── app.json
├── tsconfig.json
├── eslint.config.js
└── README.md
```

## 🚀 Installation

### Prerequisites
- Node.js (v16 or higher)
- npm or yarn
- [Expo CLI](https://docs.expo.dev/get-started/installation/)
- Firebase account with Firestore enabled
- Clerk account for authentication

### Step 1: Clone the Repository

```bash
git clone <repository-url>
cd E-commerce-App
```

### Step 2: Install Dependencies

```bash
npm install
```

### Step 3: Configure Environment Variables

Create a `.env` file in the root directory with your Firebase and Clerk credentials:

```env
EXPO_PUBLIC_FIREBASE_API_KEY=your_api_key
EXPO_PUBLIC_FIREBASE_AUTH_DOMAIN=your_auth_domain
EXPO_PUBLIC_FIREBASE_PROJECT_ID=your_project_id
EXPO_PUBLIC_FIREBASE_STORAGE_BUCKET=your_storage_bucket
EXPO_PUBLIC_FIREBASE_MESSAGING_SENDER_ID=your_sender_id
EXPO_PUBLIC_FIREBASE_APP_ID=your_app_id
EXPO_PUBLIC_FIREBASE_MEASUREMENT_ID=your_measurement_id

EXPO_PUBLIC_CLERK_PUBLISHABLE_KEY=your_clerk_key
```

### Step 4: Update Firebase Configuration

Edit [config/FirebaseConfig.js](config/FirebaseConfig.js) and replace the placeholder values with your actual Firebase credentials:

```javascript
const firebaseConfig = {
  apiKey: process.env.EXPO_PUBLIC_FIREBASE_API_KEY,
  authDomain: process.env.EXPO_PUBLIC_FIREBASE_AUTH_DOMAIN,
  projectId: process.env.EXPO_PUBLIC_FIREBASE_PROJECT_ID,
  // ... other config
};
```

## ⚙️ Configuration

### Firebase Setup
1. Create a Firebase project at [firebase.google.com](https://firebase.google.com)
2. Enable Firestore Database and Authentication
3. Copy your configuration from Firebase Console
4. Update [config/FirebaseConfig.js](config/FirebaseConfig.js)

### Clerk Authentication Setup
1. Create a Clerk account at [clerk.com](https://clerk.com)
2. Create an application in Clerk dashboard
3. Copy your Publishable Key
4. Configure Clerk in your app's environment variables

## 📜 Available Scripts

```bash
# Start the development server
npm start

# Run on Android emulator
npm run android

# Run on iOS simulator
npm run ios

# Run on web browser
npm run web

# Reset project to fresh state
npm run reset-project

# Run ESLint
npm run lint
```

### Starting the App

```bash
npm start
```

The terminal will display a menu with options:
- Press `a` to open in Android Emulator
- Press `i` to open in iOS Simulator  
- Press `w` to open in Web Browser
- Press `j` to open in Expo Go mobile app (scan QR code)

## 📱 Usage

### First-Time Setup
1. **Install Dependencies**: `npm install`
2. **Start Dev Server**: `npm start`
3. **Open on Device**: Select your preferred platform (Android, iOS, or Web)
4. **Sign In**: Use your Clerk account to authenticate
5. **Explore**: Browse businesses and categories

### Main Navigation
- **Home**: View featured categories and popular businesses
- **Explore**: Browse all available businesses
- **Favorites**: Access your saved businesses
- **Profile**: Manage your account and preferences
- **Business Detail**: View comprehensive business information

### Key User Flows
1. **Browse Businesses**: Home → Explore → Select Category → View Business List
2. **View Details**: Select Business → View About, Reviews, and Actions
3. **Save Favorite**: Click heart icon on business card
4. **Leave Review**: Navigate to Review section in business detail

## 🗂️ File-Based Routing

This project uses [Expo Router](https://docs.expo.dev/router/introduction/) for file-based routing. Routes are automatically generated from the file structure in the `app/` directory.

### Routing Examples
```
app/index.tsx              → /
app/favorites.jsx          → /favorites
app/(tabs)/home.jsx        → /home (in tab group)
app/businessdetail/[businessid].jsx  → /businessdetail/:businessid
app/businesslist/[category].js       → /businesslist/:category
```

Dynamic routes use square brackets: `[paramName].jsx`

## 🏗️ Architecture

### Component Hierarchy
- **Layouts**: Root and tab-based layout containers
- **Screens**: Full-page components (Home, Explore, Profile, etc.)
- **Feature Components**: Business detail components, listing cards, etc.
- **UI Components**: Reusable elements (buttons, cards, sliders)

### State Management
- **Custom Hooks**: `useFavorites` for favorite state management
- **Local Storage**: Secure storage with `expo-secure-store`
- **Firebase Realtime**: Firestore for persistent data

### Data Flow
1. Components fetch data from Firebase
2. Custom hooks manage local state
3. Navigation provides context
4. Components re-render on state changes

## 🤝 Contributing

Contributions are welcome! Please follow these guidelines:

1. **Fork the Repository**
2. **Create Feature Branch**: `git checkout -b feature/your-feature`
3. **Commit Changes**: `git commit -m 'Add your feature'`
4. **Push Branch**: `git push origin feature/your-feature`
5. **Open Pull Request**

### Code Standards
- Use ESLint: `npm run lint`
- Follow React component best practices
- Keep components focused and reusable
- Add appropriate comments for complex logic
- Test on multiple platforms before submitting

## 📚 Resources

- [Expo Documentation](https://docs.expo.dev/)
- [React Native Docs](https://reactnative.dev/)
- [Firebase Documentation](https://firebase.google.com/docs)
- [Clerk Documentation](https://clerk.com/docs)
- [Expo Router Guide](https://docs.expo.dev/router/introduction/)

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🤔 Support

For issues, questions, or suggestions:
- Open an issue on GitHub
- Check existing documentation
- Review Firebase and Clerk setup guides

---

**Built with ❤️ using Expo and React Native**


## Great excitement to build something that works 🚀🚀

