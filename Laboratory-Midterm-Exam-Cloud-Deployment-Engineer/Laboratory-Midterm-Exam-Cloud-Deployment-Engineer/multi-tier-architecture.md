# Two-Tier Architecture

## Definition

A **Two-Tier Architecture** separates an application into two main layers: a web/application tier and a database tier. In this laboratory, Nextcloud represents the web/application tier while MariaDB represents the database tier.

## The Web/Application Tier

The web/application tier is responsible for interacting with users and handling application requests. In this activity, the Nextcloud container provides the web interface and processes HTTP requests from the browser.

## The Database Tier

The database tier stores persistent application data. MariaDB is used by Nextcloud to store information such as user accounts, configuration information, and file metadata.

## Why Separate Them?

Separating the web/application server and database into different containers makes the system easier to manage, update, and scale. It also keeps responsibilities separated, so changes to one component can be made without placing both application and database services inside the same container.

## Architecture

```text
User / Browser
      |
      | HTTP :8080
      v
+----------------------+
| Nextcloud App        |
| Web/Application Tier |
+----------------------+
          |
          | Docker network
          v
+----------------------+
| MariaDB              |
| Database Tier        |
+----------------------+
```

## Student Note

Add or revise details based on what you actually observed during your deployment.
