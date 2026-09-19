# sethkolodny.com

Your website. Plain HTML and CSS — no frameworks, no database, nothing to
update or patch. The whole site is about 40 KB, so it loads almost instantly
on a phone.

---

## What each file is

| File | What it is |
|---|---|
| `index.html` | The home page |
| `about.html` | About page (personal + professional) |
| `markets.html` | Markets section — the list of your notes |
| `notes/example-note.html` | Template for a single market note |
| `contact.html` | Contact page |
| `404.html` | Shown when someone hits a bad address |
| `css/style.css` | All the styling for every page |
| `assets/images/` | Where your photos go |
| `CNAME` | Tells GitHub your domain is sethkolodny.com |
| `robots.txt`, `sitemap.xml` | Help search engines index the site |

---

## Editing the text

Open any `.html` file in **TextEdit** (right-click the file → Open With →
TextEdit) or any plain-text editor. You will see text mixed with tags in
angle brackets:

```html
<p>This is a paragraph of text.</p>
```

**Change the words, leave the tags alone.** That is the whole rule.

Everywhere I left something for you to fill in, there is a marker:

```html
<!-- EDIT ME: what to write here -->
```

Anything between `<!--` and `-->` is a note to yourself. Visitors never see
it. Delete those lines once you have written the real text.

### The tags you will actually use

| Tag | Does |
|---|---|
| `<p>text</p>` | A paragraph |
| `<h2>text</h2>` | A section heading |
| `<strong>text</strong>` | **Bold** |
| `<em>text</em>` | *Italic* |
| `<a href="https://example.com">text</a>` | A link |
| `<ul><li>item</li></ul>` | A bulleted list |

---

## Adding your photo

1. Put the image file in `assets/images/`. Name it `portrait.jpg`.
2. In `index.html`, find the line with `portrait-placeholder.svg`
   and change it to `portrait.jpg`.

**Resize it first.** A photo straight off a phone can be 5 MB, which is
slower than the rest of the site combined. Open it in Preview → Tools →
Adjust Size → set the width to **880 pixels** → File → Export → JPEG,
quality around 70%. That gets you well under 200 KB with no visible loss.

---

## Adding a new market note

1. Duplicate `notes/example-note.html` (right-click → Duplicate).
2. Rename it to something short with dashes instead of spaces, e.g.
   `october-outlook.html`.
3. Open it and write your note. Change the `<title>` near the top too —
   that is what shows in the browser tab and in Google results.
4. Open `markets.html` and add an entry to the list, copying the
   shape of the one that is already there:

```html
<li>
  <span class="post-date">1 October 2026</span>
  <h3><a href="notes/october-outlook.html">Your title here</a></h3>
  <p>A one-line summary that shows in the list.</p>
</li>
```

Newest note goes at the top.

---

## Changing the colors

Open `css/style.css`. The first block is the entire palette:

```css
:root {
  --ink:    #1a1d21;   /* main text */
  --paper:  #fbfaf8;   /* page background */
  --accent: #1f4d6b;   /* links and buttons */
  ...
}
```

Change a value, save, reload. Every page updates at once. The block below
it does the same thing for people whose phone or laptop is set to dark
mode — change both if you want them to match.

---

## Previewing changes before they go live

Double-click `index.html` in this folder. It opens in your browser from your own Mac.
Nobody else can see it. Make an edit, save, and hit reload to see it.

---

## Publishing a change

Once the site is on GitHub (see below), editing is:

1. Go to your repository on github.com
2. Click the file you want to change
3. Click the **pencil icon**
4. Edit the text
5. Scroll down, click **Commit changes**

Your live site updates in about a minute. No software to install.
