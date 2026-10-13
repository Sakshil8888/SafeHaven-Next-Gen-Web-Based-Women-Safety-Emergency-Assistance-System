🛡️ SafeHaven — Women Safety Web Application
A full-stack, production-ready Women Safety & Emergency Response Web Application built with Node.js, Express.js, MongoDB, HTML5, CSS3, and Vanilla JavaScript.

🌟 Features
🚨 One-Tap SOS Alert — Instantly triggers an emergency alert with real-time GPS tracking and generates a shareable live-location link for trusted contacts (no login needed to view).
🗺️ Interactive Safe Map — Leaflet.js + OpenStreetMap to find nearby Police Stations, Hospitals, and safe routes using OSRM routing.
🔊 Emergency Siren — Web Audio API generates a loud emergency alarm sound directly from the browser.
🔦 Flashlight Strobe — Controls the device camera torch or falls back to a screen strobe effect.
📞 Fake Call Simulator — Full-screen fake incoming call overlay with custom caller name, ringtone, and voice response.
👥 Emergency Contacts — Add, edit, and delete trusted contacts with name, phone, and relationship details.
📚 Safety Tips — Categorized safety guidelines covering Night Travel, Public Transport, Solo Travel, Emergency Protocols, and Digital Privacy.
📊 Admin Dashboard — Analytics, user management, SOS audit logs, and incident timeline.
🌙 Dark / Light Theme — Fully responsive, mobile-first UI with theme switching.
📶 PWA Support — Works offline via Service Worker caching.
🛠️ Tech Stack
Layer	Technology
Frontend	HTML5, CSS3, Vanilla JavaScript
Maps	Leaflet.js, OpenStreetMap, OSRM, Overpass API
Backend	Node.js, Express.js
Database	MongoDB + Mongoose (auto falls back to in-memory store)
Security	JWT, bcryptjs, helmet, express-rate-limit, cors
PWA	Service Worker, Web App Manifest
🚀 Setup & Run Locally
1. Install Dependencies
npm install
2. Create a .env file
PORT=5000
MONGODB_URI=mongodb://127.0.0.1:27017/women_safety_db
JWT_SECRET=your_secret_key_here
JWT_EXPIRES_IN=7d
NODE_ENV=development
3. Seed Initial Data (optional)
npm run seed
4. Start the App
npm start

Then open: http://localhost:5000

🔑 Demo Login Credentials
Role	Email	Password	Emergency PIN
Admin	admin@safehaven.org	Admin@123	9999
User	sarah@example.com	User@123	1234
📡 API Endpoints

Auth
POST /api/auth/register — Register new user
POST /api/auth/login — Login & get JWT token
GET /api/auth/me — Get current user profile

SOS
POST /api/sos/trigger — Trigger SOS alert
POST /api/sos/location-update — Push live GPS coordinates
POST /api/sos/resolve — Deactivate SOS with PIN
GET /api/sos/active — Get active SOS state
GET /api/sos/share/:token — Public live tracking view

Contacts
GET /api/contacts — List contacts
POST /api/contacts — Add contact
PUT /api/contacts/:id — Update contact
DELETE /api/contacts/:id — Delete contact

Tips & Admin
GET /api/tips — Get safety tips
POST /api/tips — Add tip (Admin only)
GET /api/admin/analytics — System metrics (Admin only)
GET /api/admin/users — Manage users (Admin only)
☁️ Deploy to Render / Railway
Push your code to GitHub
Create a new Web Service on Render or Railway
Build command: npm install
Start command: npm start
Add environment variables: PORT, MONGODB_URI, JWT_SECRET, NODE_ENV=production

For the database, use a free MongoDB Atlas cluster and update your MONGODB_URI.

📄 License
MIT License
