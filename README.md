
# 🧩 Config Data Repository

This repository contains the centralized configuration files used by Spring Cloud Config Server in a microservice-based architecture.
## It defines the configuration for:

 - Microservices
 - Eureka Server
 - API Gateway
 
The purpose of this repository is to provide a single source of truth for application configuration across all services.
## 🔐 Security & Credentials

No sensitive information is stored in this repository.

All credentials and sensitive values are externalized using environment variables, which means:

 - Real credentials are not committed
 - Configuration files only define placeholders and structure
 - Secrets are injected at runtime depending on the environment

This allows the repository to remain safe even when shared within the organization.
## ⚙️ Configuration Strategy

 - Uses .properties files per service
 - Supports multiple environments (dev / test / prod)
 - Follows Spring Cloud Config naming conventions
 - Centralizes common properties to avoid duplication
## 🌐 Usage

This repository is consumed by Spring Cloud Config Server, which exposes the configuration to all registered services at startup.

Each microservice retrieves its configuration dynamically based on:

 - application name
 - active profile
 - environment variables
## 🏗️ Architecture Context

 - Spring Boot Microservices
 - Spring Cloud Config
 - Eureka Service Discovery
 - API Gateway

This setup improves maintainability, consistency, and scalability across the system.
## 🔒 Notes

This repository shows how the project must be configured, not the real credentials used in production.
