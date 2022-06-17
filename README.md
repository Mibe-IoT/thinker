# Thinker

Thinker is the *brain* of mibe-iot smart-house network.

## Introduction

Thinker is simple realisation of smart-house network. It offers you a possibility to set up a smart house network upon
any existing LAN/WLAN. Thinker requires you to configure SSID and password of your WLAN network, and, after that the
system is ready-to-go.

Thinker consists of two applications: back-end and front-end. Back-end is implemented using Kotlin and Spring Boot.
Front-end is a ReactJS application. To learn more about each of them
see [front-end repository](https://github.com/mibe-iot/thinker-frontend)
and [back-end repository](https://github.com/mibe-iot/thinker-backend).

You could easily run the whole system using docker-compose tool. You can find docker-compose in this repository.

See related mibe iot projects:

- **IOT device mirror:** https://github.com/mibe-iot/mirror
- **IOT Sample device:** https://github.com/mibe-iot/bit

## Features

1. **Thinker doesn't require internet connection**. Whole iot network could be built upon WLAN, that doesn't even have a
   gateway.
2. **Thinker has open interface specification** built on top of high-level, easy to understand and use technologies. It
   uses
   Bluetooth for device pairing and configuration and MQTT for the further device communication. To learn more about
   device configuration and communications,
   see [thinker back-end documentation](https://github.com/mibe-iot/thinker-backend#device-connection-contract).
3. **Thinker is hardware-independent**. The only problem you could have running this application is bluetooth adapter
   configuration.
   See [thinker back-end system requirements](https://github.com/mibe-iot/thinker-backend#system-requirements) to learn
   how you can avoid this issue.
4. **Thinker has GUI** that is easy-to-use and that could be run on any device with web browser.
   See [thinker front-end repository](https://github.com/mibe-iot/thinker-frontend) to learn more about thinker's GUI.
5. **Thinker is open-source**. If you like this project and want to change something or to contribute to our project -
   feel
   free to fork it and do whatever you want.
6. **Thinker is extensible**. We built system with flexibility in mind. System doesn't wait specific device
   implementation.
   Instead of this configuration process includes discovering device characteristics: how this device is called and what
   actions it could perform.

## Running thinker

Thinker depends on MongoDB and MQTT broker. Don't worry, we already included both of them ass services to
the `docker-compose` script. 

**Also note that you need to provide `.env` file.** This repository contains `.env.example` ([see it](./.env.example)) to give you
an example of `.env` content.

The only thing you need to do after cloning this repository is to run:

```shell
docker-compose up -d
```

This will run thinker in background container. After a minute application GUI will be available on port `:80` and
backe-nd on port `:8080`. If you'd like to configure something or to run application from sources, see sections about
that inside front-end and back-end
repositories: [running back-end from sources](https://github.com/mibe-iot/thinker-backend#running-application-from-sources)
and [running front-end from sources](https://github.com/mibe-iot/thinker-frontend#running-app-from-sources).

## Technologies used

### Back-end technologies

- **Spring Boot.** Official website: https://spring.io/projects/spring-boot
- **Kotlin**. Official website: https://kotlinlang.org/
- **Blessed for BlueZ**. Repository: https://github.com/weliem/blessed-bluez
- **MongoDB**. Official website: https://www.mongodb.com/
- **HiveMQ MQTT** client implementation. Official website: https://www.hivemq.com/
- **Gradle**. Official website: https://gradle.org/

### Front-end technologies

- **React**. Official website: https://reactjs.org/
- **JS**
- **create-react-app**. Official website: https://create-react-app.dev/
- **npm**. Official website: https://www.npmjs.com/
- **RTK**. Official website: https://redux-toolkit.js.org/rtk-query/overview
- **Redux**. Official website: https://redux.js.org/
- **Chakra UI**. Official website: https://chakra-ui.com/
- **Axios**. Repository: https://github.com/axios/axios
- **Formik**. Official website: https://formik.org/docs/overview

## Contacts:

Feel free to reach me out in case of any question:

**Linked-in:** https://www.linkedin.com/in/ilya-buhlakou-33860b205/

**Mail:** ilboogl@gmail.com
