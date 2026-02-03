# Safaricom SMS Bundle Simulator

An interactive web-based simulator that replicates the Safaricom SMS bundle USSD menu interface. This application provides an intuitive and visually appealing way to explore all available SMS bundle options that are typically accessed through the *188# USSD code.

## Features

- **Interactive USSD Simulation**: Navigate through the complete Safaricom SMS bundle menu system with an authentic user experience
- **Modern User Interface**: Clean, responsive design with smooth animations and transitions
- **Phone Simulator Display**: Visual representation of a mobile phone interface for enhanced realism
- **Complete Menu Coverage**: All SMS bundle options including daily, weekly, monthly, and unlimited plans
- **Responsive Design**: Optimized for seamless viewing on desktop, tablet, and mobile devices
- **No External Dependencies**: Pure HTML, CSS, and JavaScript - runs entirely in the browser

## Live Demo

Simply open the `Index.html` file in any modern web browser to start exploring the SMS bundle options.

## Available SMS Bundle Options

The simulator includes all major Safaricom SMS bundle categories:

- **Unlimited SMS Bundles**: Daily and weekly unlimited SMS packages
- **Daily SMS Bundles**: 20, 200, or unlimited SMS options
- **Weekly SMS Bundles**: 100, 1000, or unlimited SMS packages
- **Monthly SMS Bundles**: 1500 or 3500 SMS packages
- **My5 Unlimited SMS**: Special service for unlimited SMS to 5 favorite numbers
- **Gift Bundles**: Purchase SMS bundles for other phone numbers
- **Balance Check**: Simulate balance inquiry functionality
- **Chat Ibambe**: SMS tracking and bonus balance features

## Installation

### Option 1: Clone the Repository

```bash
git clone https://github.com/Martin888Maina/JS-Safaricom-SMS-Bundle-Program.git
cd JS-Safaricom-SMS-Bundle-Program
```

### Option 2: Download ZIP

1. Click the "Code" button on the GitHub repository page
2. Select "Download ZIP"
3. Extract the ZIP file to your desired location

## Usage

1. Navigate to the project directory
2. Open `Index.html` in your preferred web browser
3. Click "Start Exploring" to begin navigating the menu
4. Select options by clicking on the menu items
5. Use the "Back" button to return to previous menus or "Main Menu" to start over

## Technology Stack

- **HTML5**: Semantic markup and modern document structure
- **CSS3**: Custom styling with CSS variables, flexbox, animations, and responsive design
- **JavaScript (ES6+)**: Object-oriented programming with classes, modern syntax, and DOM manipulation
- **Google Fonts**: Poppins and Inter font families for professional typography

## Project Structure

```
JS-Safaricom-SMS-Bundle-Program/
├── Index.html          # Main application file containing HTML, CSS, and JavaScript
├── README.md           # Project documentation
├── LICENSE             # MIT License
└── LICENSE.txt         # Original license file
```

## Browser Compatibility

The application is compatible with all modern web browsers:

- Google Chrome (version 90+)
- Mozilla Firefox (version 88+)
- Microsoft Edge (version 90+)
- Safari (version 14+)
- Opera (version 76+)

## Code Architecture

The application is built using object-oriented JavaScript with a `SafaricomUSSD` class that manages:

- Menu state and navigation history
- Dynamic content rendering
- User interaction handling
- Input validation and error management
- Result display and feedback

Key methods include:
- `showMainMenu()`: Displays the primary menu options
- `selectOption()`: Handles user selections and routing
- `renderMenu()`: Generic menu rendering system
- `showResult()`: Success message display
- `showError()`: Error feedback to users

## Customization

The application uses CSS variables for easy theme customization. Key color variables are defined in the `:root` selector:

```css
--primary-coral: #E07856;
--primary-dark: #D35F3C;
--secondary-mint: #52D4A3;
--secondary-dark: #3AB88A;
--bg-cream: #F9F5F0;
```

Modify these values in the `<style>` section to change the color scheme.

## Educational Purpose

This project serves as an educational demonstration of:

- Building interactive web applications without frameworks
- Implementing state management in vanilla JavaScript
- Creating responsive and accessible user interfaces
- Object-oriented programming principles in JavaScript
- Modern CSS techniques including animations and transitions

## Contributing

Contributions are welcome! If you have suggestions for improvements or find any issues:

1. Fork the repository
2. Create a new branch (`git checkout -b feature/improvement`)
3. Make your changes
4. Commit your changes (`git commit -m 'Add some improvement'`)
5. Push to the branch (`git push origin feature/improvement`)
6. Open a Pull Request

## Disclaimer

This is a simulator for educational and demonstration purposes only. It does not connect to Safaricom's actual USSD system and does not perform real transactions. For actual SMS bundle purchases, please dial *188# on your Safaricom line or visit the official Safaricom website.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Author

**Martin Maina**

- GitHub: [@Martin888Maina](https://github.com/Martin888Maina)

## Acknowledgments

- Safaricom Kenya for the original USSD menu structure and SMS bundle offerings
- The open-source community for inspiration and best practices
- Google Fonts for providing the Poppins and Inter font families

## Future Enhancements

Potential improvements for future versions:

- Add keyboard navigation support for accessibility
- Implement search functionality for quick bundle lookup
- Add price comparison charts between different bundles
- Include bundle validity period information
- Add dark mode toggle option
- Create multi-language support (English and Swahili)

---

For questions, feedback, or support, please open an issue on the GitHub repository.
