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

The OAuth redirect URI is a separate Login Kit setting. This site does not
implement an OAuth callback endpoint and its home page must not be used as the
redirect URI unless a working callback is deliberately added and registered.

## Keep the pages accurate

The policies describe the current local manager: preparation and caption
generation are local, OAuth credentials and operational state are stored on
the owner's computer, and the app communicates with TikTok when the owner
authorizes or explicitly starts a TikTok API operation. Review and update the
policies if the software starts using new data, providers, or hosting.
