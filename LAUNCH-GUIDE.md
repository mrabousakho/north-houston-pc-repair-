# Launch Guide — northhoustonpcrepair.com

Your files live in: **C:\Users\buakartrading\Desktop\repairshop**
Domain: **northhoustonpcrepair.com** ✅ (registered)
Public email: **info@northhoustonpcrepair.com** · Phone: **(346) 917-7951**

---

## THE BIG PICTURE — how a repair request reaches you

GitHub Pages just *shows* your website; it can't send email on its own. So the form uses a free relay:

```
Customer fills the form
      ↓
FormSubmit.co  (free, no signup — already built into your site)
      ↓  emails
info@northhoustonpcrepair.com
      ↓  forwards to
your Gmail  →  ping on your phone 📱
```

You'll get every request as a tidy email with the person's name, contact, problem, and details. You also get calls/texts directly from the phone + WhatsApp buttons.

Two one-time setups make this work: **(A) get info@ forwarding to your Gmail**, and **(B) activate FormSubmit**. Both below.

---

## STEP A — Make info@northhoustonpcrepair.com reach your Gmail (10 min)

You own the domain, so create the address as a **free forward** to your Gmail:

1. Log in to the registrar where you bought the domain.
2. Find **Email Forwarding** (Namecheap: Domain List → Manage → "Redirect Email / Email Forwarding". Cloudflare: **Email → Email Routing**. GoDaddy: "Email" / forwarding).
3. Create: **info@northhoustonpcrepair.com  →  mrabousakho@gmail.com**
4. Save. Send a test email to info@… and confirm it lands in your Gmail.

> Want to *send* replies as info@… too (looks pro)? In Gmail: Settings → Accounts → "Send mail as" → add info@northhoustonpcrepair.com. Optional, do it later.

---

## STEP B — Put the site on GitHub Pages (20 min)

1. Create a free account at **github.com**.
2. Click **+ → New repository**. Name it `northhoustonpcrepair` (or anything). Set **Public**. Create.
3. On the repo page: **Add file → Upload files**. Drag in EVERYTHING from your `repairshop` folder — `index.html`, `CNAME`, and the two `.md` guides. Commit.
   - The **CNAME** file (already in your folder) tells GitHub your custom domain. Keep it.
4. Go to **Settings → Pages**:
   - Source: **Deploy from a branch** → Branch: **main** → **/(root)** → Save.
   - Under "Custom domain" type **northhoustonpcrepair.com** → Save.
   - Tick **Enforce HTTPS** once it becomes available (may take an hour).
5. GitHub gives you a temporary address like `yourname.github.io/northhoustonpcrepair` — the site is already live there.

---

## STEP C — Point northhoustonpcrepair.com at GitHub (15 min + wait)

In your **registrar's DNS settings**, add these records (this is proper hosting, better than URL forwarding — it keeps your real domain in the address bar with HTTPS):

**Apex domain (northhoustonpcrepair.com) — four A records:**
| Type | Name | Value |
|------|------|-------|
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |

**www subdomain — one CNAME record:**
| Type | Name | Value |
|------|------|-------|
| CNAME | www | yourname.github.io |

(Replace `yourname` with your GitHub username.)

Save. DNS can take 15 minutes to a few hours to spread. Then **northhoustonpcrepair.com** shows your site. Back in GitHub → Settings → Pages it'll confirm the domain is verified and issue HTTPS automatically.

> Prefer plain URL forwarding instead? Your registrar can "forward northhoustonpcrepair.com → yourname.github.io". It works but is uglier (visitors may see the github URL) and HTTPS is trickier. The DNS method above is the right way — I recommend it.

---

## STEP D — Activate the form so emails actually send (2 min) ⭐

FormSubmit needs a one-time activation the first time it emails a new address:

1. Once the site is live, open it and **submit the contact form once yourself** (use real info).
2. FormSubmit sends a **confirmation email to info@northhoustonpcrepair.com** (which now forwards to your Gmail). Open it and click **Activate**.
3. Done — from now on every submission emails you automatically. Submit one more test to confirm it lands.

> Spam control: after activation you can grab your private FormSubmit "random string" endpoint and put it in `CONFIG.formSubmitTo` instead of the email, so your address isn't visible in the page source. Optional — ask me and I'll switch it.

---

## STEP E — Go get customers (this week)

- [ ] Create a **free Google Business Profile** for "North Houston PC Repair" — your #1 source of local calls.
- [ ] Post your site in **North Houston Facebook groups + Nextdoor** ("Free step-by-step computer fixes — local tech if you get stuck").
- [ ] Put **northhoustonpcrepair.com** in every bio, WhatsApp status, email signature, and on a cheap car magnet / flyer.
- [ ] Ask your first 3 customers for a Google review; swap the sample reviews on the site for real ones.
- [ ] Open `social-content-starter.md` — 20 posts ready. Post every other day.

---

## Coming next (when you're ready)
- **Video Library** — browsable repair & DIY videos by topic and device (your YouTube + curated), to make people frequent the site.
- **Automated social posts** — say "set up my recurring social posts" and I'll schedule a fresh tip every other day.
- Drop in your **real photo/logo**, add a booking calendar, or expand the Fix-It Tool.

## Editing your details later
Everything is in the `CONFIG` block near the bottom of `index.html`. Change a line, re-upload the file to GitHub, done.
