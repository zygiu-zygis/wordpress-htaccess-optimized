# WordPress .htaccess for Maximum Speed, Security & SEO

A production-grade `.htaccess` file for WordPress — meticulously optimized for **performance**, **security**, **Core Web Vitals**, and **SEO**. This version (`v1.0.1`) integrates state-of-the-art caching, GZIP compression, modern HTTP security headers, robust bot blocking, and optional hotlink protection right out of the box.

---

## 🚀 Key Features & Benefits

* 🔐 **Enhanced Security Headers**: Implements a comprehensive suite of modern HTTP security headers (`HSTS`, `Content-Security-Policy`, `Permissions-Policy`, `Referrer-Policy`, `X-Frame-Options`, `X-XSS-Protection`, `X-Content-Type-Options`) to fortify your WordPress site against common web vulnerabilities.

* 🚫 **Advanced Bot & Vulnerability Blocking**: Includes proactive rules to block common nuisance requests, known vulnerability scans (e.g., `xmlrpc.php`, `readme.html`), and suspicious attempts to access sensitive files within your WordPress installation.

* ⚡ **Intelligent Browser Caching**: Leverages `mod_expires` and `Cache-Control` headers to set aggressive, long-term browser caching for static assets (CSS, JS, images, fonts). This significantly improves loading times for repeat visitors and reduces server load.

* 🗜️ **Optimized GZIP Compression**: Configures `mod_deflate` to efficiently compress text-based content, reducing bandwidth usage and accelerating content delivery to user browsers. Includes support for modern image formats like AVIF.

* 🖼️ **Optional Hotlink Protection**: Provides a commented-out section to prevent other websites from directly embedding your images, thereby saving your bandwidth and server resources. *Requires configuration.*

* 🌐 **CDN & Cross-Origin Font Support**: Properly configured Cross-Origin Resource Sharing (CORS) headers (`Access-Control-Allow-Origin`) ensure seamless integration with Content Delivery Networks (CDNs) and correct loading of web fonts from external sources.

* 📈 **Improved Core Web Vitals**: Directly contributes to better scores on Google PageSpeed Insights and a superior overall user experience, which are critical factors for search engine rankings and SEO performance.

---

## ✅ Why Choose This .htaccess?

* **Drop-in Solution**: Offers a ready-to-use, secure, and performant `.htaccess` preset, designed to minimize common misconfigurations and streamline deployment.

* **SEO Advantage**: Directly impacts site speed and user experience, both of which are vital ranking signals for major search engines like Google.

* **Robust Hardening**: Provides a strong foundational layer of defense for your WordPress installation against automated threats, malicious bots, and targeted exploits.

* **Broad Compatibility**: Engineered to work effectively across various Apache environments, including common proxy setups such as Apache + NGINX (e.g., Cloudways) and LiteSpeed Web Servers.

---

## 💻 Compatibility & Requirements

This `.htaccess` configuration has been tested and validated with:

* ✅ **Apache 2.4+**

* ✅ **LiteSpeed** Web Server

* ✅ **Plesk** (Apache + NGINX configurations)

* ✅ **Cloudways** (Apache + NGINX reverse proxy + Varnish caching stacks)

> **Required Apache Modules**: For full functionality, ensure the following Apache modules are enabled on your server: `mod_rewrite`, `mod_headers`, `mod_deflate`, `mod_alias`, `mod_expires`.

---

## 🛠 Installation Guide

1.  **Backup**: **Crucially**, create a full backup of your existing `.htaccess` file *before* making any modifications.

2.  **Replace**: Copy the entire content from this repository's `.htaccess` file and paste it into your WordPress site's root `.htaccess` file (typically located in your public_html directory).

3.  **Hotlink Protection (Optional)**: If you choose to enable the hotlink protection section, remember to **replace `yourdomain\.com`** with your actual domain name (e.g., `yourwebsite\.com`, `myblog\.net`).

