# RentEase - Modern Property Rental Manager

A sleek, modern web-based application for managing residential rental properties, tenants, payments, and expenses.

### 🌐 Public Data Portal
Share a unique link with tenants and managers so they can submit data directly without needing a PIN. All submissions go to a review queue where you approve or reject them.

**Portal Features:**
- Tenant profile updates (name, phone, email, emergency contact)
- Payment submissions with proof/reference numbers
- Maintenance request reporting with urgency levels
- Automatic audit trail of all submissions
- Manager review and approval workflow

### 📋 Submissions Management
- Review pending submissions in the "Submissions" tab
- Approve submissions to automatically add data to your records
- Reject submissions that don't match your requirements
- Clear processed submissions to keep the queue clean
- Timestamp tracking for all submitted data

## 🔄 Data Submission Workflow

### How Tenants Submit Data

1. **Share Portal Link**
   - Click "🌐 Share Portal" button in header
   - Copy the unique link
   - Send to tenants via WhatsApp, email, or SMS

2. **Tenants Fill Forms**
   - They open the link (no PIN needed)
   - Choose what to submit:
     - 👤 Profile info
     - 💰 Payment confirmation
     - 🔧 Maintenance requests

3. **You Review & Approve**
   - Check "Submissions" tab for pending items
   - Review accuracy and completeness
   - Click "✓ Approve & Add" to add to your records
   - Click "✗ Reject" if something is wrong

4. **Data is Automatically Added**
   - Approved tenant profiles → Tenants tab
   - Approved payments → Payments tab
   - Maintenance requests → Tracked separately

### Benefits

✅ **Accurate Data** - Tenants enter their own information  
✅ **No Manual Entry** - You don't type their details  
✅ **Time Saving** - Batch approve multiple submissions  
✅ **Audit Trail** - Know who submitted what and when  
✅ **Easy Sharing** - One link works for all tenants  
✅ **Secure** - No sensitive data in links  
✅ **Payment Proof** - Tenants can include transaction IDs  
✅ **Maintenance Tracking** - Centralized issue reporting  

## ✨ Features

### 📊 Dashboard
- **Real-time Statistics**: Track total properties, occupied units, vacant spaces, and monthly rental income
- **Recent Payments**: View the latest 5 payments at a glance
- **Upcoming Rent**: Monitor tenants who haven't paid for the current month
- **Visual Overview**: Color-coded stats for quick insights

### 🏠 Property Management
- Add, edit, and delete properties
- Track property type, location, bedrooms, and status
- Monitor monthly rent amounts
- Status indicators (Occupied, Vacant, Maintenance)

### 👥 Tenant Management
- Register tenants with contact information
- Link tenants to properties
- Track move-in dates
- Quick search and filter functionality
- Edit and delete tenant records

### 💰 Payment Tracking
- Record rental payments with detailed information
- Track payment status (Paid, Pending, Overdue)
- Filter by month, tenant, or property
- Payment history and date tracking

### 📝 Expense Tracking
- Log property maintenance and operational expenses
- Categorize expenses (Maintenance, Cleaning, Utilities, Other)
- Track expenses by property
- Detailed notes support

### 🔒 Security
- PIN-based access control (default: 1234)
- Change PIN anytime in settings
- Secure local storage of all data

### 💾 Data Management
- **Export Backup**: Download all data as JSON
- **Import Restore**: Restore from backup files
- **Auto-save**: All changes automatically saved to browser storage
- **Clear Data**: Option to reset all data (use with caution)

### 📱 Responsive Design
- Works seamlessly on desktop, tablet, and mobile
- Progressive Web App (PWA) support
- Offline capabilities
- Install as app on mobile devices

## 🎨 Design Features

