# WordPress .htaccess for Maximum Speed, Security & SEO

[![Release v1.0.3](https://img.shields.io/badge/release-v1.0.3-blue.svg)](CHANGELOG.md#103---2025-08-21)
[![License: GPL v2](https://img.shields.io/badge/License-GPL%20v2-blue.svg)](LICENSE)

This production-grade `.htaccess` file provides a complete **WordPress .htaccess optimization** solution, designed to be a safe and effective way to improve performance, security, and technical SEO.

---

## 🚀 Key Features & Benefits

- 🔐 **Advanced Security**: Implements modern security headers and rules based on **WordPress .htaccess security best practices** to protect your site from common vulnerabilities.
- ⚡ **Intelligent Caching**: Uses `mod_expires` and `Cache-Control` with `immutable` directives to create a powerful browser caching policy. This is a key step to **fix .htaccess caching WordPress** issues and dramatically improve site speed.
- 🗜️ **Efficient Compression**: Enables GZIP compression for all text-based assets, with an optional (commented-out) block for Brotli for even better performance.
- 📈 **SEO-Ready**: Includes several **WordPress htaccess SEO tweaks** that contribute to better Core Web Vitals and search engine rankings.
- 🌐 **CDN & Hosting Friendly**: Works on Apache, LiteSpeed, and popular hosting platforms. It disables `ETag` to work seamlessly with CDNs.

---

## 🤔 Why This Matters for SEO

A well-configured `.htaccess` file is a cornerstone of technical SEO. Search engines like Google prioritize websites that are fast, secure, and provide a good user experience. Here’s how this configuration helps:

-   **Site Speed:** Faster loading times are a critical ranking factor. By enabling browser caching and GZIP/Brotli compression, this `.htaccess` reduces server response times and the size of your pages, directly improving your PageSpeed Insights score.
-   **Security:** A secure website is a trustworthy website. The security headers and rules in this file help protect your site from common threats, which prevents it from being flagged as unsafe by search engines and protects your SEO rankings from being damaged by a hack.
-   **User Experience:** By preventing mixed-content warnings (via `upgrade-insecure-requests`) and ensuring resources load quickly, this configuration contributes to a smoother experience for your visitors, reducing bounce rates and encouraging longer session durations—both positive signals for SEO.

Proper **WordPress .htaccess optimization** is a powerful way to enhance your site's technical foundation for better search engine visibility.

---

## 🛠 WordPress .htaccess Optimization Guide

1.  **Backup** your current `.htaccess` file.
2.  **Replace** the contents with the file from this repository.
3.  **Customize (Optional)**:
    -   **Hotlink Protection**: To prevent other sites from embedding your images, uncomment the `Hotlink Protection` block and replace `yourdomain\.com` with your actual domain.
    -   **XML-RPC**: If you do not use services that require it (like the Jetpack plugin or the WordPress mobile app), keep the `xmlrpc.php` block enabled. Otherwise, comment it out.
    -   **Brotli Compression**: If your server supports `mod_brotli`, you can get better compression by commenting out the `mod_deflate` (GZIP) section and uncommenting the `mod_brotli` section.
4.  **Validate** your site using tools like [Security Headers](https://securityheaders.com) and [Google PageSpeed Insights](https://pagespeed.web.dev/) to see the improvements.

---

## 💻 Compatibility & Requirements

-   **Servers**: Apache 2.4+, LiteSpeed, Plesk (Apache+NGINX), Cloudways stacks.
-   **Modules**: `mod_rewrite`, `mod_headers`, `mod_deflate`, `mod_alias`, `mod_expires`.

> When using Cloudflare or similar CDNs, prefer managing headers centrally there; this `.htaccess` acts as a robust fallback.

---

## 🔄 Contributing & Versioning

- Use **Conventional Commits** (e.g., `feat:`, `fix:`, `docs:`).
- Test on **staging** before production.
- Tag releases (e.g., `v1.0.3`) with clear change logs.

---

## 📌 What’s New in `v1.0.3`

- **SEO & Discoverability**: Added SEO-focused keywords and comments to `.htaccess` and `README.md` to make the project more discoverable.
- **Improved Documentation**: Restructured the `README.md` with a new "Why This Matters for SEO" section and a clearer optimization guide.
- **Versioning**: The project is now at `v1.0.3`.

See the [**CHANGELOG.md**](CHANGELOG.md) for full details on this and previous versions.

---

## 📚 References

- MDN HTTP Headers: https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers
- OWASP Hardening Guides: https://cheatsheetseries.owasp.org/
- Sucuri WordPress Security: https://sucuri.net/guides/wordpress-security/
- WPBeginner Bot Blocking: https://www.wpbeginner.com/wp-tutorials/how-to-block-bad-bots-in-wordpress-using-htaccess/
