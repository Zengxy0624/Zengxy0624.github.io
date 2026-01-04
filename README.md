# Xiangyu Zeng's Personal Homepage

Personal academic homepage based on [Jon Barron's template](https://github.com/jonbarron/jonbarron.github.io).

## 🌐 Website

https://Zengxy0624.github.io

---

## 📁 Project Structure

```
├── index.html          # Main page
├── stylesheet.css      # Global stylesheet
├── images/             # Image assets
│   ├── profile.jpg     # Profile photo (to be added)
│   └── favicon/        # Website favicon
├── data/               # Data files (CV, BibTeX, etc.)
└── README.md           # This documentation
```

---

## ✏️ How to Customize

### 1. Edit Personal Information

Edit the personal info section in `index.html`:

```html
<!-- Change name -->
<p class="name" style="text-align: center;">
  Xiangyu Zeng
</p>

<!-- Change bio -->
<p>
  Welcome to my personal homepage. I am Xiangyu Zeng.
</p>

<!-- Change contact links -->
<p style="text-align:center">
  <a href="mailto:your-email@example.com">Email</a> &nbsp;/&nbsp;
  <a href="https://github.com/Zengxy0624">Github</a>
</p>
```

### 2. Add Profile Photo

Save your photo as `images/profile.jpg` (square image recommended, will display as circle).

### 3. Add Contact Links

Uncomment and modify the following links:

```html
<a href="mailto:your-email@example.com">Email</a>
<a href="data/YourName-CV.pdf">CV</a>
<a href="https://scholar.google.com/citations?user=YOUR_ID">Scholar</a>
<a href="https://github.com/Zengxy0624">Github</a>
```

---

## 📄 How to Add Papers

Find the paper templates in `index.html` and uncomment/modify:

### Option 1: With Hover Animation (Highlighted)

```html
<tr onmouseout="paper1_stop()" onmouseover="paper1_start()" bgcolor="#ffffd0">
  <td style="padding:16px;width:20%;vertical-align:middle">
    <div class="one">
      <div class="two" id='paper1_image'>
        <img src='images/paper1_after.jpg' width=100%>  <!-- Image shown on hover -->
      </div>
      <img src='images/paper1_before.jpg' width=100%>   <!-- Default image -->
    </div>
    <script type="text/javascript">
      function paper1_start() {
        document.getElementById('paper1_image').style.opacity = "1";
      }
      function paper1_stop() {
        document.getElementById('paper1_image').style.opacity = "0";
      }
      paper1_stop()
    </script>
  </td>
  <td style="padding:8px;width:80%;vertical-align:middle">
    <a href="https://your-project-page.com">
      <span class="papertitle">Your Paper Title</span>
    </a>
    <br>
    <strong>Xiangyu Zeng</strong>,
    <a href="https://co-author.com">Co-Author Name</a>
    <br>
    <em>Conference/Journal Name</em>, 2025
    <br>
    <a href="project-folder/">project page</a> /
    <a href="https://arxiv.org/abs/xxxx.xxxxx">arXiv</a> /
    <a href="https://github.com/your-repo">code</a>
    <p></p>
    <p>Brief description of your paper.</p>
  </td>
</tr>
```

**Notes**:
- Each paper needs a unique ID (e.g., `paper1`, `paper2`)
- `bgcolor="#ffffd0"` adds yellow highlight; remove for no highlight
- Prepare two images: `before` (default) and `after` (shown on hover)

### Option 2: Simple Version (No Animation)

```html
<tr>
  <td style="padding:16px;width:20%;vertical-align:middle">
    <img src='images/paper_image.jpg' width="160">
  </td>
  <td style="padding:8px;width:80%;vertical-align:middle">
    <a href="https://your-project-page.com">
      <span class="papertitle">Your Paper Title</span>
    </a>
    <br>
    <strong>Xiangyu Zeng</strong>,
    <a href="https://co-author.com">Co-Author Name</a>
    <br>
    <em>Conference/Journal Name</em>, 2025
    <br>
    <a href="https://arxiv.org/abs/xxxx.xxxxx">arXiv</a>
    <p></p>
    <p>Brief description of your paper.</p>
  </td>
</tr>
```

---

## 🎨 How to Create a Project Page

To create a standalone project page for a paper:

1. Create a folder, e.g., `my-project/`
2. Create the following structure:
   ```
   my-project/
   ├── index.html      # Project main page
   ├── css/
   │   └── app.css     # Custom styles
   └── img/            # Project images and videos
   ```
3. Link from main page:
   ```html
   <a href="my-project/">project page</a>
   ```

---

## 🚀 Deployment

1. **Push to GitHub**:
   ```bash
   git add .
   git commit -m "Update homepage"
   git push origin master
   ```

2. **Enable GitHub Pages**:
   - Go to repository Settings → Pages
   - Set Source to `master` branch
   - Wait a few minutes for deployment

3. **Custom Domain** (Optional):
   - Create a `CNAME` file in root directory
   - Add your domain, e.g., `yourdomain.com`
   - Configure DNS at your domain registrar

---

## 📝 Stylesheet Reference

### Key CSS Classes in stylesheet.css

| Class | Description |
|-------|-------------|
| `.name` | Name style at top (32px font) |
| `.papertitle` | Paper title style (14px bold) |
| `.one` / `.two` | Image hover animation containers |
| `.highlight` | Highlighted text background |

### Color Palette

| Color | Usage |
|-------|-------|
| `#1772d0` | Default link color |
| `#f09228` | Link hover color |
| `#ffffd0` | Highlighted paper background |

---

## 📚 References

- [Original Template](https://github.com/jonbarron/jonbarron.github.io)
- [GitHub Pages Documentation](https://docs.github.com/en/pages)
