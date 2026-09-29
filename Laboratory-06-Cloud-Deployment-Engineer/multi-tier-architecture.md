# Two-Tier Architecture

## What is Two-Tier Architecture?

Two-tier architecture separates a system into two major layers that work together. In this activity, Nextcloud handles the application side while MariaDB manages the stored data.

## Web/Application Tier

The web/application tier is where users interact with Nextcloud through a web browser. It processes user requests and provides the features needed to manage files and accounts.

## Database Tier

The database tier keeps the information that Nextcloud needs to operate properly. MariaDB stores details such as user information, settings, and file-related records.

## Why Separate Them?

Keeping the application and database in separate containers gives each part its own role. This makes the system easier to organize, update, troubleshoot, and manage.
