# GamiFrench — Privacy Policy site

The official privacy policy of the **GamiFrench** learning app, served as a static
page on **GitHub Pages**:

> **Live URL:** <https://mrlearner168.github.io/gamifrench-privacy/>

This URL is what you paste into **Google Play Console → App content → Privacy
policy**, and it is already wired into the app itself (Settings ▸ *Privacy
policy*, plus the Login and Register screen footers) via
`Frontend/GamiFrench/src/components/privacy-policy-link.tsx`.

**Why GitHub Pages works for this:** it is `https://`, publicly accessible
worldwide with no login or geo-blocks, and it serves this page as a standard,
non-editable web page — exactly what Google Play's policy-link requirements
demand. Keep this repo **Public** and never delete it.

---

## Before you publish (2 minutes)

1. Confirm the contact email in `index.html`'s **Contact** section &mdash;
   currently `rogerskie500@gmail.com` (it appears twice: once as text, once in
   the `mailto:` link). If that isn't the mailbox you want users and Play
   reviewers writing to, change it there, and make sure it stays monitored.
2. All URLs assume the GitHub username **Mrlearner168** (case is ignored in the
   URL). If that ever changes, update: this README, the URLs in
   `index.html`, and `src/components/privacy-policy-link.tsx` in the app.

## Publish — web UI, no terminal

1. On github.com: **New repository** → name it `gamifrench-privacy` → **Public**
   → **Create repository**. (Skip the "Add a README" option — we're uploading ours.)
2. On the new repo's page click **uploading an existing file**, drag in
   `index.html`, `.nojekyll` and this `README.md`, then **Commit changes**.
3. **Settings → Pages** → *Build and deployment*: Source **Deploy from a branch**
   → Branch **main**, folder **/(root)** → **Save**.
4. Wait 1–3 minutes, then open <https://mrlearner168.github.io/gamifrench-privacy/>
   in a private/incognito window and on mobile data to confirm it loads with no
   login or country blocks.

## Publish — terminal

This folder is already a git repo with one commit, so after creating the empty
repo on github.com:

```powershell
cd "d:\French Game App\privacy-policy-site"
git remote add origin https://github.com/Mrlearner168/gamifrench-privacy.git
git push -u origin main
```

Then enable Pages as in step 3 above.

## Wire it into Google Play

- Play Console → **App content → Privacy policy** → paste the live URL → Save.
- Quick Data-safety mapping for the form (matches what this policy discloses):
  - **Collected:** Email, Name, User IDs, App interactions/other user-generated
    content (learning progress, quiz results, survey answers), Audio (clips from
    speaking exercises), Diagnostics (IP-based rate limiting, server logs).
  - **Purposes:** App functionality, Analytics (de-identified improvement),
    Account management, Fraud prevention/security.
  - **Shared with third parties:** *No* — our providers (Render, Neon, Vercel,
    Groq) process data only on our behalf as service providers.
  - Encrypt in transit: **Yes** · Deletion mechanism available: **Yes**
    (request via the policy's Contact section or your admin/teacher).
- Heads-up: Google also requires a working **account-deletion** pathway for apps
  with account creation — the Contact section above is that pathway; keep it
  live and answer requests promptly.

## Updating the policy

Edit `index.html`, bump the *Last updated* date in the header, commit — GitHub
Pages redeploys automatically. The public git history doubles as a "Changes"
log (section 13 of the policy promises exactly that).

> **Never push the whole `d:\French Game App` workspace to GitHub.** It contains
> `.env` files, signing keystores and `credentials.json` that must stay private.
> Only the three files in this folder are meant to be public.
