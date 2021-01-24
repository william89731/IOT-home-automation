# passion for home automation? look here

![immagine](https://user-images.githubusercontent.com/68069659/105637074-c5531480-5e6b-11eb-87ab-532952ba2198.png)

in this guide we will explain in a simple way how to have a safe and fun home automation management.

**requirements**: [home assistant](https://www.home-assistant.io/) and [node red](https://nodered.org/).

# step 1: type of installation of home assistant

![immagine](https://user-images.githubusercontent.com/68069659/105637130-20850700-5e6c-11eb-9166-e58db0496291.png)

our advice is to keep the "hot" spots separate. many times tap restart home assistant (example a new sensor in configuration.yaml) and our home automation is out of 

order; in my case i installed home assistant in a [raspberry p4 +](https://www.raspberrypi.org/products/raspberry-pi-4-model-b/), but you can install home assitant with 

[proxmox os]() o [hyper V](https://docs.microsoft.com/en-us/windows-server/virtualization/hyper-v/hyper-v-technology-overview). read [here](https://www.home-assistant.io/hassio/installation/) for more information. 

# step 2: node red

![immagine](https://user-images.githubusercontent.com/68069659/105636982-3cd47400-5e6b-11eb-95ea-3b91686dbdfd.png)

Install node red not as an addon, but as a separate installation from home assistant. you can install it in [windows](https://nodered.org/docs/getting-started/windows), 

if you have a mini pc, or with [proxmox]().

# step 3: zigbee2mqtt

![immagine](https://user-images.githubusercontent.com/68069659/105637572-8bcfd880-5e6e-11eb-89a3-22ab72d7e355.png)

Install [zigbee2mqtt](https://www.zigbee2mqtt.io/) outside home assistant. you can do it with [windows](https://www.zigbee2mqtt.io/information/windows.html) or with 

[proxmox]().

# step 4: broker mqtt

![immagine](https://user-images.githubusercontent.com/68069659/105637829-be2e0580-5e6f-11eb-9cc6-87c9c9ac58f5.png)

install the [aedes](https://flows.nodered.org/node/node-red-contrib-aedes) node, and configure the broker before creating flows.

![immagine](https://user-images.githubusercontent.com/68069659/105637962-75c31780-5e70-11eb-85cd-b02a251ae9ef.png)

in home assistant search integration **mqtt**  points towards **aedes**

![immagine](https://user-images.githubusercontent.com/68069659/105638095-2b8e6600-5e71-11eb-9e69-dc713c243405.png)

# step 4b: reverse proxy (optional but strongly recommended)

![immagine](https://user-images.githubusercontent.com/68069659/105638263-064e2780-5e72-11eb-86f5-92418370e904.png)

To increase the security of your home automation, [mattiols reverse proxy](https://github.com/andrea-mattioli/mattiols_hassio_repository/tree/master/mattiols_reverse_proxy) is strongly recommended. this guy did a great job.


















