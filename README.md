# Nagad Payment Gateway

A modern, multi-stage payment gateway interface built with HTML5, CSS3, and Vanilla JavaScript. This project provides a complete payment processing flow with account verification, OTP validation, password confirmation, and transaction status pages.

## Features

- **Account Entry** - 11-digit Nagad account number input with auto-focus digit fields
- **OTP Verification** - 6-digit One-Time Password validation
- **Password Confirmation** - 4-digit password verification
- **Payment Processing** - Real-time loading indicator with countdown timer
- **Transaction Status** - Success and failure confirmation pages
- **Responsive Design** - Optimized for mobile devices (360px container width)
- **Smart Input Handling** - Auto-advance digits, backspace support, paste functionality
- **Form Validation** - Mandatory field checks with error animations

## Project Structure

```
Button/
├── Button.html           # Account number entry form
├── otp.html             # 6-digit OTP verification form
├── password.html        # 4-digit password confirmation form
├── Waiting.html         # Payment processing page with countdown
├── success.html         # Success confirmation page
├── fail.html            # Failure notification page
├── Button.js            # Placeholder file
├── Untitled design (1).png   # Merchant logo
├── image001.gif         # Footer branding
└── README.md            # This file
```

## Payment Flow

```
Button.html (Account) 
    ↓
otp.html (OTP)
    ↓
password.html (Password)
    ↓
Waiting.html (Processing - 6 seconds)
    ↓
success.html OR fail.html (Result)
```

## How to Use

1. **Open in Browser** - Navigate to `Button.html` in any modern web browser
2. **Enter Account Number** - Type your 11-digit Nagad account number
3. **Accept Terms** - Check the terms and conditions checkbox
4. **Proceed** - Click the Proceed button to continue
5. **Complete OTP** - Enter your 6-digit OTP when prompted
6. **Enter Password** - Provide your 4-digit password
7. **Wait for Processing** - System will process your payment for 6 seconds
8. **Confirm Result** - View success or failure status with action buttons

## Technical Details

### Technologies Used
- **HTML5** - Semantic markup
- **CSS3** - Flexbox layout, gradient backgrounds, animations
- **JavaScript (ES6)** - Event handling, URL parameter passing, validation

### Key Features

#### Auto-Focus Digit Inputs
- Digits automatically advance to the next field when entered
- Backspace moves cursor to the previous field
- Paste functionality fills multiple fields from current position

#### Form Validation
- All fields are mandatory
- Terms checkbox must be accepted
- Shake animation on validation errors
- Alert dialogs for invalid inputs

#### URL Parameter Passing
- Data flows between pages via query strings
- Account number → OTP page
- OTP code → Password page
- Password → Processing page

#### Countdown Timer
- 6-second countdown on Waiting page
- Instant redirect on Close button
- Spinner animation during processing

## Customization

### Change Colors
Modify the gradient colors in the CSS:
```css
background: linear-gradient(180deg, #8B0000 0%, #D22B2B 100%);
```

### Adjust Container Size
Update the container width in CSS:
```css
.pgw-container {
    width: 360px;  /* Change this value */
}
```

### Update Merchant Logo
Replace `Untitled design (1).png` with your logo file and ensure it's in the same directory.

### Modify Countdown Duration
In `Waiting.html`, change the countdown value:
```javascript
let countdownTime = 6;  // Change to desired seconds
```

## Browser Compatibility

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## Notes

- All images must be in the same directory as the HTML files
- Uses relative file paths for image loading
- No external dependencies or frameworks required
- Pure client-side processing

## Future Enhancements

- Backend API integration for actual payment processing
- SMS/Email OTP delivery
- Multiple language support
- Transaction history tracking
- Receipt generation and download

## License

This project is part of the Nagad Payment Gateway system.

## Support

For issues or feature requests, please contact the development team.
