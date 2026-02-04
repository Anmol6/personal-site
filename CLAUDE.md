# Personal Site

Anmol's personal portfolio and blog. Hosted on GitHub Pages at anmoljawandha.com.

## Structure

```
/
├── index.html          # Main portfolio page
├── blog/
│   ├── images/         # Blog post images
│   └── *.html          # Individual blog posts
└── CLAUDE.md
```

## Tech Stack

- Pure HTML + embedded CSS (no frameworks, no build step)
- Google Fonts (Inter, weights 400 & 600)
- GitHub Pages for hosting

## Styling

CSS variables defined in each file:
```css
--bg-color: #fff;
--text-color: #333;
--accent-color: #3a86ff;
--muted-color: #718096;
--border-radius: 12px;
```

Design principles:
- Minimal and clean
- No emojis
- Subtle hover transitions (opacity 0.8 for links, border-color for cards)
- 700px max-width for blog posts, 1000px for main page

## Writing Blog Posts

### File location
Create new posts at `blog/<slug>.html`

### HTML template
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Post Title | Anmol</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600&display=swap" rel="stylesheet">
    <style>
        :root {
            --bg-color: #fff;
            --text-color: #333;
            --accent-color: #3a86ff;
            --muted-color: #718096;
            --border-radius: 12px;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            font-family: 'Inter', -apple-system, sans-serif;
            line-height: 1.6;
            color: var(--text-color);
            max-width: 700px;
            margin: 0 auto;
            padding: 2rem;
            background-color: var(--bg-color);
            font-size: 16px;
        }

        a {
            color: var(--accent-color);
            text-decoration: none;
            transition: opacity 0.15s ease;
        }

        a:hover {
            opacity: 0.8;
        }

        .back-link {
            display: inline-block;
            margin-bottom: 2rem;
            font-size: 0.9rem;
        }

        h1 {
            font-size: 2rem;
            font-weight: 600;
            margin-bottom: 0.5rem;
        }

        .date {
            color: var(--muted-color);
            font-size: 0.9rem;
            margin-bottom: 2rem;
        }

        h2 {
            font-size: 1.4rem;
            font-weight: 600;
            margin-top: 2rem;
            margin-bottom: 1rem;
        }

        h3 {
            font-size: 1.1rem;
            font-weight: 600;
            margin-top: 1.5rem;
            margin-bottom: 0.75rem;
        }

        p {
            margin-bottom: 1rem;
        }

        ul, ol {
            margin-bottom: 1rem;
            padding-left: 1.5rem;
        }

        li {
            margin-bottom: 0.5rem;
        }

        strong {
            font-weight: 600;
        }

        em {
            font-style: italic;
        }

        img {
            max-width: 100%;
            border-radius: 12px;
            margin: 1.5rem 0;
        }

        .caption {
            font-size: 0.85rem;
            color: var(--muted-color);
            text-align: center;
            margin-top: -1rem;
            margin-bottom: 1.5rem;
        }

        blockquote {
            border-left: 3px solid var(--accent-color);
            padding-left: 1rem;
            margin: 1.5rem 0;
            color: var(--muted-color);
            font-style: italic;
        }

        code {
            background-color: #f5f5f5;
            padding: 0.2rem 0.4rem;
            border-radius: 4px;
            font-size: 0.9em;
        }

        pre {
            background-color: #f5f5f5;
            padding: 1rem;
            border-radius: var(--border-radius);
            overflow-x: auto;
            margin-bottom: 1rem;
        }

        pre code {
            background: none;
            padding: 0;
        }
    </style>
</head>
<body>
    <a href="../" class="back-link">← Back</a>

    <article>
        <h1>Post Title</h1>
        <div class="date">Month Year</div>

        <p>Content goes here...</p>

        <h2>Section Heading</h2>
        <p>More content...</p>
    </article>
</body>
</html>
```

### Adding images
1. Place images in `blog/images/`
2. Reference with relative path:
```html
<img src="images/filename.png" alt="Descriptive alt text">
<p class="caption">Caption text.</p>
```

### After creating a post
Add entry to `index.html` in the Writing section:
```html
<div class="blog-item">
    <a href="blog/slug.html">Post Title</a>
    <span class="blog-date">Mon YYYY</span>
</div>
```
Posts are ordered newest first.

## Writing Style

- Direct, opinionated, technical
- Short paragraphs
- Use h2 for main sections, h3 for subsections
- Bold key terms with `<strong>`
- Use lists for frameworks/checklists
- Include diagrams when they clarify concepts
- End with actionable takeaways or open questions
