# Passion for home automation? look here

![immagine](https://user-images.githubusercontent.com/68069659/105637074-c5531480-5e6b-11eb-87ab-532952ba2198.png)

In this guide we will explain in a simple way how to have a safe and fun home automation management.

**requirements**: [home assistant](https://www.home-assistant.io/) and [node red](https://nodered.org/).

# step 1: node red

![immagine](https://user-images.githubusercontent.com/68069659/105636982-3cd47400-5e6b-11eb-95ea-3b91686dbdfd.png)

Install node red not as an addon, but as a separate installation from home assistant. you can install it in 

[windows](https://nodered.org/docs/getting-started/windows), 

if you have a mini pc, or with [proxmox](https://nodered.org/docs/getting-started/local).

# step 2: zigbee2mqtt

![immagine](https://user-images.githubusercontent.com/68069659/105637572-8bcfd880-5e6e-11eb-89a3-22ab72d7e355.png)

Install [zigbee2mqtt](https://www.zigbee2mqtt.io/) outside home assistant. you can do it with [windows](https://www.zigbee2mqtt.io/information/windows.html) or with 

[proxmox](https://www.zigbee2mqtt.io/getting_started/running_zigbee2mqtt.html) in a LXC Container or in a VM .

# step 3: broker mqtt

![immagine](https://user-images.githubusercontent.com/68069659/105637829-be2e0580-5e6f-11eb-9cc6-87c9c9ac58f5.png)

install the [aedes](https://flows.nodered.org/node/node-red-contrib-aedes) node, and configure the broker before creating 

flows.

![immagine](https://user-images.githubusercontent.com/68069659/105637962-75c31780-5e70-11eb-85cd-b02a251ae9ef.png)

In home assistant search integration **mqtt**  points towards **aedes**

![immagine](https://user-images.githubusercontent.com/68069659/105638095-2b8e6600-5e71-11eb-9e69-dc713c243405.png)

In Proxmox VM/Container or same Linux Server use this guide

[Ubuntu 18.04](https://github.com/william89731/passion-for-home-automation/blob/main/Install%20Mosquitto%20Broker%20Ubuntu%2018.pdf)


# step 3b: reverse proxy (optional, but strongly recommended)

![immagine](https://user-images.githubusercontent.com/68069659/105638263-064e2780-5e72-11eb-86f5-92418370e904.png)

To increase the security of your home automation, [mattiols reverse proxy](https://github.com/andrea-mattioli/mattiols_hassio_repository/tree/master/mattiols_reverse_proxy) 

is strongly recommended. this guy did a great job.

# step 5: your device in google home. Easy and free!


![20210127_221534](https://user-images.githubusercontent.com/68069659/106055336-82a06f00-60ed-11eb-8ec9-6b4bb6917a9c.gif)

Install node [googlehome](https://flows.nodered.org/node/node-red-contrib-googlehome) and fllow this [guide](https://googlehome.hardill.me.uk/docs) to add your devices in google 

home:

**light**

![20210127_222619](https://user-images.githubusercontent.com/68069659/106056680-381ff200-60ef-11eb-95ec-0f3a19025ecd.gif)

Ihis is the flow to control your light: 

![immagine](https://user-images.githubusercontent.com/68069659/105639391-647e0900-5e78-11eb-9a60-645298b44ec6.png)

[Here](https://github.com/william89731/passion-for-home-automation/blob/main/flows.json) you will find the code

**Outlet**

![20210127_223617](https://user-images.githubusercontent.com/68069659/106057761-b7fa8c00-60f0-11eb-8ade-fba82faadd50.gif)

Switch your power outlet:

![immagine](https://user-images.githubusercontent.com/68069659/106058354-6b638080-60f1-11eb-955f-df26e3b25905.png)

do you want the code? look [here](https://github.com/william89731/passion-for-home-automation/blob/main/outlet.json)

**Scene**

![immagine](https://user-images.githubusercontent.com/68069659/106324701-e657a300-6279-11eb-8208-ed2d9caaa462.png)

Here you can expand the possibilities of your home automation by controlling your flows with the voice commands of google assistant:

![immagine](https://user-images.githubusercontent.com/68069659/106324866-2cad0200-627a-11eb-8fa9-574cd1b20903.png)

code [here](https://github.com/william89731/passion-for-home-automation/blob/main/scena.json)



**thermostat**
Using MQTT Node

![immagine](https://github.com/william89731/passion-for-home-automation/blob/main/ClimateMQTT.jpg)

code [here](https://github.com/william89731/passion-for-home-automation/blob/main/ClimateMQTT.json)

Using Home Assistant Node

![immagine](https://github.com/william89731/passion-for-home-automation/blob/main/Clima_HA_node.jpg)

code [here](https://github.com/william89731/passion-for-home-automation/blob/main/Climate_HA_node.json)
















