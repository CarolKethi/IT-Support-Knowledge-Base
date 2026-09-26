### Ticket Number: 005
### Title: Chrome Redirecting to jxsrchrdr.com on Startup
### Date: 2026-09-26
### Category: Software / Browser

**Reported Issue:**
When opening Chrome, it automatically redirects to jxsrchrdr.com/?gd=RD1005865&searchsource=69&n=19r9qo6xerlmm29 with a blank white page instead of normal homepage.

**Root Cause:**
Browser hijacker changed Chrome settings. Default search engine and On Startup page were modified to jxsrchrdr.com domain by a malicious extension. Common cause is third-party extension or software installed from unverified source.

**Troubleshooting Steps:**
1. Observed URL - confirmed redirect to jxsrchrdr.com on Chrome launch
2. Checked chrome://extensions - looked for unknown "Search" extensions
3. Checked chrome://settings > Search engine and On startup - found jxsrchrdr set as homepage/search
4. Checked desktop shortcut properties - verified Target field
5. Cleared cache/cookies

**Solution:**
Fixed by:
1. Removing suspicious extension from chrome://extensions
2. In Settings > Search engine - set back to Google
3. In Settings > On startup - removed jxsrchrdr link, set to "Open New Tab page"
4. In Settings > Manage search engines - deleted jxsrchrdr.com entry
5. Cleared browsing data (All time) and restarted Chrome

**Time to Resolve:** ~5 minutes
**Prevention:** Only install extensions from Chrome Web Store. Educate users not to click Allow on search permission popups.
