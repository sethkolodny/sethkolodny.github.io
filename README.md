# sethkolodny.com

A two-page site: an About page (which is also the landing page) and a
Contact page. Plain HTML and CSS — no frameworks, no database, nothing to
update or patch.

---

## What each file is

| File | What it is |
|---|---|
| `index.html` | The About page — what visitors see at sethkolodny.com |
| `contact.html` | Contact page (email and LinkedIn) |
| `404.html` | Shown when someone hits a bad address |
| `css/style.css` | All the styling for both pages |
| `assets/images/portrait.webp` | Your photo, modern format |
| `assets/images/portrait.jpg` | Same photo, fallback for older browsers |
| `CNAME` | Tells GitHub your domain is sethkolodny.com |
| `robots.txt`, `sitemap.xml` | Help search engines index the site |

---

## Editing the text

Open either `.html` file in **TextEdit** (right-click → Open With →
TextEdit) or any plain-text editor. You will see text mixed with tags in
angle brackets:

```html
<p>This is a paragraph of text.</p>
```

**Change the words, leave the tags alone.** That is the whole rule.

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

## Replacing your photo

The site uses the same photo in two formats. Browsers that support WebP get
the smaller file; older ones fall back to the JPEG.

If you swap the photo, replace **both** files, keeping the same names —
otherwise some visitors see the old picture and some see the new one.
Easiest route: give me the new image and I will produce both.

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

Change a value, save, reload. Both pages update at once. The block below it
does the same for visitors whose device is set to dark mode — change both
if you want them to match.

---

## Previewing changes before they go live

Double-click `index.html` in this folder. It opens in your browser from your
own Mac. Nobody else can see it. Make an edit, save, hit reload.

---

## Publishing a change

1. Go to your repository on github.com
2. Click the file you want to change
3. Click the **pencil icon**
4. Edit the text
5. Scroll down, click **Commit changes**

Your live site updates in about a minute.

**Note:** uploading files only adds and replaces. To *remove* a page from
the live site you must delete it on GitHub — open the file there, click the
trash icon, then commit.
