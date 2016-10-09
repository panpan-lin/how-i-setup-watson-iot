# Notes for myself on how I set up Watson IOT on bluemix for Galway Hackathon

## Mobile

Actually, you just need to follow this, that's pretty much it:
https://www.ibm.com/developerworks/library/iot-mobile-phone-iot-device-bluemix-apps-trs/
and perhaps this one too (for the node-red thing):
https://console.ng.bluemix.net/docs/starters/IoT/iot500.html#iot500

1. go to Bluemix platform, log in.
2. go to Catalogue page, choose to create Watson IoT platform instance.
3. go to the URL of my instance, follow instructions to set up Node-RED password.
4. go back to main dashboard, under services, select the iot platform, under connect your devices, chose Launch Dashboard, choose Devices in menu, click Add Device button. Create device type (for I have no device there yet), click through the rest till add device, type in device ID 
5. Configure your Andoird phone to send MQTT messages. The easy way is to install: https://ibm.box.com/v/iotstarterapp (might need to change settings > security first ). *Beware that you need to create a device type called __Android__ (case sensitive) and register your device under this category!*
6. Create Boards and Cards: https://console.ng.bluemix.net/docs/services/IoT/data_visualization.html, maybe even set up some rules if you like (optional, go to device > manage schemas to set up schemas first, then go to Rules > Create Cloud Rule)
7. Edit Node-RED in Bluemix
  to connect the default node-red temperature thing, see this: https://console.ng.bluemix.net/docs/starters/IoT/iot500.html#iot500
  

Download the Bluemix Command Line Interface and Cloud Foundary Command Line Interface. (https://console.ng.bluemix.net/docs/starters/install_cli.html)

-----

## TI SimpleLink SensorTag
Following this recipe: https://developer.ibm.com/recipes/tutorials/connect-a-cc2650-sensortag-to-the-iot-foundations-quickstart/

Untill you reach the point to connect to IoTF Platform. Have a look at this documentation:
https://console.ng.bluemix.net/docs/services/IoT/iotplatform_task.html#iotplatform_task

Here are the configurations I use:
* Username: `use-token-auth`
* Password: `<device's authentication token>`
* Device ID: `d:<6-character org id>:<device type>:<device id>`
* Broker Address: `tcp://<6-character org id>.messaging.internetofthings.ibmcloud.com`
* Port: `1883`
* Event topic format: `iot-2/evt/status/fmt/json`

-----

## Useful Commands for Bluemix cli
First of all, cd into your code directory
1. Connect: bluemix api https://api.DomainName
2. Login: bluemix login -u username -o org_name -s space_name
3. Deploy: cf push "app_name"

-----

## Useful Links
### Gentle Start / Play Around (eg. scan a QR code to add your device for demo)
http://www.ibm.com/cloud-computing/bluemix/internet-of-things/

### Getting Started
https://console.ng.bluemix.net/docs/services/IoT/index.html
https://console.ng.bluemix.net/docs/starters/IoT/iot500.html#iot500

### IoT Starter App
http://m2m.demos.ibm.com/iotstarter.html (with link to GitHub code)

### Connecting Devices
https://console.ng.bluemix.net/docs/services/IoT/iotplatform_task.html#iotplatform_task
https://console.ng.bluemix.net/docs/services/IoT/devices/api.html
https://console.ng.bluemix.net/docs/services/IoT/reference/security/connect_devices_apps_gw.html
https://console.ng.bluemix.net/docs/services/IoT/gateways/mqtt.html

### Watson IoT Platform HTTP REST API
https://docs.internetofthings.ibmcloud.com/swagger/v0002.html

### Recipe for connecting your smart phone to Watson IoT as a device
https://www.ibm.com/developerworks/library/iot-mobile-phone-iot-device-bluemix-apps-trs/
https://developer.ibm.com/recipes/tutorials/practice-watson-iot-platform-with-smart-phone-as-device/

### Recipe for connection Raspberry Pi to Watson IoT:
https://developer.ibm.com/recipes/tutorials/raspberry-pi-4/

### Recipe for connecting Intel Galileo to Watson IoT:
https://developer.ibm.com/recipes/tutorials/connect-an-intel-galileo-to-the-internet-of-things-foundation-connect/

### Recipe for connecting TI SimpleLink SensorTag with CC2650 wireless MCU
https://developer.ibm.com/recipes/tutorials/connect-a-cc2650-sensortag-to-the-iot-foundations-quickstart/

### Collection of step-by-step Recipes related to IoT
https://developer.ibm.com/recipes/?post_type=tutorials&s=IoT

### Create Boards and Cards, and rules for analytics:
https://console.ng.bluemix.net/docs/services/IoT/analytics.html
https://developer.ibm.com/recipes/tutorials/using-rules-and-actions-with-ibm-watson-iot-platform-cloud-analytics/

### Bluemix Cli:
https://console.ng.bluemix.net/docs/starters/install_cli.html
http://clis.ng.bluemix.net/ui/home.html
Cloud Foundry Cli:
https://github.com/cloudfoundry/cli/releases

### Watson IOT sample code:
https://github.com/ibm-watson-iot

### Bluemix with Git:
https://console.ng.bluemix.net/docs/starters/deploy_devops.html
