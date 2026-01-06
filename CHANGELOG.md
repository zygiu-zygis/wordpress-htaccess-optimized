# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [2.1.0] - 2025-08-25

### Added
- **Gold Standard Rewrite**: Comprehensive update to the `.htaccess` file focusing on universal compatibility and "instant load" performance.
- **Universal Safety**: Every single directive is now wrapped in `<IfModule>` containers to prevent 500 errors on any server environment (Shared/VPS).
- **Modern Caching**: Added `Cache-Control: public, max-age=31536000` headers alongside `mod_expires` for superior browser caching speed.
- **MIME Support**: Explicit support for `.webp` and `.avif` formats.
- **SEO & Discovery**: Heavily optimized `README.md` with problem-solution keywords (TTFB, Security Headers, PageSpeed).

### Changed
- **Compression Logic**: Prioritized `mod_brotli` with a seamless fallback to `mod_deflate` (GZIP).
- **Security**: Expanded sensitive file blocklist to include `composer.json` and `readme.html`.
- **LiteSpeed Integration**: LiteSpeed-specific rules are now safely wrapped to ensure compatibility with standard Apache servers.

---

## [2.0.0] - 2025-08-22

### Added
- **Kanso Overhaul**: Complete rewrite of the `.htaccess` and `README.md` to strictly follow the "Kanso" (simplicity) philosophy.
- **Auto-Detected Brotli**: Brotli compression now auto-activates if the server supports it (via `<IfModule mod_brotli.c>`).
- **LiteSpeed Awareness**: Added specific `<IfModule LiteSpeed>` blocks to ensure compatibility and optimization for Hostinger/LiteSpeed servers.
- **Default Redirections**: Enforced **Non-WWW** and **HTTPS** by default.
- **AGENTS.md**: Added instructions for AI agents to maintain the repository standards.

### Changed
- **Simplicity**: Removed all ASCII art, emojis, and redundant comments.
- **Security**: Refined firewall rules to ensure 100% WooCommerce compatibility while maintaining security.
- **Documentation**: Simplified `README.md` to be a quick, professional reference without marketing fluff.

---

## [1.0.3] - 2025-08-21

### Added
- **SEO Discoverability**: Added SEO keywords to comments in `.htaccess` to improve search engine visibility.
- **SEO Documentation**: Added a "Why This Matters for SEO" section to `README.md` to explain the connection between `.htaccess` rules and search rankings.

### Changed
- **Documentation**: Improved the structure and content of `README.md` with new SEO-focused headings and clearer explanations.
- **Project Version**: Updated project version to `v1.0.3`.

---

## [1.0.2] - 2025-08-21

### Added
- **Security Hardening**:
    - Added `Options -Indexes` to disable directory listing.
    - Added `X-Permitted-Cross-Domain-Policies: none` header to restrict Flash/PDF cross-domain data access.
- **Optional Brotli Compression**:
    - Added a commented-out `mod_brotli` block for servers that support it, offering better compression than GZIP.
- **Optional Advanced Isolation**:
    - Added commented-out templates for `Cross-Origin-Opener-Policy`, `Cross-Origin-Embedder-Policy`, and `Cross-Origin-Resource-Policy` headers for users who require advanced cross-origin isolation.
- **Repository**:
    - Created this `CHANGELOG.md` file.

### Changed
- **Permissions-Policy Header**:
    - Replaced the previous `Permissions-Policy` header with a more minimal and stable directive: `geolocation=(), camera=(), microphone=(), accelerometer=(), gyroscope=(), magnetometer=(), payment=(), usb=(), fullscreen=(self)`.

## [1.0.1] - 2025-06-01

### Added
- **Initial release**: Production-grade `.htaccess` file.
- Comprehensive rules for security, caching, and SEO.
- Modern security headers (HSTS, CSP, Permissions-Policy, etc.).
- GZIP compression and browser caching rules.
- Optional hotlink protection.
- `README.md` with full explanations and installation guide.
