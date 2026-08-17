---
title: "Search feature"
icon: lucide/search
tags:
  - Features
---
# [[Search]]
- Knotis search is a concept-aware search that replaces [[Zensical]]’s default search.
    - It understands [[wikilink|wikilinks]] and plain words.
    - It renders all the content items, Markdown tables, images, Mermaid diagrams, admonitions, code blocks, and videos.
- Click on the :lucide-search: Search bar in the header, or use the keyboard shortcut:
    - :fontawesome-brands-windows:  &nbsp; ++ctrl+k++
    - :fontawesome-brands-apple:  &nbsp; ++command+k++

## [[Search order]]
1. Wikilink-first ranking.
    1. Wikilink concepts outrank non-wikilink concepts.
2. The matching [[reference]] wikilinks.
    1. No duplicate results.
3. Content-tags.
    1. Searching `frequency table #output` finds `#output` sections about the frequency table.
4. Ordinary text that mentions the words without using a wikilink.
# [[Search view]]
- ![Search results for “nonsignificant correlation” entered in the search bar at the top (1). The “Correlation analysis” section is highlighted (2), filters part (3), related concepts are highlighted (4), a “2 more on this page” link is highlighted below the related tags (5)](../assets/attachments/features/search-feature/search-card.png)
    1. User clicks on the :lucide-search: Search bar in the header, or use the keyboard shortcut.
        1. Types the keyword/concept, such as `nonsignificant correlation` to see every module that mentions it, or narrow down with `correlation code` to find only code sections.
    2. The search cards show the module name.
    3. Clicking on [[page tags]] narrows the search.
    4. Right below each search card, there are clickable "RELATED" concepts, and
    5. How many times the searched keyword/concept is mentioned in the same page.
        1. Clicking that number expands the results within that page.
    6. Clicking on a search card to jump directly to that part on the page.
# Search #settings
- Search is customized in [[zensical.toml]] file.
    - ```toml
    [project.extra.knotis.search]
    enabled = true
    exclude_paths = []
    exclude_wikilinks = []
    order = []
    ```
        - **Line 2:** Default is `true`. `false` turns the search feature off.
        - **Line 3:** Sections or pages to remove from the site graph.
        - **Line 4:** Wikilinks to remove from the site graph.
        - **Line 5:** sections or pages are ordered.
            - Example: order = ["features", "workflows", "what-is-knotis.md"] → features pages, then workflows, then that page, then the rest.