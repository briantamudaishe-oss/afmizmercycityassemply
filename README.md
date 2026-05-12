# AFMIZ Mercy City Assembly Website

A comprehensive church management website featuring modern design, secure admin dashboard, and integrated social media functionality.

## 🌟 Features

### 🏠 Homepage
- **Church Introduction**: Spirit-filled community focused on Word, Worship, and Prayer
- **Service Times**: Sunday services, prayer meetings, youth programs
- **Announcements**: Latest church news and events
- **Social Media Links**: Facebook, Instagram, TikTok, WhatsApp, YouTube
- **Call-to-Action Buttons**: "Give Now" and "Make a Pledge"

### 📜 Pledges System
- **Popup Modal Form** with fields for:
  - Full Name, Email, Phone Number
  - Pledge Type (Building, Missions, Facility, General)
  - Amount (ZWL)
- **Auto-notifications**: Email confirmation and WhatsApp alerts

### 💰 Tithes & Offerings System
- **Secure Online Giving** with popup form
- **Payment Integration** (Bank Transfer, Mobile Banking, Cash)
- **Auto Receipt Generation** via Email
- **Optional WhatsApp Confirmations**

### 🔐 Admin Dashboard
- **Restricted Access**: Pastor-approved login with 2FA
- **Role-Based Security**: Admin, Member, Visitor permissions
- **Dashboard Features**:
  - View pledges and offerings
  - Track financial data with charts
  - Manage users and roles
  - Send notifications (Email & WhatsApp)
  - Generate reports (Financial, Membership, Attendance)

### 🔔 Notification System
- **Multi-Channel**: Email and WhatsApp
- **Automated Triggers**: New pledges, payment confirmations, announcements
- **Bulk Messaging**: Send to all members or specific groups

### 📱 Social Media Integration
- **Embedded Feeds**: Facebook posts, Instagram grid, TikTok videos
- **Direct Links**: All platforms linked to @AFMIZMercyCityAssembly
- **Live Updates**: Mock social media content display

## 🛡️ Security Features

### Authentication
- **Encrypted Passwords**: Secure storage (mock implementation)
- **Two-Factor Authentication**: SMS verification codes
- **Session Management**: 30-minute auto-logout
- **Role-Based Access Control**: Different permissions per user type

### Data Protection
- **Input Validation**: XSS and SQL injection prevention
- **HTTPS Ready**: SSL encryption support
- **Security Logging**: All access attempts monitored
- **Account Lockout**: After 3 failed login attempts

## 🎨 Design & Technology

