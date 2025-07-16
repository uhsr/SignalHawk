# SignalHawk - Real-time Signal Processing and Visualization

SignalHawk is a TypeScript-based application designed for real-time processing, analysis, and visualization of signal data. It provides a robust platform for developers and researchers to build custom signal processing pipelines, leveraging modern web technologies for efficient data handling and interactive visualization. This project aims to offer a modular and extensible framework for various signal processing applications, from audio analysis to sensor data interpretation.

SignalHawk addresses the need for a flexible and accessible tool for signal processing. Many existing solutions are either tied to specific hardware, lack real-time capabilities, or have a steep learning curve. By utilizing TypeScript and leveraging web-based visualization libraries, SignalHawk offers a platform-independent solution that can be easily integrated into existing workflows. The core functionality includes data ingestion from various sources, a configurable signal processing pipeline, and interactive visualization components.

The primary goal is to empower users to quickly prototype and deploy signal processing applications without being constrained by platform limitations. SignalHawk is designed to be modular, allowing developers to easily add new signal processing algorithms and visualization techniques. This modularity ensures that the application can evolve to meet the changing demands of the signal processing community. Furthermore, the use of TypeScript promotes code maintainability and reduces the risk of runtime errors, making SignalHawk a reliable and scalable solution.

## Key Features

*   **Real-time Data Ingestion:** Supports various data sources, including WebSocket streams, file uploads (CSV, JSON), and simulated data generation. Implements efficient data buffering to ensure smooth operation even with high-frequency data streams.
*   **Configurable Signal Processing Pipeline:** Allows users to define a sequence of signal processing modules (e.g., FFT, filtering, noise reduction) through a graphical interface or configuration file. Each module can be individually configured with specific parameters.
*   **Modular Architecture:** Designed with a plugin-based architecture, enabling developers to easily add new signal processing algorithms and visualization techniques. Implements a well-defined API for creating custom modules.
*   **Interactive Visualization:** Provides a range of interactive visualization components, including time-domain plots, frequency-domain plots, spectrograms, and scatter plots. Uses Canvas API for high-performance rendering of large datasets.
*   **Data Export:** Enables users to export processed data in various formats (CSV, JSON) for further analysis or integration with other tools. Includes options for specifying data range and sampling rate.
*   **TypeScript Implementation:** Built with TypeScript, providing strong typing and improved code maintainability. Leverages modern JavaScript features for efficient data processing.
*   **Web-Based Interface:** Utilizes a web-based interface for easy access and platform independence. Compatible with modern web browsers on desktop and mobile devices.

## Technology Stack

*   **TypeScript:** Provides strong typing and improves code maintainability.
*   **Node.js:** Used for server-side development and data processing.
*   **Express.js:** A minimalist web framework for building APIs.
*   **WebSocket:** Enables real-time data streaming and communication between the server and client.
*   **Chart.js/D3.js (choose one):** Used for creating interactive data visualizations. Chart.js is simpler, while D3.js offers more customization.
*   **Webpack:** A module bundler for packaging the application for deployment.

## Installation

1.  **Prerequisites:** Ensure you have Node.js (version 16 or later) and npm (Node Package Manager) installed on your system.

2.  **Clone the Repository:**
    git clone https://github.com/uhsr/SignalHawk.git
    cd SignalHawk

3.  **Install Dependencies:**
    npm install

4.  **Build the Application:**
    npm run build

## Configuration

The application can be configured using environment variables. Create a `.env` file in the root directory of the project with the following variables:

*   `PORT`: The port number the server will listen on (default: 3000).
*   `DATA_SOURCE`: The type of data source to use (e.g., 'websocket', 'file', 'simulated').
*   `WEBSOCKET_URL`: The URL of the WebSocket server (if `DATA_SOURCE` is 'websocket').
*   `FILE_PATH`: The path to the data file (if `DATA_SOURCE` is 'file').

Example `.env` file:

PORT=3000
DATA_SOURCE=simulated

## Usage

1.  **Start the Server:**
    npm start

2.  **Access the Application:** Open your web browser and navigate to `http://localhost:3000` (or the port specified in your `.env` file).

3.  **Data Source Configuration:** Configure the data source in the application settings. For WebSocket, enter the URL of the WebSocket server. For file uploads, select the data file. For simulated data, adjust the simulation parameters.

4.  **Signal Processing Pipeline Configuration:** Define the signal processing pipeline by adding and configuring modules. Available modules include FFT, filtering, and noise reduction.

5.  **Visualization:** The processed data will be visualized in real-time using the interactive visualization components. Use the controls to zoom, pan, and adjust the visualization settings.

## Contributing

We welcome contributions to SignalHawk! Please follow these guidelines:

*   Fork the repository.
*   Create a new branch for your feature or bug fix.
*   Write clear and concise commit messages.
*   Submit a pull request with a detailed description of your changes.
*   Ensure your code adheres to the project's coding standards.

## License

This project is licensed under the MIT License. See the [LICENSE](https://github.com/uhsr/SignalHawk/blob/main/LICENSE) file for details.

## Acknowledgements

We would like to thank the open-source community for providing the tools and libraries that made this project possible.