---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

**NOTE:** This page is deprecated and will no longer receive updates, please use below site for future updates:

[https://darkxst.github.io/silabs-firmware-builder/](https://darkxst.github.io/silabs-firmware-builder/)


This page allows you to flash Silicon Labs EFR32MG21 based Zigbee dongles directly from your Chrome-based browser.

Supported devices:
* Sonoff ZBDongle-E
* Easyiot ZB-GW04

It will install the most recent builds from [darkxst/silabs-firmware-builder](https://github.com/darkxst/silabs-firmware-builder)  

### Start by clicking `Connect` for your device below.

You can select from these firmware:
* EZSP - Standard Zigbee (NCP) firmware - Baudrate 115200
* MultiPAN RCP - Zigbee + Thread for Silabs Multiprotocol Addon - Baudrate 460800 (230400 for ZB-GW04)
* Openthread RCP - Thread Only - Baudrate 460800 (230400 for ZB-GW04)
* Upload Custom - Provide a custom .gbl firmware file

***NOTE:** Make sure to close anything using your devices serial port (e.g. ZHA, Zigbee2MQTT, Silabs Multiprotocol Add-on)*

> Your browser does not support the WebSerial API. Try Chrome or Edge instead.
{: #notSupported .hidden .serialErr }


-----

## ZBDongle-E
Sonoff Zigbee 3.0 USB Dongle Plus V2 - No hardware flow control  
![ZBDongle-E](./assets/images/dongle-e.png)
<div class="Supported">
    <nabucasa-zigbee-flasher manifest="./assets/manifests/zbdongle-e.json">
        <span slot="button">Connect</span>
    </nabucasa-zigbee-flasher>
</div>
<br>

-----

## ZB-GW04 (v1.2)
Easyiot ZB-GW04 Revision v1.2 - Hardware flow control  
![ZB-GW04](./assets/images/zb-gw04-1v1.png)  

<div class="Supported">
    <nabucasa-zigbee-flasher manifest="./assets/manifests/zb-gw04-v1.2.json">
        <span slot="button">Connect</span>
    </nabucasa-zigbee-flasher>
</div>
<br>

-----


## ZB-GW04 (v1.1)
Easyiot ZB-GW04 Revision v1.1 - No flow control  
![ZB-GW04](./assets/images/zb-gw04-1v1.png)  

<div class="Supported">
    <nabucasa-zigbee-flasher manifest="./assets/manifests/zb-gw04-v1.1.json">
        <span slot="button">Connect</span>
    </nabucasa-zigbee-flasher>
</div>
<br>

-----




<script>
    if(!navigator.serial){
        // const buttons = document.querySelectorAll('.Supported');

        // buttons.forEach(element => {
        //     element.classList.add('hidden');
        // });
        document.getElementById("notSupported").classList.remove('hidden');
    }
</script>