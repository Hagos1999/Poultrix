Poultrix: IoT & AI-Powered Poultry Monitoring System 
Poultrix is an affordable, solar-powered IoT and AI system designed to reduce poultry mortality for smallholder farmers in Nigeria. Built for resource-constrained environments, it uses an ESP8266 microcontroller, Grove sensors, and a WhatsApp chatbot to deliver real-time environmental insights, supporting food security and economic empowerment.OverviewPoultrix addresses high poultry mortality due to poor monitoring in rural Nigeria, where power, connectivity, and funds are scarce. Key features:Hardware: Grove sensors (temperature, humidity, gas) on an ESP8266 (~80 mW), powered by a solar module for off-grid use.
Software: Local data logging, Firebase cloud dashboard, and WhatsApp-based LLM chatbot for farmer-friendly insights (e.g., “Temperature: 30°C, adjust ventilation”).
Business Model: Rentals and cooperative-based brooding make it accessible to smallholder farmers.
Future Plans: Google Forms platform to connect farmers to markets and sensor data for disease control (e.g., ammonia > 25 ppm).

Developed for the Africa Deep Tech Challenge 2025, Poultrix showcases innovation in resource-constrained computing, leveraging local components and familiar tech (WhatsApp) to drive impact.FeaturesLow-Power Design: ESP8266 optimizes power usage, critical for rural deployment.
Solar-Powered: Ensures reliability in off-grid areas, aligning with sustainability goals.
Offline Capability: Local data logging supports low/no connectivity.
User-Friendly: WhatsApp chatbot delivers insights in simple English, with Hausa support planned.
Scalable: Modular design suits small and large farms, with rental/cooperative models.
Impact-Driven: Reduces poultry losses, boosts farmer incomes, and supports food security.

Development JourneyInspiration: Witnessing poultry losses in Nigeria due to unreliable power and limited resources.
Pivots:Switched from Raspberry Pi (~3 W) to ESP8266 for cost and power efficiency.
Moved from one-time purchases to rentals/cooperatives for affordability.
Adopted solar power to overcome grid outages.

Challenges: Funding, AI integration (Hausa support pending), and testing the PID-controlled heating system (target: 32°C).
Future Vision: Market access via Google Forms and data-driven disease control.

Getting StartedPrerequisitesHardware:ESP8266 (e.g., NodeMCU)
Grove sensors (BME680 for temperature, humidity, gas)
Solar panel (12V) with battery and charge controller

Software:Arduino IDE
Libraries: Zanshin_BME680, FirebaseESP8266, WiFi, Time
Firebase account (https://firebase.google.com/)
WhatsApp API (e.g., Twilio, placeholder in code)

InstallationClone the Repository:bash

git clone https://github.com/your-username/poultrix.git
cd poultrix

Install Libraries:In Arduino IDE, go to Sketch > Include Library > Manage Libraries.
Install Zanshin_BME680, FirebaseESP8266, WiFi, and Time.

Configure Credentials:Create a config.h file in the project directory:cpp

#define WIFI_SSID "your_wifi_ssid"
#define WIFI_PASSWORD "your_wifi_password"
#define DATABASE_URL "your_firebase_url"
#define DATABASE_SECRET "your_firebase_secret"

Ensure config.h is listed in .gitignore to protect sensitive data.

Upload Code:Open poultrix.ino in Arduino IDE.
Connect your ESP8266 via USB.
Select Tools > Board > NodeMCU 1.0 (ESP-12E Module) and upload.

Test Setup:Monitor Serial output (115200 baud) for sensor data.
Verify Firebase logging and test WhatsApp alerts (placeholder in code).

UsageDeploy: Connect sensors and solar module to the ESP8266 in a poultry pen.
Monitor: View real-time data on the Firebase dashboard or receive WhatsApp alerts.
Scale: Use the rental/cooperative model to deploy across farmer groups.

Directory Structure

poultrix/
├── poultrix.ino          # Main Arduino sketch
├── config.h             # Wi-Fi and Firebase credentials (not committed)
├── README.md            # Project documentation
├── .gitignore           # Excludes config.h and sensitive files
└── docs/                # Additional docs (e.g., schematics, future plans)

Future PlansMultilingual Support: Add Hausa to the WhatsApp chatbot for inclusivity.
Market Access: Launch a Google Forms platform to connect farmers with buyers.
Disease Control: Use sensor data (e.g., ammonia > 25 ppm) for predictive health monitoring.
Expansion: Scale rentals/cooperatives across Nigeria, creating jobs in assembly and training.

ContributingContributions are welcome! Please:Fork the repo.
Create a feature branch (git checkout -b feature/your-feature).
Commit changes (git commit -m "Add feature").
Push to the branch (git push origin feature/your-feature).
Open a Pull Request.

LicenseThis project is licensed under the MIT License. See LICENSE for details.AcknowledgmentsAfrica Deep Tech Challenge 2025 for inspiring resource-constrained innovation.
Plateau State Government for early recognition.
Local Farmers for feedback shaping Poultrix’s design.

