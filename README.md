# Branch Overdue Comparison Tool

A comprehensive web-based application for comparing branch-wise overdue collections between master and daily files, with Google Drive integration and advanced analytics.

## ✨ Enhanced Features

- 🔐 **Google Drive Integration**: Secure upload and management of master files in Google Drive
- 📊 **Advanced Excel Processing**: Robust processing of Excel files (.xlsx, .xls) with comprehensive validation
- 📈 **Branch-wise Analysis**: Detailed summary reports by branch with sorting and filtering
- 📅 **Year-wise Pivot**: Track not collected quantities by branch and year with advanced filtering
- 💾 **Enhanced Export**: Download comprehensive Excel reports with multiple sheets and timestamps
- 🎨 **Modern UI/UX**: Beautiful, responsive interface with loading indicators and progress bars
- 🔍 **Search & Filter**: Advanced search and filtering capabilities for results
- 📊 **Statistics Dashboard**: Quick statistics overview with key metrics
- 🛡️ **Security**: Input sanitization and secure data handling
- ⚡ **Performance**: Optimized for large datasets with batch processing
- 📖 **Help System**: Comprehensive in-app help and tooltips
- 📱 **Responsive Design**: Works seamlessly on desktop and mobile devices

## How to Use

### 1. Start the Application
```bash
# Navigate to the collectionComparison directory
cd collectionComparison

# Start a local server (Python 3)
python -m http.server 8000

# Or use any other local server
# For example, with Node.js http-server:
# npx http-server -p 8000
```

### 2. Access the Application
Open your browser and go to: `http://localhost:8000`

### 3. Authentication
1. Click "Sign in with Google" to authenticate with Google Drive
2. Grant necessary permissions for file access

### 4. Upload Master File
1. Select an Excel file containing your master data
2. Click "Upload/Replace Master" to store it in Google Drive
3. The file will be remembered for future sessions

### 5. Process Daily File
1. Select your daily Excel file for comparison
2. Click "Process Comparison" to analyze the data
3. View the results in the summary and pivot tables

### 6. Analyze Results
1. View the **Statistics Dashboard** for quick overview of key metrics
2. Use **Search & Filter** options to find specific branches or data
3. Sort results by different criteria (branch, collectible, collected, percentage, amount)
4. Filter pivot table by specific years

### 7. Download Results
1. Click "Download Results Excel" to get a comprehensive report
2. The enhanced report includes:
   - **Summary sheet** with branch-wise statistics and totals
   - **Collected items** details with collection dates
   - **Not collected items** details with status
   - **Pivot table** by branch and year
   - **Timestamped filename** for easy organization

## Data Format Requirements

### Master File Columns
The application expects these columns (case-insensitive):
- **Branch Name** (or Branch, Plaza, Division, Area)
- **Account Number** (or Account Number, Account_No, Code)
- **Customer Name** (or Customer Name, Customer_Name, Name)
- **Overdue** (or Opening, Closing)
- **Credit** (or Cr, Amount Received, Payment)
- **Sale Date** (or Sale_Date, Date)

### Daily File Columns
Same format as master file, with the same column names.

## Technical Details

- **Frontend**: Pure HTML, CSS, JavaScript with modern ES6+ features
- **Libraries**: 
  - SheetJS (XLSX) for Excel processing
  - Google APIs for Drive integration
- **Authentication**: Google Identity Services (OAuth 2.0)
- **Storage**: Google Drive for master files, localStorage for session data
- **Performance**: Optimized with Map data structures and batch processing
- **Security**: Input sanitization and XSS protection
- **UI Framework**: Custom CSS with modern design patterns and responsive layout

## Troubleshooting

### Common Issues

1. **Authentication Failed**
   - Ensure you're using a supported browser
   - Check if pop-ups are blocked
   - Try refreshing the page

2. **File Upload Issues**
   - Verify the file format (.xlsx or .xls)
   - Check file size (Google Drive has limits)
   - Ensure you have proper permissions

3. **Processing Errors**
   - Verify column names match expected format
   - Check for empty or corrupted data
   - Ensure both files have the same structure

### Browser Compatibility
- Chrome (recommended)
- Firefox
- Safari
- Edge

## Security Notes

- All authentication is handled by Google
- Files are stored in your Google Drive
- No data is sent to external servers except Google's APIs
- Access tokens are stored locally and can be revoked anytime

## New Features in This Version

### 🎨 Enhanced User Interface
- Modern gradient background and card-based layout
- Responsive design that works on all devices
- Beautiful loading animations and progress indicators
- Improved typography and spacing

### 🔍 Advanced Filtering & Search
- Real-time search across branch names
- Multiple sorting options (branch, collectible, collected, percentage, amount)
- Year-based filtering for pivot tables
- Reset filters functionality

### 📊 Statistics Dashboard
- Quick overview cards showing key metrics
- Total collectible, collected, and collection rate
- Total amount and item counts
- Visual representation of data

### ⚡ Performance Improvements
- Optimized data processing with Map data structures
- Batch processing for large datasets
- Non-blocking UI updates
- Memory-efficient operations

### 🛡️ Security Enhancements
- Input sanitization to prevent XSS attacks
- File validation and size limits
- Secure error handling
- Protected data processing

### 📖 Help & Documentation
- Comprehensive in-app help modal
- Contextual tooltips throughout the interface
- Step-by-step instructions
- Troubleshooting guide

## Support

For issues or questions:
1. Click the "📖 Help & Instructions" button in the application
2. Check the browser console for error messages
3. Verify your Google Drive permissions
4. Ensure your Excel files have the correct format
5. Check the troubleshooting section in the help modal
