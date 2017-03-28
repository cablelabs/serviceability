# An Ethernet Services Serviceability API

This repository contains an example Serviceability API that meets the business requirements being documented by the MEF Ethernet Serviceability Project.

Serviceability provides an API to help determine if a particular service is available (or could be made available) via a particular medium (e.g. Fiber, HFC) at a particular location by a particular Seller. Serviceability also provides fluid transitions to the quoting and site survey processes. The result of a Serviceability Request is a Serviceability Response that contains Product Offerings (quotations) that the Buyer may order from the Seller.

> **IMPORTANT**: This project is in pre-release development. Please expect frequent changes and updates.

**Repository Structure**

| Folder | Contents |
| ------ | -------- |
| `/documentation` | Markdown files containing documentation for this repository. |
| `/endpoints` | JSON files that describe the various API endpoints |
| `/example-data` | Example JSON files for Serviceability |
| `/schemas` | JSON Schema files for Serviceability |

The best place to start is the [Serviceability Markdown file in the documentation directory](/documentation/serviceability.md)

## Other important stuff

We use an [MIT License](LICENSE).
