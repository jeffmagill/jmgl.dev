---
title: Lorem Ipsum Formatting Reference
description: A kitchen-sink post showing every formatting option the blog supports. Delete before launch.
date: 2026-10-08
---

Lorem ipsum dolor sit amet, consectetur adipiscing elit. This post exists to show **every formatting option** the site supports, so you can see how each one renders and copy the syntax. Open the Markdown source next to the rendered page and compare.

## Inline text

Plain paragraph text with **bold**, *italic*, ***bold italic***, ~~strikethrough~~, `inline code`, and a [link to somewhere](https://jmgl.dev). Keyboard keys use HTML: press <kbd>Ctrl</kbd> + <kbd>K</kbd>. You can <mark>highlight</mark> text, add H<sub>2</sub>O subscripts and E = mc<sup>2</sup> superscripts. Footnotes look like this.[^1]

Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo.

## Headings

Section headings start at `##` (the post title is the only `#`). Hover a heading to see its anchor link, so you can link people straight to a section.

### Third-level heading

Nemo enim ipsam voluptatem quia voluptas sit aspernatur aut odit aut fugit.

#### Fourth-level heading

Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet.

## Lists

Unordered:

- Lorem ipsum dolor sit amet
- Consectetur adipiscing elit
  - Nested item one
  - Nested item two
- Sed do eiusmod tempor

Ordered:

1. Identify the problem
2. Find where it actually starts
3. Fix it there, not downstream
   1. Nested step
   2. Another nested step

Task list:

- [x] Pick a static site generator
- [ ] Write the first four posts
- [ ] Share the link

## Blockquote

> Ut enim ad minima veniam, quis nostrum exercitationem ullam corporis suscipit laboriosam, nisi ut aliquid ex ea commodi consequatur.
>
> — Someone quotable

## Pull quote / callout

Use a little HTML when you want something to stand out:

<aside class="callout">
<strong>Takeaway:</strong> Lorem ipsum dolor sit amet. Callouts are good for the one sentence you want a skimmer to remember.
</aside>

## Code

Inline: run `npm run build`.

Fenced, with syntax highlighting:

```js
// eleventy.config.js
export default function (eleventyConfig) {
  eleventyConfig.addPassthroughCopy("src/css");
  return { dir: { input: "src", output: "_site" } };
}
```

```python
def triage(error):
    """Walk the stack upstream until the bad data first appears."""
    for layer in ["dashboard", "semantic_model", "dbt", "warehouse", "source"]:
        if not layer_is_clean(layer, error):
            return layer
    return "unknown"
```

```sql
select order_date, count(*) as orders
from fct_orders
where order_date >= current_date - interval '30 days'
group by 1
order by 1;
```

```bash
npm install
npm start   # local preview at http://localhost:8080
```

Diff blocks are useful for before/after:

```diff
- theme: minima
- plugins: [jekyll-feed]
+ "@11ty/eleventy": "^3.1.6"
```

## Table

| Option   | Templating        | Stars | Verdict      |
|:---------|:------------------|------:|:-------------|
| Jekyll   | Liquid            |  49k  | Unenthused   |
| Hugo     | Go templates      |  90k  | Awkward      |
| Astro    | Components        |  60k  | Close second |
| Eleventy | Nunjucks / JS     |  22k  | **Chosen**   |

## Images

Put images in `src/img/` and reference them with an absolute path. Alt text is required for accessibility.

<figure>
  <svg viewBox="0 0 640 200" role="img" aria-label="Placeholder image" style="width:100%;height:auto;background:var(--code-bg);border-radius:8px">
    <text x="50%" y="50%" text-anchor="middle" dominant-baseline="middle" fill="currentColor" font-family="system-ui" font-size="20">640 × 200 placeholder</text>
  </svg>
  <figcaption>A figure with a caption. Markdown syntax: <code>![Alt text](/img/photo.jpg)</code></figcaption>
</figure>

## Horizontal rule

Quis autem vel eum iure reprehenderit qui in ea voluptate velit esse.

---

At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium voluptatum deleniti atque corrupti quos dolores.

## Collapsible details

<details>
<summary>Click to expand the boring part</summary>

Temporibus autem quibusdam et aut officiis debitis aut rerum necessitatibus saepe eveniet ut et voluptates repudiandae sint.

</details>

## Footnotes

Footnotes collect at the bottom automatically.[^2]

[^1]: This is a footnote. Good for asides that would derail the paragraph.
[^2]: And a second one, just to show the numbering.
