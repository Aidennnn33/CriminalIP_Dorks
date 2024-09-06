# Table of Contents

| **Section**                          | **Sub-sections**             |
|--------------------------------------|-------------------------------|
| [Basic Filters](#basic-filters)      | 1) Location 🌍<br>2) Organization & ASN 🏢<br>3) Port & Time Filters ⏲️<br>4) SSL/TLS Certificates 🔒<br>5) Product & Server 🖥️ |
| [Web](#web)                          | Web Filters 🌐                 |
| [Databases](#databases)              | Database Filters 🗃️           |
| [Industrial Control Systems](#industrial-control-systems) | ICS Filters 🏭                |
| [Remote Desktop](#remote-desktop)    | Remote Desktop Filters 💻      |
| [C2 Infrastructure](#c2-infrastructure) | C2 Filters 🕵️‍♂️              |
| [Network Infrastructure](#network-infrastructure) | Network Filters 🌐            |
| [Webcams](#webcams)                  | Webcam Filters 📷              |
| [Printers & Copiers](#printers--copiers) | Printer & Copier Filters 🖨️    |
| [Home Devices](#home-devices)        | Home Device Filters 🏠         |
| [Random Stuff](#random-stuff)        | Random Filters 🎲             |

# Basic Filters


## Location 🌍

| **Filter**   | **Description**                              | **Examples**                              |
|--------------|----------------------------------------------|-------------------------------------------|
| `city:`      | Find devices in a particular city.           | `city: Tokyo`                             |
| `country:`   | Find devices in a particular country.        | `country: IN`                             |
| `hostname:`  | Find devices matching the hostname.          | `hostname: example.com NOT hostname: subdomain.example.com`<br>`hostname: example.com OR hostname: example.org` |
| `net:`       | Find devices based on an IP address or /x CIDR. | `ip: 210.214.0.0/16`                      |

## Organization & ASN

| **Filter**            | **Description**                          | **Examples**               |
|-----------------------|------------------------------------------|----------------------------|
| `org:`                | Find devices by organization.            | `org: Amazon`              |
| `as_name:`            | Find devices by Autonomous System Number (ASN). | `as_name: ASxxxx`         |

## Port & Time Filters

| **Filter**         | **Description**                              | **Examples**                                 |
|--------------------|----------------------------------------------|----------------------------------------------|
| `port:`            | Find devices based on open ports.            | `product: proftpd AND port: 21`             |
| `before/after:`    | Find devices before or after a specific date. | `product: apache AND after: 2022-02-22 AND before: 2024-08-14` |

## SSL/TLS Certificates

| **Filter**                          | **Description**                               | **Examples**                                |
|-------------------------------------|-----------------------------------------------|---------------------------------------------|
| `ssl_expired:`                      | Find expired SSL certificates.                | `ssl_expired: true`                         |
| `ssl_subject_common_name:`          | Find SSL certificates by subject common name. | `ssl_subject_common_name: example.com`     |
| `ssl_issuer_organization:`          | Find SSL certificates by issuer organization. | `ssl_issuer_organization: Let's Encrypt`  |
| `ssl_subject_country:`              | Find SSL certificates by subject country.     | `ssl_subject_country: KR`                  |
| `ssl_subject_organization:`         | Find SSL certificates by subject organization. | `ssl_subject_organization: Fortinet`       |

## Product & Server

| **Filter**           | **Description**                           | **Examples**                         |
|----------------------|-------------------------------------------|--------------------------------------|
| `product:`           | Find devices by product.                  | `product: apache`<br>`product: nginx` |
| `server:`            | Find devices by server type.              | `server: nginx`<br>`server: apache`  |

# Web

## Web Filters

| **Filter**                          | **Description**                                           | **Examples**                               |
|-------------------------------------|-----------------------------------------------------------|--------------------------------------------|
| `dana-na`                           | Pulse Secure                                            | `dana-na`                                  |
| `title:`                            | Find PEM certificates by title.                          | `title: Index of ".pem"`                   |
| `onion-location`                    | Find Tor / Dark Web sites.                               | `onion-location`                           |

# Databases

## Database Filters

| **Filter**               | **Description**                                   | **Examples**                        |
|--------------------------|---------------------------------------------------|-------------------------------------|
| `product: MySQL`         | Find MySQL databases.                            | `product: MySQL AND port: 3306`     |
| `product: MongoDB`       | Find MongoDB databases.                          | `product: MongoDB AND port: 27017`   |
| `product: CouchDB`       | Find CouchDB databases.                          | `product: CouchDB`<br>`port: 5984 AND product: CouchDB/2.1.0` |
| `port: 5432`             | Find PostgreSQL databases.                       | `port: 5432 AND product: PostgreSQL`  |

# Industrial Control Systems

## ICS Filters

| **Filter**                        | **Description**                                  | **Examples**                               |
|-----------------------------------|--------------------------------------------------|--------------------------------------------|
| `product: Prismview Player`       | Samsung Electronic Billboards.                   | `product: Prismview Player`                |
| `port: 10001 AND in-tank inventory` | Gas Station Pump Controllers.                    | `port: 10001 AND in-tank inventory`       |
| `P372 AND ANPR enabled`           | Automatic License Plate Readers.                 | `P372 AND ANPR enabled`                   |
| `mikrotik AND streetlight`        | Traffic Light Controllers / Red Light Cameras.   | `mikrotik AND streetlight`               |

# Remote Desktop

## Remote Desktop Filters

| **Filter**                                    | **Description**                       | **Examples**                        |
|-----------------------------------------------|---------------------------------------|-------------------------------------|
| `service_name: VNC AND port: 5900 OR port: 5901` | Unprotected VNC                        | `service_name: VNC AND port: 5900 OR port: 5901` |
| `authentication disabled AND RFB 003.008`    | Windows RDP (No equivalent filter)     | `authentication disabled AND RFB 003.008` |

# C2 Infrastructure

## C2 Filters

| **Filter**                          | **Description**                        | **Examples**                          |
|-------------------------------------|----------------------------------------|---------------------------------------|
| `product: cobalt strike team server` | CobaltStrike Servers                    | `product: cobalt strike team server`  |
| `ssl: Covenant AND http.component: Blazor` | Covenant                                | `ssl: Covenant AND http.component: Blazor` |

# Network Infrastructure

## Network Filters

| **Filter**                                 | **Description**                                         | **Examples**                                        |
|--------------------------------------------|---------------------------------------------------------|-----------------------------------------------------|
| `hacked-router-help-sos`                   | Hacked routers                                         | `hacked-router-help-sos`                           |
| `product: Redis key-value store`           | Redis open instances                                    | `product: Redis key-value store`                   |
| `title: Weave Scope AND http.favicon.hash: 567176827` | Weave Scope Dashboards                                  | `title: Weave Scope AND http.favicon.hash: 567176827` |

# Webcams

## Webcam Filters

| **Filter**                       | **Description**                              | **Examples**                            |
|----------------------------------|----------------------------------------------|-----------------------------------------|
| `title: camera`                  | Generic camera search                       | `title: camera`                         |
| `webcam AND has_screenshot: true` | Webcams with screenshots                     | `webcam AND has_screenshot: true`       |
| `Server: yawcam AND Mime-Type: text/html` | Yawcams                                  | `Server: yawcam AND Mime-Type: text/html` |

# Printers & Copiers

## Printer & Copier Filters

| **Filter**                           | **Description**                                 | **Examples**                           |
|--------------------------------------|-------------------------------------------------|----------------------------------------|
| `Server: KS_HTTP AND 200 OK`         | Canon Printers                                  | `Server: KS_HTTP AND 200 OK`            |
| `Server: EPSON-HTTP AND 200 OK`      | Epson Printers                                  | `Server: EPSON-HTTP AND 200 OK`         |

# Home Devices

## Home Device Filters

| **Filter**                        | **Description**                             | **Examples**                              |
|-----------------------------------|---------------------------------------------|-------------------------------------------|
| `Server: AV_Receiver AND HTTP/1.1 406` | Yamaha Stereos                           | `Server: AV_Receiver AND HTTP/1.1 406`   |
| `08_airplay AND port: 5353`       | Apple AirPlay Receivers                     | `08_airplay AND port: 5353`              |

# Random Stuff

## Random Filters

| **Filter**                             | **Description**                      | **Examples**                                    |
|----------------------------------------|--------------------------------------|-------------------------------------------------|
| `Server: calibre AND http.status: 200 AND http.title: calibre` | Calibre libraries                  | `Server: calibre AND http.status: 200 AND http.title: calibre` |
| `Minecraft Server AND protocol 340 AND port: 25565` | Too Many Minecraft Servers         | `Minecraft Server AND protocol 340 AND port: 25565`             |
| `ip: 175.45.176.0/22 OR ip: 210.52.109.0/24 OR ip: 77.94.35.0/24` | Literally Everything in North Korea | `ip: 175.45.176.0/22 OR ip: 210.52.109.0/24 OR ip: 77.94.35.0/24` |
