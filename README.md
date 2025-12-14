# Anmol Narang Wedding Photography Website

A premium, minimal, luxury wedding photography website with cinematic aesthetic, built with HTML, CSS, JavaScript, PHP, and MySQL.

## 🎨 Design Features

- **Elegant Design System**: White background, black typography, soft beige accents
- **Typography**: Playfair Display (headings) + Montserrat (body)
- **Fully Responsive**: Mobile-first design with clean breakpoints
- **Modern Animations**: Smooth transitions and scroll effects
- **SEO Optimized**: Semantic HTML structure with proper meta tags

## 📁 Project Structure

```
anmol-narang/
├── index.html              # Home page
├── services.html           # Services page
├── portfolio.html          # Portfolio with masonry grid
├── about.html              # About the photographer
├── booking.html            # Booking/Contact form
├── css/
│   └── style.css          # Complete styling system
├── js/
│   └── main.js            # All JavaScript functionality
├── php/
│   ├── config.php         # Database configuration
│   └── process-booking.php # Form handler
├── database/
│   └── schema.sql         # MySQL database schema
└── images/                 # Image directory

```

## 🚀 Setup Instructions

### 1. Prerequisites
- XAMPP installed (Apache + MySQL)
- Web browser (Chrome, Firefox, Safari, Edge)

### 2. Installation Steps

#### Step 1: Copy Files
1. Copy the `anmol-narang` folder to `C:\xampp\htdocs\`

#### Step 2: Setup Database
1. Start XAMPP and run Apache + MySQL
2. Open phpMyAdmin: `http://localhost/phpmyadmin`
3. Click on "SQL" tab
4. Open `database/schema.sql` file
5. Copy all content and paste into SQL tab
6. Click "Go" to execute

#### Step 3: Configure Database Connection
1. Open `php/config.php`
2. Update database credentials if needed:
   ```php
   define('DB_HOST', 'localhost');
   define('DB_USER', 'root');
   define('DB_PASS', '');  // Your MySQL password
   define('DB_NAME', 'anmol_narang_photography');
   ```

#### Step 4: Access Website
Open your browser and navigate to:
```
http://localhost/anmol-narang/
```

## 📄 Pages Overview

### 1. Home (`index.html`)
- Cinematic full-screen hero with overlay
- Featured wedding highlights (3 wedding stories)
- Philosophy section
- Services overview with icons
- Client testimonial
- Call-to-action sections

### 2. Services (`services.html`)
- Page hero
- 4 detailed service sections with alternating layouts:
  - Wedding Photography
  - Wedding Films
  - Pre-Wedding Shoots
  - Destination Weddings
- "How We Work" process timeline
- CTA section

### 3. Portfolio (`portfolio.html`)
- Masonry grid layout (3 columns on desktop)
- Category filters: All | Weddings |Pre-Weddings | Films | Travel
- Lightbox image viewer (click to expand)
- Hover overlays with couple names and locations

### 4. About (`about.html`)
- Photographer hero image
- Personal biography and story
- Experience statistics (years, weddings, countries)
- Philosophy section with 4 key principles
- Personal connection approach

### 5. Booking (`booking.html`)
- Two-column layout
- Contact information + social links
- Booking form with fields:
  - Name, Email, Phone (required)
  - Event Type dropdown
  - Event Date picker
  - Location
  - Message textarea
- AJAX form submission
- Success/error message display

## 🔧 Features & Functionality

### Frontend Features
- ✅ Responsive mobile menu
- ✅ Sticky navigation with scroll effect
- ✅ Portfolio category filtering
- ✅ Lightbox image viewer
- ✅ Scroll animations (fade-in effects)
- ✅ Smooth scrolling navigation
- ✅ Form validation (client & server side)
- ✅ AJAX form submission (no page reload)
- ✅ Placeholder image generation

### Backend Features
- ✅ PHP form processing
- ✅ Data sanitization & validation
- ✅ MySQL database storage
- ✅ JSON API responses
- ✅ Prepared statements (SQL injection protection)
- ✅ Error handling

### Database Schema
**Table: `bookings`**
- id (Primary Key)
- name, email, phone
- event_type, event_date, location
- message
- status (pending/contacted/confirmed/declined)
- created_at, updated_at
- Indexes on status, created_at, event_date

## 🎯 JavaScript Functionality

Located in `js/main.js`:

1. **Mobile Navigation**: Toggle menu for mobile devices
2. **Portfolio Filters**: Click to filter by category
3. **Lightbox**: Click images to view full-screen
4. **Form Handler**: AJAX submission with validation
5. **Scroll Animations**: Fade-in effects on scroll
6. **Placeholder Images**: Auto-generates gradient placeholders

## 💾 Database Management

### View All Bookings
Open phpMyAdmin and run:
```sql
SELECT * FROM bookings ORDER BY created_at DESC;
```

### Update Booking Status
```sql
UPDATE bookings 
SET status = 'confirmed' 
WHERE id = 1;
```

### Available Status Values
- `pending` - New inquiry
- `contacted` - Follow-up sent
- `confirmed` - Booking confirmed
- `declined` - Not available

## 🎨 Color Palette

```css
Primary White: #FFFFFF
Primary Black: #1A1A1A
Accent Beige: #D4C5B0
Dark Beige: #8B7355
Light Beige: #F5F1ED
```

## 📱 Responsive Breakpoints

- **Desktop**: 1024px+
- **Tablet**: 768px - 1023px
- **Mobile**: < 768px

## 🔒 Security Features

- Server-side validation
- Input sanitization with `htmlspecialchars()`
- SQL injection protection (prepared statements)
- XSS protection
- Email validation

## 📧 Optional: Email Notifications

To enable email notifications when a new booking is received:

1. Open `php/process-booking.php`
2. Uncomment the `mail()` function call in `sendNotificationEmail()`
3. Configure PHP mail settings in `php.ini`

## 🌐 Browser Compatibility

- ✅ Chrome (latest)
- ✅ Firefox (latest)
- ✅ Safari (latest)
- ✅ Edge (latest)

## 📝 Customization Tips

### Change Colors
Edit `css/style.css` - update the CSS variables:
```css
:root {
    --beige: #D4C5B0;  /* Change accent color */
    --black: #1A1A1A;  /* Change text color */
}
```

### Add More Portfolio Items
1. Add images to `images/` folder
2. Edit `portfolio.html`
3. Add new `.masonry-item` divs with appropriate `data-category`

### Modify Form Fields
1. Edit `booking.html` form
2. Update `php/process-booking.php` to process new fields
3. Alter database table if needed

## 🐛 Troubleshooting

### Form Not Submitting
- Check Apache is running in XAMPP
- Verify database exists and table is created
- Check `php/config.php` credentials
- Open browser console for JavaScript errors

### Images Not Showing
- JavaScript auto-generates placeholders
- Add your own images to `images/` folder
- Name them according to IDs in HTML files

### Database Connection Error
- Ensure MySQL is running in XAMPP
- Verify database name matches in `config.php`
- Check username/password are correct

## 📞 Support

For questions or issues:
- Email: hello@anmolnarang.com
- Phone: +91 98765 43210

## 📄 License

© 2024 Anmol Narang Photography. All rights reserved.

---

**Built with ❤️ using HTML, CSS, JavaScript, PHP & MySQL**
