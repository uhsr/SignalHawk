# SignalHawk: Real-time Crypto Anomaly Detection

SignalHawk is a cutting-edge system designed for real-time detection of anomalies in cryptocurrency transaction flows by employing spectral analysis techniques on mempool data. This allows for proactive identification of potentially malicious activities, market manipulation, or unexpected network behaviors, enabling swift responses and informed decision-making. The system is built to be highly adaptable, scalable, and integrates seamlessly with various notification platforms.

SignalHawk leverages the inherent patterns present in mempool transaction data, treating them as time-series signals. By applying spectral analysis, we decompose these signals into their constituent frequencies, revealing underlying periodicities and deviations from established baselines. Significant changes in the spectral characteristics  such as sudden spikes in specific frequencies, shifts in power distribution, or the emergence of previously unseen spectral components  trigger automated alert notifications. These alerts can be customized based on severity thresholds and delivered via configurable channels, ensuring timely awareness of potentially critical events. The system aims to provide a robust and reliable tool for monitoring the health and integrity of cryptocurrency networks.

The primary benefit of SignalHawk lies in its ability to detect subtle anomalies that might be missed by traditional rule-based systems. By focusing on the spectral fingerprint of transaction activity, the system can identify deviations from normal behavior regardless of the specific transaction details. This makes it particularly effective against novel attack vectors and sophisticated manipulation strategies. Furthermore, the real-time nature of the analysis enables immediate response, minimizing potential damage and maximizing opportunities for intervention. The system is designed with modularity in mind, allowing for easy integration of new data sources, analysis techniques, and notification mechanisms.

## Key Features

*   **Real-time Mempool Monitoring:** Continuously monitors incoming transactions in the mempool, providing a stream of data for analysis. Uses a WebSocket connection to a dedicated node to receive transaction data.
*   **Spectral Analysis:** Employs Fast Fourier Transform (FFT) algorithms to analyze the frequency components of transaction data, identifying deviations from established baselines. The window size and overlap ratio are configurable to optimize detection sensitivity. Implemented using the `fftw3.js` library for efficient computation.
*   **Anomaly Detection:** Implements statistical anomaly detection algorithms (e.g., z-score, moving average) on the spectral features to identify significant deviations. Thresholds for anomaly detection are configurable and can be adjusted based on historical data and desired sensitivity.
*   **Automated Alert Notifications:** Triggers configurable alerts upon detection of anomalies, delivering notifications via various channels (e.g., email, Slack, SMS). Uses the `nodemailer` library for email notifications and `node-slack-sdk` for Slack integration.
*   **Customizable Configuration:** Allows for extensive customization of analysis parameters, anomaly detection thresholds, and notification settings. Configuration is managed through environment variables and a configuration file.
*   **Data Persistence:** Stores historical transaction data and anomaly detection results in a database for analysis and reporting. Supports various database systems, including PostgreSQL and MongoDB, configured via environment variables. Uses `TypeORM` for database interaction.
*   **Modular Architecture:** Designed with a modular architecture, allowing for easy integration of new data sources, analysis techniques, and notification mechanisms. Each module is implemented as a separate class with well-defined interfaces.

## Technology Stack

*   **TypeScript:** The primary programming language, providing strong typing and modern language features.
*   **Node.js:** The runtime environment for executing the application.
*   **fftw3.js:** JavaScript library for performing Fast Fourier Transform (FFT) calculations. Used for spectral analysis of transaction data.
*   **TypeORM:** Object-Relational Mapping (ORM) library for interacting with databases.
*   **Nodemailer:** Library for sending email notifications.
*   **node-slack-sdk:** Library for integrating with Slack.
*   **dotenv:** For loading environment variables from a `.env` file.

## Installation

1.  **Clone the repository:**
    git clone https://github.com/uhsr/SignalHawk.git
2.  **Navigate to the project directory:**
    cd SignalHawk
3.  **Install dependencies:**
    npm install
4.  **Create a `.env` file:**
    Copy the `.env.example` file to `.env` and configure the necessary environment variables.
5.  **Configure the database:**
    Ensure that the database specified in the `.env` file is running and accessible.
6.  **Run database migrations:**
    npm run typeorm migration:run
7.  **Build the project:**
    npm run build

## Configuration

The system is configured using environment variables and a configuration file (config.json). The following environment variables are required:

*   `NODE_ENV`: The environment (e.g., `development`, `production`).
*   `DATABASE_TYPE`: The type of database (e.g., `postgres`, `mongodb`).
*   `DATABASE_HOST`: The database host.
*   `DATABASE_PORT`: The database port.
*   `DATABASE_USERNAME`: The database username.
*   `DATABASE_PASSWORD`: The database password.
*   `DATABASE_NAME`: The database name.
*   `EMAIL_HOST`: The email server host.
*   `EMAIL_PORT`: The email server port.
*   `EMAIL_USERNAME`: The email username.
*   `EMAIL_PASSWORD`: The email password.
*   `SLACK_API_TOKEN`: The Slack API token.
*   `SLACK_CHANNEL_ID`: The Slack channel ID.

The `config.json` file contains settings for the spectral analysis and anomaly detection algorithms. These settings can be adjusted to optimize the system's performance for specific cryptocurrency networks.

## Usage

To start the system, run the following command:

npm start

The system will begin monitoring the mempool, performing spectral analysis, and triggering alerts upon detection of anomalies. The API documentation is currently under development.

## Contributing

We welcome contributions to SignalHawk. Please follow these guidelines when contributing:

*   Fork the repository and create a branch for your changes.
*   Write clear and concise commit messages.
*   Submit a pull request with a detailed description of your changes.
*   Ensure that your code adheres to the project's coding style.
*   Write unit tests for your code.

## License

This project is licensed under the MIT License. See the [LICENSE](https://github.com/uhsr/SignalHawk/blob/main/LICENSE) file for details.

## Acknowledgements

We would like to thank the following organizations and individuals for their contributions to this project:

*   The developers of the open-source libraries used in this project.
*   The cryptocurrency community for their valuable feedback and support.