### Visual Design
- **Classic + Technological**: Professional church aesthetic
- **Zimbabwe-Inspired Colors**: Deep green (#1a472a), Gold (#d4af37), Red (#c41e3a)
- **Responsive Design**: Mobile, tablet, and desktop optimized
- **Modern UI/UX**: Smooth animations and intuitive navigation

### Technical Stack
- **Frontend**: HTML5, CSS3, JavaScript (ES6+)
- **Charts**: Chart.js for data visualization
- **Icons**: Font Awesome 6
- **Fonts**: Google Fonts (Segoe UI)
- **Responsive**: CSS Grid and Flexbox

## 📁 File Structure

```
mercy-city-files/
├── index.html              # Main church website
├── styles.css              # Main website styles
├── script.js               # Main website functionality
├── admin.html              # Admin dashboard
├── admin-styles.css        # Admin dashboard styles
├── admin-script.js         # Admin dashboard functionality
├── login.html              # Admin login page
├── login-styles.css        # Login page styles
├── login-script.js         # Login functionality
└── 501677961_18089998102718163_546494354468193759_n.PNG.jpg  # Church logo
```

## 🚀 Getting Started

1. **Download all files** to the same directory
2. **Open `index.html`** in your web browser to view the main website
3. **Admin Access**: Click "Admin" in navigation or open `login.html`
4. **Login Credentials** (Demo):
   - Username: `pastor` or `admin@mercycityassembly.zw`
   - Password: `admin123` or `password123`
   - 2FA Code: `123456` or `654321`

## 👥 User Roles

### Visitor
- Browse website content
- Submit pledges and offerings
- View public information

### Member
- All visitor permissions
- Receive notifications
- Track personal pledges

### Admin (Church Leaders)
- Full dashboard access
- User management
- Financial oversight
- Notification broadcasting
- Report generation

## 📊 Admin Dashboard Features

### Dashboard Overview
- Real-time statistics (pledges, offerings, members)
- Recent activity feed
- Financial trend charts
- Quick action buttons

### Pledges Management
- View all pledges with filtering
- Search by name/email
- Status tracking (Active, Pending, Completed)
- Export capabilities

### Offerings Management
- Track all donations
- Receipt generation
- Payment method analysis
- Financial reporting

### User Management
- Add/edit user accounts
- Role assignment
- Member statistics
- Bulk operations

### Notifications
- Compose messages
- Multi-channel sending
- Delivery tracking
- History and analytics

### Reports
- Financial reports (downloadable)
- Membership analytics
- Attendance tracking
- Notification performance

## 🔧 Customization

### Church Information
- Update church name, address, contact details
- Modify service times and announcements
- Change social media links

### Branding
- Replace logo file with your church logo
- Adjust color scheme in CSS variables
- Customize text content and messaging

### Features
- Add new pledge types or payment methods
- Extend notification channels
- Add new admin dashboard sections

## 📞 Support

For technical support or customization requests:
- Email: info@mercycityassembly.zw
- Phone: +263 0000 000000
- Address: 88-89 Aerodrome Road, Mutare, Zimbabwe

## 📝 License

This website is created for AFMIZ Mercy City Assembly. All rights reserved.

## 🙏 Acknowledgments

Built with love for the AFMIZ Mercy City Assembly community. May this website serve to strengthen our church family and spread God's message of hope and mercy.

**"For where two or three gather in my name, there am I with them." - Matthew 18:20**

---

## New Full-Stack Church Management System

This workspace now includes a new full-stack structure under `client` and `server`:

- `client/public-site`: Next.js public website with Tailwind CSS and SEO-ready pages.
- `client/admin-dashboard`: Next.js admin dashboard with secure role-based UI.
- `server`: Express backend with JWT authentication, Mongoose models, protected admin routes, and CMS content APIs.

### Setup

1. Copy `.env.example` to `server/.env` and set `MONGODB_URI`, `JWT_SECRET`, and `CLIENT_URL`.
2. Run `npm install` in `server`, `client/public-site`, and `client/admin-dashboard`.
3. Start the backend with `npm run dev` in `server`.
4. Start the public site with `npm run dev` in `client/public-site`.
5. Start the admin dashboard with `npm run dev` in `client/admin-dashboard`.

### Notes

- Admin routes are protected by `server/middleware/authMiddleware.js`.
- Public pages fetch dynamic content from `/api/public/home`.
- The admin dashboard is designed as a separate app and is not accessible through the public site.
- The backend includes models for `User`, `Member`, `Event`, `Sermon`, `Donation`, `PrayerRequest`, `Ministry`, `BlogPost`, `GalleryImage`, and `Notification`.
- Authentication is handled via JWT tokens stored in localStorage for the admin dashboard.
- Public forms (donations, prayer requests, contact) submit data to backend APIs with success/error feedback.
- **NEW**: Email notifications are sent for prayer requests, donations, sermon uploads, and blog posts.
- **NEW**: Admin dashboard includes interactive charts (donations, attendance, ministry distribution).
- **NEW**: Public site features dark mode toggle with persistent theme preference.

### Admin Login

- **Email:** admin@mercycity.org
- **Password:** admin123
- **URL:** http://localhost:3001 (admin dashboard)

### API Endpoints

**Public:**
- `GET /api/public/home` - Get homepage content (events, sermons, ministries, gallery, blog posts)
- `POST /api/public/prayer-requests` - Submit prayer request
- `POST /api/public/contact` - Submit contact form

**Auth:**
- `POST /api/auth/login` - Admin login
- `POST /api/auth/register` - Register admin user
- `GET /api/auth/profile` - Get current user profile

**Admin (Protected):**
- `GET /api/admin/overview` - Dashboard statistics
- `POST /api/admin/events` - Create event
- `PUT /api/admin/events/:id` - Update event
- `POST /api/admin/sermons` - Upload sermon
- `POST /api/admin/donations` - Record donation
- `PUT /api/admin/prayers/:id` - Update prayer request status
- `POST /api/admin/blog` - Create blog post
- `POST /api/admin/gallery` - Upload gallery image
- `PUT /api/admin/users/:id/role` - Change user role

### Features

#### Public Website
- Responsive design with mobile-first approach
- Dark mode toggle (persistent across sessions)
- Dynamic content from admin dashboard
- Interactive forms with email notifications
- SEO-optimized pages

#### Admin Dashboard
- Secure authentication with JWT
- Role-based access control
- Interactive charts and analytics
- Real-time dashboard statistics
- Activity logging for all admin actions
- Email notifications for key events

#### Backend
- RESTful API with proper error handling
- Email notifications for user interactions
- Activity logging for admin actions
- CSRF protection and input validation
- Sample data seeding on first run