### Modern Aesthetics
- Clean, professional dark theme
- Orange accent colors (#f97316)
- Smooth animations and transitions
- Modern typography (Plus Jakarta Sans, Syne)

### User Experience
- Intuitive navigation with tab-based interface
- Modal dialogs for all data entry
- Real-time search and filtering
- Responsive alert notifications
- Smooth fade and slide animations

### Accessibility
- Clear visual hierarchy
- Readable contrast ratios
- Keyboard navigation support
- Semantic HTML structure

## 🚀 Getting Started

### Installation

1. **As a Web App**: 
   - Open `index.html` in any modern browser
   - Visit `http://localhost` if using a local server

2. **As a PWA (Mobile)**:
   - Open the app in a mobile browser
   - Tap "Add to Home Screen" or "Install"
   - The app will work offline

### First Steps

1. **Unlock the App**
   - Default PIN: `1234`
   - Change it in Settings ⚙️

2. **Add Your First Property**
   - Go to "Properties" tab
   - Click "+ Add Property"
   - Fill in property details (name, type, location, rent)

3. **Register Tenants**
   - Go to "Tenants" tab
   - Click "+ Add Tenant"
   - Link tenant to property and set rent amount

4. **Record Payments**
   - Go to "Payments" tab
   - Click "+ Record Payment"
   - Log tenant payment with date and amount

5. **Track Expenses**
   - Go to "Expenses" tab
   - Click "+ Add Expense"
   - Log property maintenance and operational costs

## 📋 Data Structure

All data is stored locally in your browser. No data is sent to external servers.

```json
{
  "properties": [...],
  "tenants": [...],
  "payments": [...],
  "expenses": [...],
  "submissions": [
    {
      "id": "unique-id",
      "type": "tenant_profile|payment_submission|maintenance_request",
      "status": "pending|approved|rejected",
      "timestamp": "2024-01-15T10:30:00Z",
      "data": {
        "name": "John Doe",
        "phone": "+233 XX XXX XXXX",
        "email": "john@example.com",
        ...
      }
    }
  ],
  "maintenanceRequests": [
    {
      "id": "unique-id",
      "name": "Tenant Name",
      "category": "Plumbing|Electrical|...",
      "description": "Issue details",
      "urgency": "low|medium|high|emergency",
      "status": "open|in-progress|resolved",
      "createdAt": "2024-01-15T10:30:00Z"
    }
  ]
}
```

## 🔐 Security Notes

- **Local Storage**: All data is stored in your browser's local storage
- **No Cloud Sync**: Data doesn't sync across devices
- **Backup Your Data**: Use the export feature regularly
- **PIN Protection**: Default PIN is 1234 - change this immediately
- **Device Specific**: Each device/browser needs its own setup

## 💡 Tips & Tricks

1. **Quick Search**: Use search boxes to filter properties, tenants, and expenses
2. **Batch Payments**: Record multiple payments from the same tenant using dates
3. **Property Status**: Update property status to track maintenance and vacancies
4. **Monthly Reports**: Export data at month-end for accounting
5. **Mobile Usage**: Install as PWA on your phone for quick access

## 🌐 Browser Compatibility

- Chrome/Edge: ✅ Full support
- Firefox: ✅ Full support
- Safari: ✅ Full support
- Mobile browsers: ✅ Full support with PWA

## 📱 PWA Features

- **Offline Access**: Works without internet connection
- **App Installation**: Install on home screen (Android/iOS)
- **Standalone Mode**: Opens without browser UI
- **Fast Loading**: Pre-cached assets for instant startup

## 📞 Settings & Support

### Change PIN
1. Click ⚙️ (Settings) in header
2. Enter new 4-digit PIN
3. Click "Update PIN"

### Backup Data
1. Click ⚙️ (Settings)
2. Click "📥 Download Backup"
3. Save the JSON file securely

### Restore Data
1. Click ⚙️ (Settings)
2. Click "📤 Restore from Backup"
3. Select previously downloaded backup file

## 🎯 Performance

- **Lightweight**: Single HTML file (~150KB)
- **No Dependencies**: Pure vanilla JavaScript
- **Fast Load**: <1 second on most connections
- **Smooth Animations**: 60fps animations
- **Mobile Optimized**: <50MB app size when installed

## 🔄 Version

**RentEase v2.0** - Modernized Edition
- Improved UI/UX design
- Enhanced performance
- Better mobile experience
- Streamlined data management

## 📝 License

Created for property rental management. Use freely for personal and business purposes.

---

**Made with ❤️ for property managers**

For best experience, use on a modern browser and install as PWA on your mobile device.
