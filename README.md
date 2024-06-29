# Fuel Finder Node.js Server

This repository contains the Node.js server for the Fuel Finder app, which provides real-time fuel availability information to users.

## Project Overview

The server is responsible for:

* **Web Scraping:** Periodically scraping data from gas station websites to gather fuel availability information.
* **Data Processing:**  Implementing a 15-minute algorithm to process the scraped data and determine fuel availability.
* **Push Notifications:**  Communicating with Firebase to send push notifications to users about fuel availability at nearby stations.
* **Microservice:** Providing a microservice API that the React Native app can use to retrieve fuel availability data.

The server runs on a Raspberry Pi and is deployed using GitHub Actions.

## Installation & Setup

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/flow-consulting/fuel-finder-node-server.git
   cd fuel-finder-node-server
   ```

2. **Install Dependencies:**
   ```bash
   npm install
   ```

3. **Configuration:**
   * **Environment Variables:**
     * Create a `.env` file (make sure it's added to your `.gitignore`) and set the following environment variables:
       * `FIREBASE_API_KEY`: Your Firebase API key.
       * `MONGO_URI`: Your MongoDB connection string.
       * (Other environment variables specific to your project)
   * **Database Setup:**
      * Ensure that you have a MongoDB database set up and running. You can use MongoDB Atlas for a cloud-based solution.

## Running the Server

1. **Start the Server:**
   ```bash
   npm start
   ```

## Deployment to Raspberry Pi

1. **Build the Server (if necessary):**
   * If your project requires a build step (e.g., using Webpack or Babel), run `npm run build` to create a production-ready build.

2. **Set up SSH Access to Your Raspberry Pi:**
   * Follow the instructions in the GitHub Actions workflow file to set up SSH access to your Raspberry Pi. 

3. **Push to the `main` Branch:**  
   *  Any push to the `main` branch will trigger the GitHub Actions workflow, which will build and deploy the server to your Raspberry Pi.

## Documentation

* **Firebase Documentation:** [https://firebase.google.com/docs](https://firebase.google.com/docs)
* **MongoDB Documentation:** [https://www.mongodb.com/docs](https://www.mongodb.com/docs)
* **Node.js Documentation:** [https://nodejs.org/en/docs](https://nodejs.org/en/docs)

## Contributing

Contributions are welcome! Please open an issue or submit a pull request for any bug fixes or improvements.

## License

This project is licensed under the MIT License.

## Contact

If you have any questions or feedback, please contact [flow.consulting.bo@gmail.com].

