# Pothole-Reporting-System
 Project Name: Pothole Reporting System
 # PotholeWatch - Road Infrastructure Reporting System

A modern web application for reporting and tracking road infrastructure issues, specifically potholes, in your city. This system allows citizens to report potholes, track their status, and helps authorities manage road maintenance more effectively.

## Features

- 🗺️ Interactive map interface with Google Maps integration
- 📱 Mobile-responsive design
- 📸 Photo upload capability
- 📍 Real-time location detection
- 📧 Email notifications for report updates
- 🔍 Advanced filtering and search options
- 📊 Statistical dashboard
- 👤 User authentication system
- 🌍 Multi-city support

## Prerequisites

Before you begin, ensure you have the following installed:
- [Node.js](https://nodejs.org/) (v14 or higher)
- [MongoDB](https://www.mongodb.com/try/download/community)
- [Git](https://git-scm.com/downloads)

## Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd pothole-watch
```

2. Install dependencies:
```bash
npm install
```

3. Create a `.env` file in the root directory:
```env
PORT=3000
MONGODB_URI=mongodb://localhost:27017/pothole-watch
JWT_SECRET=your-secret-key
EMAIL_USER=your.email@gmail.com
EMAIL_PASS=your-app-specific-password
```

4. Set up Gmail credentials:
   - Enable 2-Step Verification in your Google Account
   - Generate an App Password:
     1. Go to Google Account settings
     2. Navigate to Security
     3. Under "Signing in to Google," find "2-Step Verification"
     4. At the bottom, click on "App passwords"
     5. Select "Mail" and your device
     6. Copy the generated 16-character password
     7. Paste it in your .env file as EMAIL_PASS

5. Set up Google Maps API:
   - Go to [Google Cloud Console](https://console.cloud.google.com/)
   - Create a new project or select existing one
   - Enable Maps JavaScript API
   - Create credentials (API key)
   - Replace `YOUR-GOOGLE-MAPS-API-KEY` in report.html and map.html with your API key

## Running the Application

1. Start MongoDB:
   - MongoDB should be running as a service on Windows
   - If not, start it manually using:
     ```bash
     mongod
     ```

2. Start the server:
```bash
npm run dev
```

3. Access the application:
   - Open your browser and go to: `http://localhost:3000`
   - The application should now be running!

## Usage

1. **Reporting a Pothole:**
   - Click "Report Pothole" button
   - Allow location access or manually select location
   - Upload a photo
   - Select severity level
   - Add description
   - Submit report

2. **Viewing Reports:**
   - Navigate to "View Map"
   - Use filters to sort by severity/status
   - Click markers for detailed information
   - Select different cities from dropdown

3. **Tracking Reports:**
   - Login to your account
   - View your submitted reports
   - Receive email notifications for updates

## API Endpoints

### Authentication
- POST `/api/register` - Register new user
- POST `/api/login` - User login

### Potholes
- GET `/api/potholes` - Get all potholes
- POST `/api/potholes` - Create new pothole report
- GET `/api/potholes/:id` - Get specific pothole
- PATCH `/api/potholes/:id` - Update pothole status

### Statistics
- GET `/api/statistics` - Get pothole statistics
- GET `/api/potholes/near/me` - Get nearby potholes

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- Google Maps API for location services
- MongoDB for database management
- Express.js for the backend framework
- Node.js for the runtime environment 
