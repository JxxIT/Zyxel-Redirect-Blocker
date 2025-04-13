
# Zyxel Redirect Blocker

Some Zyxel models redirect to HTTPS, where the connection is refused. This script forces HTTP.

Installation:
1. Install the Tampermonkey extension for your browser (Chrome, Firefox, Edge, etc.).
2. Install the script from either:
   * [GitHub](https://github.com/JxxIT/Zyxel-Redirect-Blocker/raw/refs/heads/main/zyxel.user.js)
   * [Greasy Fork](https://greasyfork.org/en/scripts/532703-zyxel-redirect-blocker/code)
3. Click the Install button.
4. Try to log in to your router; it should work.

## How it works

I looked at the frontend code of my Zyxel DX5401-B1 and saw that when some conditions were met, it redirected to HTTPS. Those conditions could be modified by modifying the 'flags.' This script intercepts the flags and sends our modified flags to the client, which reads the flags and doesn't redirect us to HTTPS.
