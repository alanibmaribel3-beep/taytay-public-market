TAYTAY PUBLIC MARKET WEBSITE — SECURED FRONT-END PROTOTYPE

How to run:
1. Open this folder in Visual Studio Code.
2. Use Live Server / localhost. Do not rely on file:// for passkeys/biometrics.
3. Open index.html.

What was changed:
- All role-sensitive routes now use access control.
- Customer: browse/view products, reserve, edit reservation, delete reservation, profile/settings.
- Vendor: add/edit/delete only the vendor's own products and view relevant reservations.
- Admin: protected Admin dashboard, website name/tagline, logo, hero background, and Admin profile image customization.
- Account registration and login now use stored password hashes instead of accepting any password.
- Admin creates their own Security Code during Admin registration.
- Admin login requires the registered email, password, and that Admin Security Code.
- Biometrics/passkey enrollment is optional and works best on localhost/HTTPS.
- Unauthorized role access is denied.
- SEO metadata was added so the site is indexable after deployment.
- Product cards retain product-specific images matching their listed item/category.

IMPORTANT SECURITY NOTE:
This project is still a browser-only academic prototype. localStorage/sessionStorage are not a secure production database. WebAuthn/passkeys should be verified by a trusted backend server in production, with server-generated challenges, secure cookies/sessions, HTTPS, rate limiting, CSRF protection, database authorization, audit logs, and password hashing such as Argon2/bcrypt on the server.

Admin registration demo code:
TPM-ADMIN-2026
Change/remove this client-side demo code before any real deployment. In production, Admin creation must be server-side/invite-only.

Making the website searchable in browsers/search engines:
1. Deploy it to a public HTTPS host/domain (GitHub Pages, Netlify, Vercel, or your own server).
2. Use a real domain if available.
3. Add the deployed URL to Google Search Console and request indexing.
4. Create robots.txt and sitemap.xml using the final public domain.
5. Keep the SEO title/description accurate and add real market contact/business information.

Biometrics/passkeys:
Platform authenticators generally require HTTPS (localhost is allowed for development), a supported browser, and a device with Windows Hello, Touch ID, Face ID, fingerprint, PIN, or another passkey-capable authenticator.

V3 updates:
- Material Symbols (Flutter/Material-style) icons replace dashboard emoji icons.
- Customer now has a dedicated dashboard.
- Role-aware Settings are available to Customer, Vendor, and Admin.
- Vendor Add/Edit Product uses device image upload or camera capture with preview (max 5 MB); Image URL entry removed.
- Admin Quick Management buttons now open working management views.
- Existing visual theme/layout is preserved.
- For camera/passkeys, run with VS Code Live Server/localhost or HTTPS rather than file:// where possible.
- GitHub publishing requires connecting/authorizing the GitHub connector in ChatGPT first.
