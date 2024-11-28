# Symfony Project Setup and Update Guide

This document provides detailed instructions for installing the `php-sockets` extension, updating project dependencies, and managing Symfony cache effectively.

---

## Requirements

- **PHP:** 8.2 or higher
- **Docker** (if using containerized environments)
- **Composer:** 2.x

---

## Steps

### 1. Install `php-sockets` Extension

#### For Docker Environments
If you are using Docker, add the following line to your Dockerfile:

```dockerfile
RUN docker-php-ext-install sockets
```

## 2. Review and Update Composer Dependencies
List the Currently Installed Packages
To review the current project dependencies, run the following command and save the output to ```packages.txt```

```composer show > packages.txt```

## 3. Update composer.json Requirements
In your composer.json, ensure the PHP version and Symfony requirements are properly set:

```
"require": {
    "php": ">=8.2",
    "symfony/framework-bundle": "^7.1",
    ...
}
```
## Once updated, run:
```
composer update --with-all-dependencies

```
php bin/console cache:clear
``

