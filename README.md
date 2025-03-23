# eBay Shopping Automation

A Selenium-based Java automation project that simulates a typical shopping experience on eBay.

## Overview

This project demonstrates automated browser testing using Selenium WebDriver with Java. The script automates several common user interactions with the eBay website, including:

- User login
- Product searching
- Product selection
- Size/color options selection
- Adding items to cart

## Features

- Automated login with user credentials
- Multi-product search (Adidas Superstar, Samsung S21 Ultra, iPhone 11 Pro)
- Handling multiple browser windows/tabs
- Selection of product variants (sizes, colors)
- Shopping cart management

## Prerequisites

- Java JDK 8 or higher
- Maven or Gradle for dependency management
- Chrome browser installed
- ChromeDriver matching your Chrome version
- Selenium WebDriver Java libraries

## Dependencies

```xml
<dependencies>
    <dependency>
        <groupId>org.seleniumhq.selenium</groupId>
        <artifactId>selenium-java</artifactId>
        <version>4.10.0</version>
    </dependency>
</dependencies>
```

## Setup Instructions

1. Clone the repository
   ```
   git clone https://github.com/yourusername/ebay-shopping-automation.git
   cd ebay-shopping-automation
   ```

2. Download ChromeDriver
   - Visit [ChromeDriver download page](https://sites.google.com/chromium.org/driver/)
   - Download the version that matches your Chrome browser
   - Place the executable in your system PATH or project directory

3. Build the project with Maven
   ```
   mvn clean install
   ```

## Running the Automation

Execute the main class to run the automation:

```
mvn exec:java -Dexec.mainClass="basicweb.FirstTestClass"
```

## Project Structure

```
ebay-shopping-automation/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── basicweb/
│   │   │       └── FirstTestClass.java
│   ├── test/
│   │   └── java/
├── pom.xml
└── README.md
```

## Customization

To modify the script for your own use:

1. Update the login credentials in the code
2. Change product search terms as needed
3. Adjust XPath selectors if the eBay website structure changes

## Important Notes

- The script includes hardcoded user credentials which should be moved to a configuration file in a real-world implementation
- Includes handling for the "passkeys" popup that may appear during login
- Uses explicit waits to handle page loading delays

## Troubleshooting

Common issues and solutions:

- **Element not found exceptions**: The eBay website structure may change. Update the XPath or CSS selectors accordingly.
- **ChromeDriver version mismatch**: Make sure your ChromeDriver version matches your Chrome browser version.
- **Login failures**: eBay may implement CAPTCHA or other security measures. Manual intervention may be required.

## License

[MIT License](LICENSE)

## Disclaimer

This project is for educational purposes only. Automated interactions with websites should comply with the website's terms of service.
