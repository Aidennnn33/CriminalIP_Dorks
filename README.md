# Criminal IP Dorks

This project is basically an archive of example queries for Criminal IP searches. I’ve organized the filters from Criminal IP, so I can see them all in one place. Each filter is categorized by its purpose, and I’ve included usage examples for each one. 

> [!CAUTION]
> Since it was put together quickly, some of the examples might not work perfect.
> If you run into any issues, just let me know!


## Table of Contents

- [Location 🌍](#location-)
- [ISP (Internet Service Provider) 📶](#isp-internet-service-provider-)
- [Organization 🏢](#organization-)
- [Date Filters 📅](#date-filters-)
- [Domain 🌐](#domain-)
- [Scanner-Related Search 🔍](#scanner-related-search-)
- [Server-Related Search 🖥️](#server-related-search-)
- [SSL-Related Search 🔒](#ssl-related-search-)
- [Vulnerability Search 🦠](#vulnerability-search-)
- [Web-Related Search 🌐](#web-related-search-)
- [Status Code Search 🛠️](#status-code-search-)
- [Technology Stack Search ⚙️](#technology-stack-search-)
- [Combined Search 🔀](#combined-search-)

---

## **Location 🌍**

|   | **Description**            | **Examples**       |
|---|----------------------------|--------------------|
| 1 | Search by City Name        | `city:Central`     |
| 2 | Search by Country Code     | `country:KR`       |

---

## **ISP (Internet Service Provider) 📶**

|   | **Description**            | **Examples**     |
|---|----------------------------|------------------|
| 1 | Search by ISP Name         | `isp:AT&T`       |

---

## **Organization 🏢**

|   | **Description**                    | **Examples** |
|---|------------------------------------|--------------|
| 1 | Search by Organization Name        | `org:Apple`   |

---

## **Date Filters 📅**

|   | **Description**                        | **Examples**             |
|---|----------------------------------------|--------------------------|
| 1 | Search for Data After a Specific Date | `apache after:2022-12-24` |

---

## **Domain 🌐**

|   | **Description**                | **Examples**           |
|---|--------------------------------|------------------------|
| 1 | Search for Domains in Banner   | `domain_from_banner:.com` |

---

## **Scanner-Related Search 🔍**

|   | **Description**                 | **Examples**        |
|---|---------------------------------|---------------------|
| 1 | Search by Specific Port         | `scanner_port:3389` |
| 2 | Search by Scanner Raw Logs      | `scanner_raw:Cookie` |

---

## **Server-Related Search 🖥️**

|   | **Description**                  | **Examples**               |
|---|----------------------------------|----------------------------|
| 1 | Search by Cloud Provider         | `cloud_provider:Azure`     |
| 2 | Search by Hostname               | `hostname:ec2`             |
| 3 | Search by IP Address             | `ip:95.130.170.143`        |
| 4 | Search by Port Number            | `port:22`                  |
| 5 | Search by Product Name           | `product:OpenSSH`          |
| 6 | Search by Product Version        | `product_version:7.9p1`    |
| 7 | Search by Service Name           | `service_name:SSH`         |
| 8 | Search by Tag                    | `tag:Data Leak`            |

---

## **SSL-Related Search 🔒**

|   | **Description**                         | **Examples**                            |
|---|-----------------------------------------|-----------------------------------------|
| 1 | Search by SSL Certificate Expiry        | `ssl_expired:true`                     |
| 2 | Search by SSL Issuer Organization       | `ssl_issuer_organization:Let's Encrypt` |
| 3 | Search by SSL Subject Common Name       | `ssl_subject_common_name:FortiGate`     |
| 4 | Search by SSL Subject Country           | `ssl_subject_country:KR`                |
| 5 | Search by SSL Subject Organization      | `ssl_subject_organization:Fortinet`     |

---

## **Vulnerability Search 🦠**

|   | **Description**                       | **Examples**                                    |
|---|---------------------------------------|-------------------------------------------------|
| 1 | Search by Malware MD5 Hash            | `malcode_md5:af289762e0c3011827452096448adfb1` |
| 2 | Search by Snort Classification        | `snort_classification:ciarmy`                   |
| 3 | Search by Snort Rule                  | `snort_rule:traffic`                            |

---

## **Web-Related Search 🌐**

|   | **Description**                      | **Examples**                              |
|---|--------------------------------------|-------------------------------------------|
| 1 | Search by Favicon Hash               | `favicon:72b36155`                        |
| 2 | Search by HTML Meta Author           | `html_meta_author:Splunk`                 |
| 3 | Search by HTML Meta Description      | `html_meta_description:create-react-app` |
| 4 | Search by HTML Meta Keywords         | `html_meta_keywords:system`              |
| 5 | Search by HTML Meta Title            | `html_meta_title:Marketplace`            |

---

## **Status Code Search 🛠️**

|   | **Description**                          | **Examples**     |
|---|------------------------------------------|------------------|
| 1 | Search by HTTP Server Response Code      | `status_code:200` |

---

## **Technology Stack Search ⚙️**

|   | **Description**                  | **Examples**     |
|---|----------------------------------|------------------|
| 1 | Search by Technology Stack       | `tech_stack:jQuery` |

---

## **Combined Search 🔀**

|   | **Description**                          | **Examples**                   |
|---|------------------------------------------|--------------------------------|
| 1 | AND Condition for Combined Search       | `port:80 AND tag:admin`        |
| 2 | NOT Condition to Exclude Specific Terms | `port:22 NOT country:US`       |
| 3 | OR Condition for Multiple Searches      | `port:8080 OR port:8091`       |
| 4 | Search for Specific Phrases             | `"default password"`           |

---
