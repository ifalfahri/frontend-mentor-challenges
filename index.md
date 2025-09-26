---
layout: default
title: Frontend Mentor Challenges
---

# Frontend Mentor Challenges

This page automatically lists challenges (folders that have an `index.html` or `index.md` file).

<ul>
{%- comment -%}
Get all pages that:
- are not root ('/')
- have basename 'index' (meaning files named index.*)
{%- endcomment -%}
{%- assign pages_index = site.pages
    | where_exp: "p", "p.basename == 'index'"
    | where_exp: "p", "p.url != '/'"
-%}

{%- assign pages_sorted = pages_index | sort: "url" -%}

{%- for p in pages_sorted -%}
    {%- assign segs = p.url | split: "/" -%}
    {%- comment -%}
    Example: "/qr-code/" → ["", "qr-code", ""]
    Get the second-to-last segment as the folder name.
    {%- endcomment -%}
    {%- assign folder = segs[segs.size - 2] -%}
    {%- assign label = folder
            | replace: "-", " "
            | replace: "_", " "
            | split: " "
            | map: "capitalize"
            | join: " "
    -%}
    <li>
        <a href="{{ p.url | relative_url }}">
            <strong>{{ label }}</strong>
            <br><small><code>{{ folder }}/</code></small>
        </a>
    </li>
{%- endfor -%}

{%- if pages_sorted == empty -%}
    <li><em>No challenges found yet.</em></li>
{%- endif -%}
</ul>
