# woocommerce-shopify-bundle-plugin
woocommerce-shopify-bundle-plugin
# Quantity Break Widgets — Shopify-style (Free)

A WordPress/WooCommerce plugin that provides 5 Shopify-style quantity break widgets:
WideBundle, Zoorix, Kaching, Vitals, and Wizio.

## Features
- Dynamic pricing (unit price applied to cart)
- Visual per-product tier editor (add/remove/reorder rows)
- Global defaults in Settings → Qty Break Widgets
- Gutenberg block + Elementor widget
- Lightweight, no external libraries (jQuery for admin)
- Internationalization-ready (text domain: qty-break-widgets)

## Installation
1. Create a folder `qty-break-widgets` in `wp-content/plugins/`.
2. Place the files:
   - `qty-break-widgets-plugin.php`
   - `README.md`
   - `assets/qtyw-admin.js`
   - `assets/qtyw-admin.css`
   - `assets/qtyw-style.css`
   - `assets/qtyw-script.js`
3. Zip the `qty-break-widgets` folder or upload via Plugins → Add New → Upload Plugin.
4. Activate the plugin.
5. Edit a product and use the "Quantity Break Tiers" meta box to add tier rows and save the product.
6. Add the shortcode `[qty_break_widgets]` on the product page (or insert the Gutenberg block).

## Example tier JSON (for defaults)
[{"min":1,"price":19.99,"note":""},{"min":2,"price":17.99,"note":"10% off"},{"min":3,"price":15.99,"note":"20% off"}]

## Notes & Caveats
- This is a starter / demo-grade plugin meant for testing and prototyping. Please test thoroughly on a staging site before using in production.
- Compatibility considerations:
  - Variable products: the current demo targets simple products. For variable support, a per-variation tier setup or hooking into variation change events is recommended.
  - Other pricing plugins: if a third-party plugin heavily overrides the price DOM or calculation, you may need to adjust selectors or the cart logic.
- Security & Hardening:
  - Nonces and capability checks are used when saving product meta.
  - Tier JSON is validated/sanitized on save.

## License
MIT-style (feel free to adapt). Author: ChatGPT/Claude
