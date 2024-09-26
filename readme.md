# Music Streaming Service Frontend

This project is a **Music Streaming Service** frontend built with **Next.js**. It incorporates a dark theme, modular design, and integrates with a backend for user authentication, song recommendations, and playlists management.

This Project built with Next.js, Redux & Redux Persist, SWR and Wavesurfer.js.
# Key Features

- **Mood-Based Song Discovery:** Users pick a mood from a list of 10, and the app recommends songs accordingly.
- **Favorites-Based Recommendations:** Tracks from the user’s favorite list are used to recommend songs through a KNN model trained on over a million song features.
- **Dark Mode:** A fully responsive and visually appealing dark-themed UI.
- **User Authentication:** Secure login via token-based authentication using Django as the backend.
- **Track List Rendering:** Dynamically fetches and renders the list of tracks.
- **AI/ML Recommendations:** Fetches and displays AI-recommended tracks.
- **Playlist Management:** Users can create, update, and delete playlists.
- **Favorites System:** Manage favorite tracks, albums, and artists.

# Overview

This app is designed to help users discover new music based on their mood or favorite tracks. It features two primary ways to discover songs:

1. **Discover Songs by Mood:** Users can choose from 10 different moods, and the app recommends songs that match the mood. This feature leverages a KNN (K-Nearest Neighbors) machine learning model to make suggestions.
    
2. **Recommendations Based on Favorite Tracks:** The app also offers personalized song recommendations based on the user’s current favorite tracks. A KNN model trained on over a million song parameters recommends songs that align with the user’s taste.
# Technologies

- **Framework:** [Next.js](https://nextjs.org/)
- **CSS:** Custom CSS with gradients for design components.
- **State Management:** Redux for handling favorite tracks and user sessions.
- **API Calls:** Uses `fetch` for communicating with the backend API (Django Rest Framework).
- **Component Library:** [Material UI](https://mui.com/) for some of the design elements.

# Folder Structure

src/
│
├── app/
│   ├── login/                  # Login page
│   ├── page.jsx                # Home page
│
├── components/
│   ├── AuthGuard/              # Protects routes requiring authentication
│   ├── navigation/
│   │   └── Sidebar.jsx         # Sidebar navigation component
│   ├── others/
│   │   ├── Playlists.jsx       # Renders playlists
│   │   ├── TrackListContainer.jsx # Displays a list of tracks
│   │   └── TopArtistsContainer.jsx # Displays top artists
│   └── CircleComponent.jsx     # Decorative circle component
│
├── styles/
│   ├── style.css               # Global styles
│   └── circle.css              # Styles for the CircleComponent
│
└── utils/
    ├── fetchers.js             # Functions to fetch data from APIs (e.g., fetchTopTracks)

# API Integration

### Top Tracks

Tracks are fetched using the `fetchTopTracks` function, which sends an API request to the backend for fetching the global top tracks. The data is passed to the `TrackListContainer` component for rendering.
### Playlist Management

Users can manage their playlists via API calls that allow for creating, updating, and deleting playlists. This is handled through backend integration with the Django API.

# Components

#### 1. AuthGuard
- Ensures that only authenticated users can access certain pages. Utilizes token-based authentication from Django Rest Framework.
#### 2. Sidebar
- A modular, dark-themed sidebar for easy navigation between sections like Tracks, Playlists, and Favorites.
#### 3. TrackListContainer
- A reusable component to render a list of tracks, fetched from the backend.
#### 4. Playlists
- Displays user playlists, allowing users to create, update, or delete playlists.
#### 5. CircleComponent
- A decorative component that renders circular elements to enhance the visual layout.

# Getting Started

### Prerequisites

- Node.js (v16+)
- NPM or Yarn package manager
### Installation

1. Clone the repository:
	git clone https://github.com/username/music-streaming-frontend.git 
	cd music-streaming-frontend
	
2. Install dependencies:
	npm install
	
3. Run the development server:
	npm run dev
	
4. Open your browser at http://localhost:3000.

