🚗 Carpool App

A full-stack carpooling web application that enables users to publish rides, search for available rides, book seats, and manage booking requests with real-time notifications.

This project is built for learning and demonstration purposes, showcasing a complete authentication flow, role-based features (driver/passenger), and ride management using a modern web stack.

📌 Features
a
User Authentication

Secure registration and login using JWT

User Profile Management

View and update personal profile details

Publish Rides

Drivers can publish car or bike rides with location, time, and seat details

Search & Book Rides

Passengers can search for available rides and send booking requests

Booking Management

Drivers can accept or reject booking requests

Notifications

Automatic notifications for booking status updates

Dashboard

Centralized access to driver and passenger actions

Responsive UI

Clean, modern, and mobile-friendly interface

🗂 Project Structure
slow/
├── package.json
├── server.js
├── public/
│   ├── index.html
│   ├── login.html
│   ├── register.html
│   ├── dashboard.html
│   ├── profile.html
│   ├── publish.html
│   ├── search.html
│   ├── notifications.html
│   ├── passenger-requests.html
│   ├── requests.html
│   ├── Passanger.html
│   ├── auth.js
│   ├── header.js
│   ├── styles.css
│   ├── auth.css
│   └── server.js

🧠 Key Files
Backend

server.js

Express server setup

MongoDB models (Mongoose)

Authentication & authorization

Ride, booking, and notification logic

Frontend (public/)

HTML Pages

index.html – Landing page

login.html, register.html – Authentication

dashboard.html – User dashboard

publish.html – Publish a ride

search.html – Search and book rides

notifications.html – Driver booking notifications

passenger-requests.html – Passenger booking requests

profile.html – User profile

JavaScript

auth.js – Authentication handling

header.js – Shared navigation/header logic

CSS

styles.css – Global styles

auth.css – Authentication page styles

🚀 Getting Started
1️⃣ Install Dependencies
cd slow
npm install

2️⃣ Environment Variables

Create a .env file inside the slow/ directory:

MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret

# Optional (for notifications)
EMAIL_USER=your_email
EMAIL_PASS=your_email_password
TWILIO_SID=your_twilio_sid
TWILIO_AUTH_TOKEN=your_twilio_auth_token
TWILIO_PHONE=your_twilio_phone_number

3️⃣ Run the Application

Production

npm start


Development (with auto-reload)

npm run dev

4️⃣ Access the App

Open your browser and visit:

http://localhost:3000

🔗 API Endpoints
Authentication

POST /api/register – Register a new user

POST /api/login – User login

User

GET /api/profile – Get logged-in user profile

Rides

POST /api/rides – Publish a new ride

GET /api/rides – Get all available rides

Bookings

POST /api/rides/:rideId/book – Send booking request

GET /api/booking-requests/user – Passenger booking requests

GET /api/rides/:rideId/booking-requests – Driver booking requests

POST /api/booking-requests/:requestId/respond – Accept or reject request

🛠 Tech Stack
Backend

Node.js

Express.js

MongoDB & Mongoose

JWT Authentication

bcryptjs

dotenv

Nodemailer

Twilio (SMS notifications)

Frontend

HTML5

CSS3

Vanilla JavaScript

⚠️ Notes

All frontend assets are served from the public/ directory.

Email and SMS notifications require valid credentials.

This project is intended for educational/demo use and may require additional security hardening before production deployment.

📄 License

This project is open-source and available for educational use.
