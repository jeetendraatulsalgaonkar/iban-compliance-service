# iban-compliance-service

# IBAN Checker Microservice

This microservice validates IBANs (International Bank Account Numbers) present in PDF documents fetched from a URL. It checks whether any of the IBANs are blacklisted, stored in a PostgreSQL database. Additionally, it supports PDF extraction, IBAN validation, and integration with Kafka for processing blacklisted IBANs.

## Features:
- **Validate URL**: Ensures the URL is valid and accessible.
- **PDF Parsing**: Extracts IBANs from PDF files using Apache PDFBox.
- **Blacklist Check**: Validates IBANs against a blacklist stored in PostgreSQL.
- **Kafka Integration**: Consumes messages of blacklisted IBANs to add to the database.
- **Error Handling**: Proper error handling for various scenarios like invalid URLs, no IBAN found, and more.

## Prerequisites

Before setting up the microservice, ensure you have the following:

- **Java 23**: The project uses Java version 23.
- **Spring Boot 3.5.0-SNAPSHOT**: The latest version of Spring Boot.
- **PostgreSQL**: The database where blacklisted IBANs are stored.
- **Redis**: For caching.
- **Apache Kafka**: For consuming blacklisted IBANs.
- **Maven**: For building the project.

### Software Dependencies:

1. **JDK 23** – To run the Spring Boot application.
2. **Maven** – For building and managing the project.
3. **PostgreSQL** – A relational database to store blacklisted IBANs.
4. **Kafka** – For processing and storing blacklisted IBANs.
5. **Redis** – To store blacklisted IBANs in cache for faster access.

## Getting Started

### Step 1: Clone the Repository

```bash
git clone https://github.com/yourusername/iban-checker-microservice.git
cd iban-checker-microservice
```
