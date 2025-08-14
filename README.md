# Free File Hosting Platform

A complete file hosting web application built with PHP, HTML, CSS, and JavaScript. Designed specifically for InfinityFree hosting compatibility.

## Features

- **File Upload**: Drag & drop file upload with support for HTML, CSS, JS, and TXT files
- **Online Editor**: Built-in code editor with syntax highlighting using CodeMirror
- **Live Preview**: Real-time HTML preview while editing
- **File Management**: View, edit, and delete uploaded files
- **Templates**: Pre-built HTML templates (Basic, Bootstrap, Landing Page)
- **Responsive Design**: Mobile-friendly interface with Bootstrap 5
- **Security**: Secure file handling with proper validation

 ## Demo = https://nghms.rf.gd/?i=1

## InfinityFree Hosting Setup

### Step 1: Download Files
Download all files from this project to your computer.

### Step 2: Upload to InfinityFree
1. Login to your InfinityFree hosting account
2. Go to File Manager or use FTP
3. Upload all PHP files to your `htdocs` or `public_html` directory:
   - `index.php`
   - `upload.php`
   - `edit.php`
   - `html-editor.php`
   - `.htaccess`
4. Create an `uploads` folder and upload:
   - `uploads/.htaccess`
   - `uploads/index.php`

### Step 3: Set Permissions
Set the following folder permissions:
- `uploads/` folder: 755 or 775

### Step 4: Test the Application
1. Visit your website URL
2. Try uploading a test file
3. Verify the editor and preview functions work

## File Structure

```
/
├── index.php           # Main page with file listing and upload
├── upload.php          # File upload and management backend
├── edit.php            # File editor with syntax highlighting  
├── html-editor.php     # HTML editor with templates and live preview
├── .htaccess          # Apache configuration
├── uploads/           # Directory for uploaded files
│   ├── .htaccess     # Security rules for uploads
│   └── index.php     # Redirect protection
└── README.md          # This file
```

## Security Features

- File type validation (only HTML, CSS, JS, TXT allowed)
- File size limits (5MB maximum)
- PHP execution disabled in uploads folder
- Secure file naming with timestamps
- Session-based file management
- Input sanitization and validation

## Supported File Types

- **.html** - HTML files
- **.css** - CSS stylesheets  
- **.js** - JavaScript files
- **.txt** - Text files

## InfinityFree Limitations

- **File Size**: Maximum 5MB per file (can be adjusted)
- **PHP Version**: Works with PHP 7.4+ 
- **Database**: Not required (uses sessions)
- **Storage**: Limited by hosting quota

## Troubleshooting

### Common Issues on InfinityFree:

1. **Upload not working**: Check folder permissions on `uploads/` directory
2. **Files not displaying**: Ensure `.htaccess` is uploaded correctly
3. **Editor not loading**: Verify CDN links are accessible
4. **Permission errors**: Contact InfinityFree support for folder permission help

### File Upload Errors:

- **File too large**: Reduce file size or adjust limits in upload.php
- **Invalid file type**: Only HTML, CSS, JS, TXT files are allowed
- **Upload failed**: Check folder permissions and disk space

## Customization

### Changing Upload Limits:
Edit `upload.php` line 6:
```php
$maxFileSize = 5 * 1024 * 1024; // Change 5 to desired MB
```

### Adding File Types:
Edit `upload.php` line 7:
```php
$allowedExtensions = ['html', 'css', 'js', 'txt', 'new_type'];
```

### Styling Changes:
Modify the CSS variables in each PHP file's `<style>` section:
```css
:root {
    --primary-color: #6c5ce7;    /* Main color */
    --secondary-color: #a29bfe;  /* Secondary color */
    --dark-color: #2d3436;       /* Dark theme */
}
```

## Browser Compatibility

- **Chrome**: ✅ Full support
- **Firefox**: ✅ Full support  
- **Safari**: ✅ Full support
- **Edge**: ✅ Full support
- **Mobile**: ✅ Responsive design

## License

This project is open source and available under the MIT License.

## Support

For issues specific to InfinityFree hosting, contact their support team.
For application bugs or feature requests, create an issue in the project repository.

---

**Made for InfinityFree Hosting** 🚀
