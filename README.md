<!-- readme-seo: bannysukumar-professional-v4 -->

# WhatsApp Bulk Messenger

WhatsApp Bulk Messenger is a CodeIgniter 4 PHP application whose source includes modules for bulk WhatsApp messaging, a WhatsApp API, chatbot, autoresponder, and account management.

## Overview

The repository is a PHP front controller (`index.php`) with application modules under `inc/core`. WhatsApp-related modules in that tree include `Whatsapp_bulk`, `Whatsapp_api`, `Whatsapp_send_message`, `Whatsapp_chatbot`, `Whatsapp_autoresponder`, `Whatsapp_contact`, and `Whatsapp_history`.

The same tree also contains account, plan, payment, and web-push modules. `composer.json` requires PHP 8 and CodeIgniter 4, and it also requires libraries for Google, Facebook, Twitter, mail, CSV, and PDF. This README only describes those modules and dependencies. It does not add behavior that is not in the source.

The repository homepage is https://whatsapp-bulk-messenger-two.vercel.app.

## Features

These names come from directories under `inc/core`:

- WhatsApp bulk, send message, API, chatbot, and autoresponder modules
- WhatsApp contacts, history, profiles, button templates, list-message templates, and poll templates
- Account manager, plans, payments, and subscriptions
- Web push campaign, composer, schedules, and subscriber modules

## Tech Stack

| Technology | Where it shows up |
|---|---|
| PHP 8 | `composer.json` platform and `index.php` |
| CodeIgniter 4 | `composer.json` requirement `codeigniter4/framework` |
| Composer | `composer.json`, `composer test` script |
| PHPUnit | `phpunit.xml.dist` and the Composer `test` script |

## Architecture

Browser or deployed host → `index.php` → CodeIgniter bootstrap in `inc/` → module controllers under `inc/core`.

## Project Structure

```text
whatsapp-Bulk-messenger/
├── app/
├── inc/core/
├── composer.json
├── index.php
├── phpunit.xml.dist
└── spark
```

## Prerequisites

- PHP 8, as set in `composer.json`
- Composer

## Installation

```bash
git clone https://github.com/Bannysukumar/whatsapp-Bulk-messenger.git
cd whatsapp-Bulk-messenger
composer install
```

`index.php` is the front controller. The repository also includes the CodeIgniter `spark` file.

## Configuration

The repository root contains a `.env` file. Do not commit real tokens or paste them into documentation. Use local environment values only on your own machine.

## Usage

Open the application through `index.php` on a PHP host. WhatsApp actions are implemented as separate modules under `inc/core`, including `Whatsapp_bulk` and `Whatsapp_send_message`.

## API

`inc/core/Whatsapp_api` contains `Controllers/Whatsapp_api.php`, `Config/Routes.php`, and `Helpers/Whatsapp_api_helper.php`. Route details are in that module's `Routes.php`.

## Testing

PHPUnit is configured:

```bash
composer test
```

## Demo

https://whatsapp-bulk-messenger-two.vercel.app

## Contributing

Read [CONTRIBUTING.md](CONTRIBUTING.md) before opening a pull request.

## License

Licensed under MIT. See [LICENSE](LICENSE).

## Author

Banny Sukumar

GitHub: https://github.com/Bannysukumar
