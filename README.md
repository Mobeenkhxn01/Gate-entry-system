# Gate Entry System

A web-based gate entry management system that allows tracking of personnel entering and exiting a facility. The system captures visitor information and automatically saves it to a spreadsheet for record-keeping and analysis.

## Features

- **User-friendly Interface**: Clean, responsive design with background imagery
- **Personnel Classification**: Support for Employees, Trainees, and Visitors
- **Time Tracking**: Records both entry and exit times with date/time picker
- **Automatic Data Storage**: Form submissions are automatically saved to a Google Sheets-compatible spreadsheet via API
- **Real-time Feedback**: Success and error notifications for form submissions

## Form Fields

The system captures the following information:

- **Name**: Full name of the person
- **Purpose**: Reason for visit/entry
- **Type**: Personnel classification (Employee/Trainee/Visitor)
- **Entry Time**: Date and time of entry
- **Exit Time**: Date and time of exit

## Technologies Used

- **HTML5**: Structure and semantic markup
- **CSS3**: Styling with Tailwind CSS framework
- **JavaScript**: Form handling and API integration
- **jQuery**: AJAX requests and DOM manipulation
- **API Spreadsheets**: Data persistence using apispreadsheets.com service

## Setup Instructions

### Prerequisites

- Web browser with JavaScript enabled
- Internet connection (required for external dependencies and API calls)

### Installation

1. **Clone or download** the project files to your local directory

2. **Required Files**:
   ```
   ├── index.html          # Main HTML file
   ├── output.css          # Tailwind CSS compiled styles
   ├── bg.jpg             # Primary background image
   └── bg2.jpg            # Secondary background image
   ```

3. **Background Images**: 
   - Add your desired background images as `bg.jpg` and `bg2.jpg` in the same directory
   - Images should be web-optimized (JPEG/PNG format)

4. **Open the application**:
   - Simply open `index.html` in a web browser
   - No server setup required for basic functionality

### API Configuration

The system uses API Spreadsheets service to store form data:

- **Current API Endpoint**: `https://api.apispreadsheets.com/data/YOUR_API_KEY/`
- **Method**: POST request with form data

To use your own spreadsheet:

1. Visit [apispreadsheets.com](https://apispreadsheets.com)
2. Create a new spreadsheet API
3. Replace the URL in the JavaScript section:
   ```javascript
   url:"https://api.apispreadsheets.com/data/YOUR_API_KEY/",
   ```

## Usage

1. **Access the System**: Open the HTML file in a web browser
2. **Fill the Form**:
   - Enter the person's name
   - Specify the purpose of visit
   - Select the appropriate personnel type
   - Set entry and exit times using the date/time pickers
3. **Submit**: Click the "Submit" button to save the data
4. **Confirmation**: You'll receive a success/error message

## Customization

### Styling
- The system uses Tailwind CSS for styling
- Modify the `output.css` file or recompile Tailwind with your custom configuration
- Background images can be changed by replacing `bg.jpg` and `bg2.jpg`

### Form Fields
- Add new fields by creating similar HTML structure in the form
- Update the corresponding spreadsheet columns to match new fields
- Ensure the `name` attribute matches your spreadsheet column headers

### Personnel Types
- Modify the dropdown options in the "Type" select element
- Add or remove options as needed for your organization

## Browser Compatibility

- Chrome (recommended)
- Firefox
- Safari
- Edge
- Internet Explorer 11+

## Security Considerations

- **Data Transmission**: Uses HTTPS for API calls
- **Input Validation**: Consider adding client-side and server-side validation
- **Access Control**: Implement authentication if sensitive data is involved
- **API Security**: Monitor API usage and consider rate limiting

## Troubleshooting

### Common Issues

1. **Form not submitting**:
   - Check internet connection
   - Verify API endpoint is accessible
   - Check browser console for JavaScript errors

2. **Styling issues**:
   - Ensure `output.css` file is in the correct location
   - Check that Tailwind CSS classes are properly compiled

3. **Background images not loading**:
   - Verify image files exist in the project directory
   - Check image file formats and sizes

### Error Messages

- **"Form Data Submitted :)"**: Successful submission
- **"There was an error :("**: API call failed - check connection and API endpoint

## Data Export

- Access your spreadsheet data through the API Spreadsheets dashboard
- Export to various formats (Excel, CSV, etc.)
- Set up automated reporting or integrations

## Future Enhancements

- Add photo capture functionality
- Implement barcode/QR code scanning
- Add search and filter capabilities
- Create dashboard for real-time monitoring
- Add email notifications for entries/exits
- Implement user authentication and roles

## Support

For technical support or feature requests, please refer to the documentation of the respective services:

- [Tailwind CSS Documentation](https://tailwindcss.com/docs)
- [jQuery Documentation](https://api.jquery.com/)
- [API Spreadsheets Documentation](https://apispreadsheets.com/docs)

## License

This project is provided as-is for educational and commercial use. Please ensure compliance with your organization's data handling policies and applicable privacy regulations.

---

**Note**: Remember to replace the API endpoint with your own before deploying to production.
