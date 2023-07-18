# Whatsapp_Alert_Esp32
WhatsApp API Message Sender using CallMeBot (Arduino IDE)
This Arduino sketch allows you to send messages via WhatsApp using the CallMeBot API. The code is specifically designed for the ESP32 board, making it ideal for IoT projects or home automation systems that require automated messaging functionality.

Features:
Easy Setup: The sketch utilizes the WiFiManager library to easily connect the ESP32 to a WiFi network. This eliminates the need for hardcoded credentials and simplifies the setup process.

Message Customization: The sketch allows you to customize the message content dynamically by passing a string to the sendMessage function.

WhatsApp API Integration: The sketch interacts with the CallMeBot API to send WhatsApp messages. It uses an API key and a specified phone number to send messages programmatically.

Error Handling: The code includes basic error handling by checking the HTTP response code when sending the message. If there's an error, it will print the response code to the serial monitor.

Low Resource Consumption: The code implements WiFi disconnection and puts the ESP32 into deep sleep after sending the message. This helps reduce power consumption in battery-operated projects.

Usage:
Replace the phoneNumber variable with the target phone number in international format (including the country code) to which you want to send the message.

Obtain an API key from CallMeBot by registering on their website and replace the apiKey variable with your API key.

Customize the message you want to send by passing it as an argument to the sendMessage function in the setup() function.

Upload the sketch to your ESP32 board using the Arduino IDE.

Open the Serial Monitor to observe the progress. It will show "connected...yeey :)" if the WiFi connection is successful and print "Message sent successfully" when the message is sent.

After sending the message, the ESP32 will disconnect from WiFi and enter deep sleep mode to save power. To make it operational again, you can trigger the board by connecting GPIO16 to the RST pin or by pressing the RST button.

With this Arduino sketch, you can easily add WhatsApp messaging capabilities to your ESP32-based projects, enabling you to send important alerts, notifications, or status updates directly to your WhatsApp contacts.
