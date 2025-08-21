# WordPress .htaccess for Maximum Speed, Security & SEO

A production-grade `.htaccess` for WordPress — optimized for **performance**, **security**, **Core Web Vitals**, and **SEO**. Version `v1.0.1` delivers modern caching, GZIP compression, security headers, proactive bot blocking, and optional hotlink protection.

---

## 🚀 Key Features & Benefits

- 🔐 **Security Headers**: HSTS, CSP (upgrade-insecure-requests), Permissions-Policy, Referrer-Policy, X-Frame-Options, X-Content-Type-Options, plus legacy X-XSS-Protection for older browsers.
- 🚫 **Bot & Exploit Mitigation**: Blocks common reconnaissance and direct access to sensitive endpoints; optional XML-RPC block (verify plugin dependencies before enabling).
- ⚡ **Intelligent Caching**: `mod_expires` + granular `Cache-Control` with `immutable` for versioned static assets. Conservatively revalidates HTML/XML/JSON; example `no-store` pattern for API JSON files.
- 🗜️ **Compression**: GZIP for text-based assets (`text/*`, `application/*`, SVG). Skips already-compressed binaries to save CPU.
- 🌐 **CORS-Ready**: Safe cross-origin access for fonts and CDN-served assets.
- 🖼️ **Hotlink Protection (Optional)**: Example rules with clear instructions.

---

## ✅ Why This .htaccess?

- **Drop-in**: Sensible defaults that avoid common pitfalls (e.g., no trailing inline comments that break Apache).
- **SEO & CWV**: Faster repeat visits via long-lived caching and `immutable`.
- **CDN-Friendly**: Disables `ETag` to avoid inode mismatches; relies on cache-busting filenames and explicit `Cache-Control`.

---

## 💻 Compatibility & Requirements

- **Servers**: Apache 2.4+, LiteSpeed, Plesk (Apache+NGINX), Cloudways stacks.
- **Modules**: `mod_rewrite`, `mod_headers`, `mod_deflate`, `mod_alias`, `mod_expires`.

> When using Cloudflare or similar CDNs, prefer managing headers centrally there; this `.htaccess` acts as a robust fallback.

---

## 🛠 Installation

1. **Backup** your current `.htaccess`.
2. **Replace** with the file from this repo.
3. **Hotlink Protection**: If enabling, replace `yourdomain\.com` with your real domain.
4. **Wordfence**: Run *Optimize Firewall* to prepend WAF rules.
5. **Cloudways**: Do **not** enable the HTTP→HTTPS block here (handled by the platform).
6. **Validate** via [securityheaders.com](https://securityheaders.com) and [PageSpeed Insights](https://pagespeed.web.dev/).

---

## 🔄 Contributing & Versioning

- Use **Conventional Commits** (e.g., `feat:`, `fix:`, `docs:`).
- Test on **staging** before production.
- Tag releases (e.g., `v1.0.2`) with clear change logs.

---

## 📌 What’s New in `v1.0.1`

- Removed deprecated/duplicate MIME types and **inline trailing comments** that can break Apache parsing.
- Added explicit `Cache-Control` with **`immutable`** for versioned static assets.
- Clarified JSON handling: revalidation by default; **example `no-store`** for API `.json` files.
- Safer security section: **do not block** `.well-known/security.txt` by default; keep `xmlrpc.php` block with a caution note.
- Improved comments for GitHub readability and maintainability.

---

## 📚 References

- MDN HTTP Headers: https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers  
- OWASP Hardening Guides: https://cheatsheetseries.owasp.org/  
- Sucuri WordPress Security: https://sucuri.net/guides/wordpress-security/  
- WPBeginner Bot Blocking: https://www.wpbeginner.com/wp-tutorials/how-to-block-bad-bots-in-wordpress-using-htaccess/
