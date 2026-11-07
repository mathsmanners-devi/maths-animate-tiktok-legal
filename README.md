# TikTok developer app legal pages

This directory is a standalone, static GitHub Pages site for the
**Maths-Animate Devi** TikTok developer app. It contains only public website
content; do not copy credentials, tokens, account configuration, videos, or
manager source code into the Pages repository.

## Publish with GitHub Pages

1. Create a GitHub account and verify its email address.
2. Create a **public** repository named `maths-animate-tiktok-legal`.
3. Upload the contents of this directory to the repository root (so `index.html`
   is at the root, not inside a `legal-pages` subdirectory).
4. In the repository, open **Settings → Pages**. Under **Build and deployment**,
   select **Deploy from a branch**, choose the `main` branch and `/ (root)`,
   then save.
5. Wait for GitHub Pages to finish deploying. The site URL will be:
   `https://YOUR-GITHUB-USERNAME.github.io/maths-animate-tiktok-legal/`
6. Confirm the home, privacy, and terms pages load in a private browser window.
   Replace `YOUR-GITHUB-USERNAME` with the exact account name. Use the resulting
   home page as the app's website URL, and the `privacy.html` and `terms.html`
   addresses as their respective URLs.
7. TikTok requires URL-property verification for the website, privacy-policy,
   and terms URLs for apps created after September 9, 2024. In the app's
   **URL properties** settings, follow TikTok's current verification flow. If
   TikTok offers URL-prefix verification, it may provide a verification file;
   publish that exact file at the path TikTok specifies and verify the live URL.
   Do not create or alter the verification file yourself.

The site URL cannot be finalized until the GitHub username is known and the
deployment has succeeded. Enter only the live URLs in TikTok's form. GitHub
Pages availability and TikTok's acceptance are controlled by those platforms;
publishing these pages does not guarantee app approval.

## TikTok OAuth callback

The CLI OAuth flow needs this exact registered HTTPS redirect URI:

`https://mathsmanners-devi.github.io/maths-animate-tiktok-legal/callback.html`

Upload `callback.html` from this directory to the repository root and wait until
that exact URL loads before registering it under the app's **Login Kit**
redirect URI settings. Then save the same URI in the manager's private
`config/developer_app_config.local.json` as `app.redirect_uri`. The CLI opens
the TikTok authorization page and reads the returned one-time authorization
code and state from the browser URL, validates the state, and exchanges the
code locally; the callback page itself does not display or store them.

The callback URL is a separate setting from the website, privacy-policy, and
terms URLs. Do not use the home page as the redirect URI. Never paste an
authorization code, access token, refresh token, or app secret into this public
repository or send one in chat.

For sandbox testing, create a Sandbox in TikTok for Developers, configure its
Login Kit, Content Posting API and only the scopes being tested, add the TikTok
account as a Sandbox target user, and apply the changes. Authorize using that
target account. Sandbox setup and approval are controlled by TikTok; this site
does not enable or grant sandbox access by itself.

The manager's publishing code is not yet a compliant end-to-end Content Posting
demo: it does not query and present current creator settings and consent in a
user-facing flow. Do not use a Sandbox test or app-review demo to claim these
posting requirements are met. Login Kit/account identification can be tested
separately after the callback and Sandbox are configured.

## Keep the pages accurate

The policies describe the current local manager: preparation and caption
generation are local, OAuth credentials and operational state are stored on
the owner's computer, and the app communicates with TikTok when the owner
authorizes or explicitly starts a TikTok API operation. Review and update the
policies if the software starts using new data, providers, or hosting.
