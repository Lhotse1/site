# Your website: start here

This folder is your whole website. There are no databases and no monthly fees, just files.

```
site/
├── index.html            ← Home page
├── portfolio.html        ← All your work, as cards
├── project-example.html  ← Case-study template (copy it once per project)
├── about.html            ← Bio, experience, qualifications, contact
├── css/style.css         ← The look: colours, fonts, spacing
└── assets/
    ├── images/           ← Screenshots go here
    └── files/            ← PDFs, Excel files and your CV go here
```

**The one idea to understand:**
- The `.html` files hold the **content** (words, links, images).
- `style.css` holds the **look**.

To change the text, edit the HTML. To change a colour everywhere, edit the top of the CSS.

---

## Stage 1: Set up (about 20 minutes)

1. **Install VS Code** (free) from code.visualstudio.com. It's a text editor built for code.
2. In VS Code, go to **Extensions** (the squares icon on the left), search for **Live Server** and install it.
3. **File → Open Folder** and choose this `site` folder.
4. Right-click `index.html` and choose **Open with Live Server**. Your site opens in your browser.
   Every time you save a file, the browser page refreshes on its own.

## Stage 2: Make it yours (1–2 evenings)

Work through the files in this order. In each one, look for placeholder text.

1. **Contact links.** Search every file (Ctrl/Cmd + Shift + F) for `you@example.com` and
   `YOUR-PROFILE`, then replace them with your real email and LinkedIn address.
2. **about.html.** Write your intro, and fill in the years for each role.
3. **index.html.** Tweak the headline if you want, then choose your three best projects.
4. **Add your CV** as `assets/files/cv.pdf`.

**HTML basics you need:**
- `<h1>…</h1>` is a big heading, `<h2>` is smaller, and `<p>…</p>` is a paragraph.
- `<a href="page.html">text</a>` is a link.
- `<img src="assets/images/pic.png" alt="description">` is an image.
- Text between `<!--` and `-->` is a note to you. Visitors never see it.
- Change only the words **between** the tags. If something breaks, press Ctrl/Cmd + Z.

## Stage 3: Add portfolio items (ongoing)

For each piece of work:

1. **Anonymise it first.** Remove client and employer names, and replace real figures with
   illustrative ones or scale them. Get permission if you're unsure. Never publish a real employer's financials.
2. Save a screenshot to `assets/images/`, using a short name with no spaces (e.g. `kpi-dashboard.png`).
   Save any download (PDF or `.xlsx`) to `assets/files/`.
3. In `portfolio.html`, copy one whole `<article class="card">…</article>` block, paste it,
   and edit the title, text, tag and links.
4. Swap `<div class="card-thumb">Screenshot goes here</div>` for
   `<div class="card-thumb"><img src="assets/images/kpi-dashboard.png" alt="KPI dashboard"></div>`.
5. **Optional case study:** duplicate `project-example.html` and rename it (e.g. `project-kpi-dashboard.html`).
   Fill in the Problem, What I did and Result sections, then point the card's link at the new file.

**Tip:** recruiters skim. A clear screenshot plus a single sentence on the result
("cut month-end close from 10 days to 5") beats a long write-up.

## Stage 4: Put it online (about 30 minutes)

We'll use **Netlify**. It's free and handles custom domains and HTTPS for you.

1. Sign up at netlify.com.
2. Go to **Add new site → Deploy manually** and drag the `site` folder onto the page.
3. After a few seconds your site is live at an address like `something.netlify.app`. Test it on your phone.
4. To update the site later, drag the folder on again. (Later on, we can connect it to GitHub so updates publish automatically.)

## Stage 5: Your own domain (about 30 minutes, plus waiting)

1. Check that the name you want is available (e.g. `arryweller.co.uk` or `.com`) and buy it from a registrar
   such as Cloudflare, Namecheap or 123-reg. Expect to pay about £5–15 a year.
2. In Netlify, go to **Domain management → Add a domain** and follow the steps. Netlify tells you
   exactly which DNS records to copy into your registrar's settings.
3. The new domain can take anywhere from a few minutes to 24 hours to start working. Netlify adds the padlock (HTTPS) for free.
4. Put the link on your CV, your LinkedIn profile and your email signature.

## Stage 6: Growing it later

To add a page, for example **Education** or **Hobbies**:

1. Duplicate `about.html` and rename it (e.g. `hobbies.html`).
2. Replace the content inside `<main>…</main>`.
3. Add a link to the new page in the `<nav>` section of **every** page:
   `<a href="hobbies.html">Hobbies</a>`

## Quick restyle

To change the whole site's colours, edit the lines near the top of `css/style.css`:

```css
--accent: #1f6f5c;   /* buttons and links: try #2b4c7e for navy or #8a3b12 for rust */
--paper:  #fbfaf7;   /* page background */
```

## Before you publish: checklist
- [ ] Your real email and LinkedIn links are in (search for "example.com" and "YOUR-PROFILE")
- [ ] The yellow "Template" boxes are deleted
- [ ] Every link and download works, and no card still says "Screenshot goes here"
- [ ] Nothing confidential appears in screenshots or files
- [ ] You've checked the site on your phone
