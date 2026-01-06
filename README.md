# WordPress .htaccess (Apache / LiteSpeed)

**High-Performance .htaccess Configuration for WordPress (2025/2026 Standards)**

Minimalist, secure, and optimized for speed. Follows the **Kanso** principle (simplicity and functionality).

## Features

- **Security**:
  - Disables directory browsing.
  - Protects sensitive system files (`wp-config.php`, `.env`, `.git`).
  - Blocks `xmlrpc.php` (prevents brute force attacks).
  - Implements modern Security Headers (`HSTS`, `X-Frame-Options`, `Referrer-Policy`).
  - Basic firewall to block malicious query strings.
- **Performance**:
  - **Compression**: Auto-enables **Brotli** (if available) or falls back to **GZIP**.
  - **Caching**: Aggressive `Browser Caching` headers for static assets (images, CSS, JS).
  - **LiteSpeed Ready**: Auto-detects LiteSpeed servers (e.g., Hostinger) and applies safe defaults.
- **Compatibility**:
  - Fully compatible with **WooCommerce** (no cart/checkout blocks).
  - Forces **HTTPS** and **Non-WWW** URLs (configurable).

## Installation

1. **Backup** your current `.htaccess` file.
2. **Copy** the content of `.htaccess` from this repository.
3. **Paste** it into your server's `.htaccess` file (root directory).
4. **Test** your site incognito to ensure everything loads correctly.

## Customization

- **WWW vs Non-WWW**: By default, this forces **non-www** (e.g., `example.com`). To force `www`, uncomment the relevant block in Section 2.
- **XML-RPC**: If you use the WordPress Mobile App or Jetpack, comment out the `xmlrpc.php` block in Section 1.

## Requirements

- Apache 2.4+ or LiteSpeed Web Server.
- Modules: `mod_rewrite`, `mod_headers`, `mod_expires`, `mod_deflate` (or `mod_brotli`).

---
*Maintained by zygiu-zygis. Designed for simplicity and speed.*
