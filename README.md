# Notes for myself on how I set up Watson IOT on bluemix for Galway Hackathon

1. go to Bluemix platform, log in.
2. go to Catalogue page, choose to create Watson IoT platform instance.
3. go to the URL of my instance, follow instructions to set up Node-RED password.
4. go back to main dashboard, under services, select the iot platform, under connect your devices, chose Launch Dashboard, choose Devices in menu, click Add Device button. Create device type (for I have no device there yet), click through the rest till add device, type in device ID 
5. Configure your Andoird phone to send MQTT messages. The easy way is to install: https://ibm.box.com/v/iotstarterapp (might need to change settings > security first ). *Beware that you need to create a device type called Android (case sensitive) and register your device under this category!*
6. Create Boards and Cards: https://console.ng.bluemix.net/docs/services/IoT/data_visualization.html

## Useful Links
Gentle Start / Play Around (eg. scan a QR code to add your device for demo)
http://www.ibm.com/cloud-computing/bluemix/internet-of-things/

Getting Started
https://console.ng.bluemix.net/docs/services/IoT/index.html

Connecting Devices
https://console.ng.bluemix.net/docs/services/IoT/iotplatform_task.html#iotplatform_task
https://console.ng.bluemix.net/docs/services/IoT/devices/api.html
https://console.ng.bluemix.net/docs/services/IoT/reference/security/connect_devices_apps_gw.html
https://console.ng.bluemix.net/docs/services/IoT/gateways/mqtt.html

Watson IoT Platform HTTP REST API
https://docs.internetofthings.ibmcloud.com/swagger/v0002.html

Recipe for connecting your smart phone to Watson IoT as a device
https://www.ibm.com/developerworks/library/iot-mobile-phone-iot-device-bluemix-apps-trs/
https://developer.ibm.com/recipes/tutorials/practice-watson-iot-platform-with-smart-phone-as-device/

Collection of step-by-step Recipes related to IoT
https://developer.ibm.com/recipes/?post_type=tutorials&s=IoT

Create Boards and Cards, and rules for analytics:
https://console.ng.bluemix.net/docs/services/IoT/analytics.html
https://developer.ibm.com/recipes/tutorials/using-rules-and-actions-with-ibm-watson-iot-platform-cloud-analytics/

