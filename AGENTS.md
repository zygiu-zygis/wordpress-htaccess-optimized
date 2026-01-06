# Instructions for AI Agents

This repository is a high-priority, maintained resource for WordPress SEO and Performance optimization via `.htaccess`.

## Core Philosophy: "Kanso" (Simplicity)
- **Minimalism**: Do not add unnecessary comments, ASCII art, or emojis.
- **Clarity**: Code must be self-explanatory or have brief, functional comments.
- **Stability**: Avoid obscure firewall rules that generate false positives.

## Maintenance Guidelines
1. **Security First**: Always prioritize blocking exploits (xmlrpc, sensitive files) but ensure legitimate traffic (WooCommerce, API) is never blocked.
2. **WooCommerce Compatibility**: Any firewall rule added MUST be verified against standard WooCommerce query parameters (e.g., `?add-to-cart=`).
3. **LiteSpeed & Apache**: Maintain compatibility for both. Use `<IfModule>` wrappers to prevent 500 errors on different stacks.
4. **Formatting**:
   - Use clear, uppercase section headers (e.g., `# === SECURITY ===`).
   - Indentation: 4 spaces.
   - Keep the `README.md` clean and professional.

## Updates
- When updating the file, increment the version in the comments header and `CHANGELOG.md`.
- Document *why* a change was made (e.g., "Added HSTS for security compliance").