4.  **Wordfence Integration**: If your site uses the **Wordfence Security plugin**, navigate to your WordPress Admin Dashboard → *Wordfence → Firewall* → and click on **"Optimize Firewall"**. This step ensures Wordfence automatically prepends its Web Application Firewall (WAF) rules, preventing conflicts.

5.  **Cloudways Specific Note**: For sites hosted on **Cloudways**, **do NOT enable the HTTP to HTTPS redirection block** within this `.htaccess` file. Cloudways automatically manages SSL redirection via its platform's SSL panel, and enabling it here can lead to conflicts or redirect loops.

6.  **Test & Verify**: After implementation, thoroughly test your website to ensure all functionalities are working as expected. Validate your security headers and performance metrics using external tools such as [securityheaders.com](https://securityheaders.com) and [Google PageSpeed Insights](https://pagespeed.web.dev/).

---

## 📌 What's New in `v1.0.1`

This version builds upon extensive research and best practices to offer a highly optimized `.htaccess` file. Key improvements and additions since a hypothetical `v1.0.0` release include:

* **Hotlink Protection Example Clarification**: The example domain in the optional hotlink protection section (Section 8) has been updated from a `.lt` TLD to a more universally recognized `.com` TLD (`yourdomain.com`). This change aims to improve clarity and reduce potential confusion for a global audience.

* **Refined Comments & Links**: All comments have been reviewed for clarity, conciseness, and professionalism, with updated and verified links to authoritative documentation for every directive.

* **Comprehensive Blocking Rules**: Expanded and refined blocking directives to address more common WordPress exploit attempts and scanner requests.

* **AVIF Image Format Support**: Included `AVIF` image format in caching and compression directives for modern image optimization.

* **Granular Cache-Control**: Enhanced `Cache-Control` directives for better resource management, including the `immutable` flag for long-lived static assets.

---

## 📦 Versioning & Credits

**Current version**: `v1.0.1`

**Optimized & Maintained by**: [@zygimantasj](https://github.com/zygimantasj)

**Based on original principles**: Andreas Hecht's Gist (v2.0.9) and insights from his article: [Die perfekte .htaccess für WordPress](https://seoagentur-hamburg.com/blog/die-perfekte-htaccess-fuer-wordpress/)

---

## 📚 Further Reading & Authoritative Resources

* [**Mozilla Developer Network (MDN) - HTTP Headers Reference**](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers): An indispensable resource for understanding HTTP headers and their usage.

* [**Google PageSpeed Insights**](https://pagespeed.web.dev/): A critical tool for analyzing and improving your website's performance on both mobile and desktop.

* [**securityheaders.com**](https://securityheaders.com): A quick and effective online tool to check your site's implemented security headers and overall security posture.

* [**Scott Helme - Referrer-Policy Guide**](https://scotthelme.co.uk/a-new-security-header-referrer-policy/): An in-depth article explaining the Referrer-Policy header and its implications.

* [**OWASP Cheat Sheet Series - .htaccess**](https://cheatsheetseries.owasp.org/cheatsheets/Hardened_php.html): While not exclusively for .htaccess, OWASP provides excellent web security guidelines that often involve server configurations.

* [**Sucuri - Hardening WordPress Security**](https://sucuri.net/guides/wordpress-security/): A comprehensive guide on securing WordPress installations against various threats.

* [**WPBeginner - How to Block Bad Bots in WordPress using .htaccess**](https://www.wpbeginner.com/wp-tutorials/how-to-block-bad-bots-in-wordpress-using-htaccess/): A practical guide on implementing bot blocking rules within .htaccess for WordPress.

---

## ⚠️ Disclaimer

This configuration is provided "as-is" and is intended as a starting point for optimizing your WordPress `.htaccess` file. While it incorporates current best practices and security standards, server configurations and specific WordPress setups can vary. **It is imperative to thoroughly test this `.htaccess` file on a staging or development environment before deploying it to a live production website.** The author is not liable for any issues, data loss, or damages caused by the use or misuse of this configuration.
