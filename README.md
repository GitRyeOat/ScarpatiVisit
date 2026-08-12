# An Evening at Blue Dot — For the Scarpati Family

A one-page website for the August 23 fundraiser at Blue Dot Barn, Nicasio, CA.

## What's in here

```
index.html            the whole website (HTML + CSS + JS in one file)
images/               the photos, already resized for the web
images/venmo-qr.png   QR code pointing at venmo.com/u/oopaddy
scarpati-flyer.pdf    the event poster, letter size — what "Share This Event" downloads
README.md             this file
```

No build tools, no frameworks, no accounts needed. Just upload it.

---

## IMPORTANT — one setup step before the contact form works

The contact form sends to **shamrockbluedot@gmail.com** through a free service
called FormSubmit. It has to be switched on once, and it can only be switched on
after the site is live. Here's the sequence:

1. Publish the site (steps below).
2. Open your live site, fill in the contact form, and hit **Send Message**.
3. FormSubmit will email **shamrockbluedot@gmail.com** a confirmation link.
   Open that email and click the link.
4. That's it — from then on every submission arrives in that inbox
   automatically. You never have to do it again.

Until step 3 is done, submissions won't be delivered. Do a test submission
yourself before you send the link to anyone.

**Why this service?** GitHub Pages only serves files — it can't send email on
its own. FormSubmit is the standard free workaround for static sites. If you'd
rather not use a third party, you can delete the form and leave the phone number
and email address that are already on the page.

---

## Publishing on GitHub Pages

1. Create a new repository on GitHub (public).
2. Upload `index.html`, the `images` folder, and this README — either by
   dragging them into the "Add file → Upload files" screen, or with git:
   ```
   git init
   git add .
   git commit -m "Scarpati fundraiser site"
   git branch -M main
   git remote add origin https://github.com/YOURNAME/YOURREPO.git
   git push -u origin main
   ```
   `index.html` must sit at the top level of the repo, with `images/` next to it.
3. In the repo, go to **Settings → Pages**.
4. Under "Build and deployment", set **Source** to `Deploy from a branch`,
   **Branch** to `main`, folder `/ (root)`. Save.
5. Wait about a minute. Your site is live at
   `https://YOURNAME.github.io/YOURREPO/`

To use a custom domain, add it under Settings → Pages → Custom domain, then
point a CNAME record at `YOURNAME.github.io` with your domain registrar.

---

## How the buttons work

**Get Tickets** (header, hero, event section, blue band) opens a pop-up with the
Venmo QR code, a link to `venmo.com/u/oopaddy`, and this message: *"Once payment
has been made, please do text or call 415 328 7388 to connect with us and cover
all the details!"* The QR scans straight into the Venmo app; tapping it opens the
same profile in a browser.

**Support Oscar** (header and blue band) opens the same pop-up, worded for an
open-amount contribution rather than a $100 minimum-donation seat. Same Venmo account, same
phone message. It's hidden in the header on narrow phones to keep the bar tidy —
the one in the blue band always shows.

**Share This Event** downloads `scarpati-flyer.pdf` — the poster, one letter-size
page, ready to print or text. To swap the poster, replace that file, keeping the
same filename.

**Contact** and **Book a Session** scroll down to the contact form.

## Changing things later

| To change | Search `index.html` for |
| --- | --- |
| Venmo account | `venmo.com/u/oopaddy` (appears twice) — and regenerate `images/venmo-qr.png` |
| Phone number | `4153287388` |
| Email address | `shamrockbluedot@gmail.com` (appears three times) |
| Pop-up wording | `modal-note` |
| Ticket price / minimum donation | `$100` |
| Pop-up wording for either mode | `var MODES` in the script at the bottom |
| Photo credit | `class="credit"` |

All the page copy is plain HTML in the order it appears on the page. Edit the
words between the tags, save, re-upload.

To swap the Venmo QR for a different account, you can regenerate it at any free
QR generator using the new profile URL, and replace `images/venmo-qr.png`.

## Photo credits

The polo field photo is credited to Alice Gipps, Equine Photographer.
