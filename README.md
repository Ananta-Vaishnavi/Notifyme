# NotifyMe - Price Tracking Application

Welcome to NotifyMe, the price tracking application that helps you monitor the prices of your favorite items from various online stores. With NotifyMe, you can set price thresholds and receive email alerts whenever the prices drop, allowing you to make informed purchasing decisions and save money.

## Features

- User Registration and Login: Create an account and log in to access personalized features.
- Price Monitoring: NotifyMe utilizes `requests` and `BeautifulSoup` to scrape store websites and fetch item prices.
- Price Alerts: Set price thresholds for items and receive email notifications when prices fall below the specified limit.
- Technology Stack: The application is built using MongoDB for the database, Python with Flask and Jinja2 for the backend, and HTML/CSS/Bootstrap for the frontend. E-mail notifications are handled through Mailgun.

## Installation and Setup

Follow these steps to install and set up NotifyMe:

1. **Prerequisites:** Ensure you have the following installed on your system:

   - Python 3.7 or higher
   - MongoDB
   - Git

2. **Clone the Repository:** Open your terminal and navigate to the directory where you want to store the project. Then, run the following command to clone the repository:

```
git clone
```

Install Dependencies: Change into the project directory and install the required Python dependencies:

```
cd notifyme
```

Configure Environment Variables: Create a .env file in the root of the project and add the following environment variables:

```
APP_ADMIN=your_admin_email@example.com
MAILGUN_URL=your_mailgun_url
MAILGUN_API_KEY=your_mailgun_api_key
MAILGUN_FROM=your_mailgun_from_email@example.com
```

Replace the placeholders with your actual admin email, Mailgun API details, and the from email address.

## Running NotifyMe

1. Start MongoDB: Ensure your MongoDB server is running. If you're using the default settings, MongoDB should be listening on localhost:27017.

2. Run the Flask Server: Start the Flask server by executing the following command:

```
python src/run.py
```

The NotifyMe application should now be accessible at `http://localhost:5000` in your web browser.

## Using NotifyMe

1. User Registration: To use the full features of NotifyMe, create an account by clicking on the "Register" link on the top right corner of the page. Provide the required details, and upon successful registration, you'll be redirected to the login page.

2. User Login: After registering, log in using your credentials on the login page.

3. Adding an Item: Once logged in, you can start adding items to track their prices. Click on the "Add Item" button, and you'll be prompted to enter the item's name, URL, and the price threshold below which you want to receive an alert.

4. Managing Alerts: View and manage your alerts by clicking on the "Alerts" link. From here, you can modify the threshold price or delete an alert.

5. Checking Prices: To update and check the prices of all your items, run the following command periodically:

```
python src/alert_updater.py
```

Please be aware that this process can take some time, especially if you are tracking a large number of items.

6. Receiving Alerts: If an item's price drops below the specified threshold, you will receive an email notification to your admin email address.
   Troubleshooting
   If you encounter any issues during setup or usage of NotifyMe, follow these troubleshooting tips:

Verify that you have correctly set up the environment variables for the Mailgun API and your admin email in the .env file.
Double-check that MongoDB is running and accessible at the expected address (localhost:27017 by default).
Ensure you have an active internet connection to fetch prices from online stores.
For any other technical problems, check the application logs in the logs directory for error messages.

## Contributing

We welcome contributions to the NotifyMe project! If you find a bug, have a feature request, or want to improve the application, feel free to submit a pull request on the GitHub repository. Please make sure to follow the guidelines outlined in the CONTRIBUTING.md file.

## Conclusion

Congratulations! You have successfully set up and started using NotifyMe, the price tracking application. Monitor your favorite items' prices, receive alerts, and make smart shopping decisions. If you have any questions or need further assistance, don't hesitate to reach out to the project maintainers or the community. Happy tracking with NotifyMe!
