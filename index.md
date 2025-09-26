---
layout: default
title: Frontend Mentor Challenges
---

# 🎨 Frontend Mentor Challenges

Welcome to my collection of [Frontend Mentor](https://www.frontendmentor.io) challenge solutions! Each project demonstrates different aspects of modern web development, from responsive design to interactive components.

## 📋 Challenge List

Below are all the completed challenges in this repository:

<style>
.challenge-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
    gap: 1.5rem;
    margin: 2rem 0;
}

.challenge-card {
    border: 2px solid #e2e8f0;
    border-radius: 12px;
    padding: 1.5rem;
    transition: all 0.3s ease;
    text-decoration: none;
    display: block;
    background: #ffffff;
    box-shadow: 0 2px 4px rgba(0,0,0,0.1);
}

.challenge-card:hover {
    transform: translateY(-2px);
    box-shadow: 0 8px 25px rgba(0,0,0,0.15);
    border-color: #3b82f6;
    text-decoration: none;
}

.challenge-title {
    font-size: 1.25rem;
    font-weight: 600;
    color: #1e293b;
    margin-bottom: 0.5rem;
}

.challenge-path {
    font-family: 'SF Mono', 'Monaco', 'Inconsolata', 'Roboto Mono', monospace;
    font-size: 0.875rem;
    color: #64748b;
    background: #f1f5f9;
    padding: 0.25rem 0.5rem;
    border-radius: 4px;
    display: inline-block;
}

.no-challenges {
    text-align: center;
    color: #64748b;
    font-style: italic;
    padding: 3rem;
    background: #f8fafc;
    border-radius: 8px;
    border: 2px dashed #cbd5e1;
}

@media (max-width: 768px) {
    .challenge-grid {
        grid-template-columns: 1fr;
        gap: 1rem;
    }
    
    .challenge-card {
        padding: 1rem;
    }
}
</style>

{%- comment -%}
Scan for both Jekyll pages and static HTML files to find all challenge folders
{%- endcomment -%}

{%- comment -%}Get Jekyll pages with front matter{%- endcomment -%}
{%- assign pages_index = site.pages
    | where_exp: "p", "p.basename == 'index'"
    | where_exp: "p", "p.url != '/'"
-%}

{%- comment -%}Get static index.html files without front matter{%- endcomment -%}
{%- assign static_index = site.static_files
    | where: "basename", "index"
    | where: "extname", ".html"
-%}

{%- comment -%}Build list of unique challenge folders{%- endcomment -%}
{%- assign folders = "" | split: "" -%}

{%- comment -%}Extract folders from Jekyll pages{%- endcomment -%}
{%- for p in pages_index -%}
{%- assign segs = p.url | split: "/" -%}
{%- assign folder = segs[segs.size - 2] -%}
{%- unless folders contains folder -%}
{%- assign folders = folders | push: folder -%}
{%- endunless -%}
{%- endfor -%}

{%- comment -%}Extract folders from static files{%- endcomment -%}
{%- for f in static_index -%}
{%- assign segs = f.path | split: "/" -%}
{%- assign folder = segs[segs.size - 2] -%}
{%- unless folders contains folder -%}
{%- assign folders = folders | push: folder -%}
{%- endunless -%}
{%- endfor -%}

{%- assign folders_sorted = folders | sort -%}

<div class="challenge-grid">
{%- for folder in folders_sorted -%}
    {%- assign label = folder
            | replace: "-", " "
            | replace: "_", " "
            | split: " "
            | map: "capitalize"
            | join: " "
    -%}
    <a href="{{ '/' | append: folder | append: '/' | relative_url }}" class="challenge-card">
        <div class="challenge-title">{{ label }}</div>
        <div class="challenge-path">{{ folder }}/</div>
    </a>
{%- endfor -%}

{%- if folders_sorted == empty -%}
<div class="no-challenges">
🔍 No challenges found yet.<br>
<small>Add folders with <code>index.html</code> files to get started!</small>
</div>
{%- endif -%}

</div>

---

### 🔗 Links

- [Frontend Mentor](https://www.frontendmentor.io) - The source of these challenges
- [My Profile](https://www.frontendmentor.io/profile/{{ site.github.owner_name | default: "your-username" }}) - See my other solutions
