# WordPress .htaccess "Gold Standard" (2025/2026 Edition)

**The ultimate, high-performance `.htaccess` configuration for WordPress.**

Designed to fix **WordPress slow TTFB**, resolve **missing security headers**, and achieve **Score 100 Google PageSpeed** instantly. Compatible with Apache and LiteSpeed (Hostinger, SiteGround, Bluehost, etc.).

## 🚀 Solves These Problems Instantly
- **Slow Site Speed**: Enables Brotli/GZIP compression and aggressive Browser Caching (1 Year) for instant asset loading.
- **Security Warnings**: Adds HSTS, X-Frame-Options, and blocks `xmlrpc.php` brute force attacks.
- **WooCommerce Issues**: 100% compatible with WooCommerce cart/checkout (prevents cache conflicts).
- **SEO Penalties**: Fixes canonical URL issues (Forces HTTPS & Non-WWW) and improves Core Web Vitals.

## 📦 Features

- **Universal Compatibility**: Works on **Shared Hosting**, **VPS**, and **Cloud** environments. Auto-detects server capabilities (Apache vs. LiteSpeed) without 500 errors.
- **Modern Performance**:
  - **Brotli Compression**: Prioritizes `mod_brotli` for smaller file sizes, falls back to GZIP.
  - **Smart Caching**: Uses `Cache-Control: public` for that "instant load" feeling on modern browsers.
  - **Image Support**: Ready for `.webp` and `.avif` next-gen formats.
- **Security Hardening**:
  - Blocks sensitive files (`wp-config.php`, `.env`, `.git`, `composer.json`).
  - Disables directory browsing.
  - Implements strict security headers.

## 🛠️ Installation

1. **Backup**: Download your existing `.htaccess` file via FTP/File Manager.
2. **Copy**: Copy the entire content of the `.htaccess` file in this repo.
3. **Paste**: Overwrite your server's `.htaccess` file (located in the `public_html` root).
4. **Verify**: Open your site in Incognito mode. Everything should load faster.

## ⚙️ Configuration

### WWW vs. Non-WWW
By default, this file forces **non-www** (e.g., `example.com`).
To force `www` (e.g., `www.example.com`), modify **Section 2**:
1. Comment out the "Force NON-WWW" block.
2. Uncomment the "Force WWW" block (if added) or write the rewrite rule manually.

### XML-RPC
Blocked by default to prevent attacks. If you use the **WordPress Mobile App** or **Jetpack**, find the `xmlrpc.php` block in **Section 1** and comment it out.

---

*Maintained by zygiu-zygis. Follows the **Kanso** principle: Minimal, Functional, Perfect.*
