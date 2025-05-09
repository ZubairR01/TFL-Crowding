# TFL Crowding App

## Project Overview
The TFL Crowding App is a web application that allows users to view crowding data for various London Underground stations. The app uses the Transport for London (TFL) API to display real-time crowding data in an easy-to-read format, including a bar chart and a table of peak crowding times.

## Features
- Select a London Underground station and day of the week to view crowding data.
- Visualize crowding percentages throughout the day using a bar chart.
- Display AM and PM peak crowding times.
- View crowding data in a tabular format with 15-minute increments.

## Technologies Used
- HTML: For structuring the web page.
- CSS: For styling the interface.
- JavaScript (jQuery): For making AJAX requests to the TFL API.
- Chart.js: For visualizing crowding data in a bar chart.
- TFL API: For fetching real-time crowding data.

## Installation
1. Clone the repository
```
git clone https://github.com/yourusername/tfl-crowding-app.git
```
2. Navigate to the project directory:
```
cd tfl-crowding-app
```
3. Open the index.html file in your browser:
```
open index.html
```

## Usage
1. Open the app in your browser.
2. Select a tube station and day of the week from the dropdown menus.
3. Click the "Show Results" button.
4. View the crowding data presented in a bar chart and a table.
5. See the AM and PM peak crowding times displayed below the chart.

## API Integration
The app integrates with the TFL API to fetch crowding data for London Underground stations. The API URL is constructed dynamically based on the selected station and day.

## API Endpoint:
```
https://api.tfl.gov.uk/crowding/{naptan}/{day}
```
## Required Headers:
- app_id: Your TFL API key.
- app_key: Your TFL API key.

## Example API Call:
```
$.ajax({
  url: "https://api.tfl.gov.uk/crowding/940GZZLUPAC/mon",
  type: "GET",
  headers: {
    app_id: "your_app_id",
    app_key: "your_app_key"
  },
  success: function (data) {
    console.log(data);
  }
});
```

## Project Structure
```
tfl-crowding-app/
├── index.html        # Main HTML file
├── README.md         # Project README
```

## How to Get TFL API Key
1. Visit the [TFL API Portal](https://api-portal.tfl.gov.uk/).
2. Register for a developer account.
3. Create a new application to obtain your app_id and app_key.

## Troubleshooting
- If the chart does not appear, ensure that:
  - The API key is correctly configured.
  - You have an active internet connection.
  - The TFL API is accessible (sometimes it may be temporarily down).
- Check the browser console (press F12) for error messages.

## License
This project is licensed under the MIT License.

## Contributions
Contributions are welcome! Please feel free to submit a pull request or open an issue.

## Contact
For any questions or feedback, please reach out at zubairrahman1201@gmail.com.
