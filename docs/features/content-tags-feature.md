---
title: "Content tags feature"
icon: lucide/hash
tags:
  - Features
---
# [[Content tags]]
- Content tags are content labels that mark sections of a page as a specific kind of material.
    - Unlike [[wikilink|wikilinks]] which connect concepts across pages, content tags group content by *what it is*:
        - A `#code` example, an `#output` table, or an `#interpretation` writeup,
        - A `#formula`,
        - An `#example`,
        - A `#discussion` prompt.
    - For this site, we have two content tags:
        1. `#settings`, and
        2. `#tip`.
- Clicking a content tag opens every matching section from across the site.
    - Wikilinks connect ideas.
    - Content tags collect reusable kinds of content.

# [[Content tags]] sidebar
- Content tags  appear as colored chips in the left sidebar.
    - Clicking a content tag chip in the home page opens the pane.
    - This makes common content types easy to reach.
        - ![Home page sidebar showing colored content-tag chips such as `#code`, `#output`, and `#interpretation`; an arrow points to the tags.](../assets/attachments/getting-started/what-is-knotis/content-tags.png)
    - When a content tag chip is clicked on a page, results are grouped by page.
        - The current page appears first.
        - The clicked section appears first inside that page.
            - ![Clicking `#output` opens a pane listing matching output sections, grouped by page, with the current page shown first.](../assets/attachments/features/content-tags-feature/content-tags-output.png)
# [[Content tags]] rules
- Content tags:
    - are case-insensitive.
        - `#Settings` and `#settings` are the same tag.
    - must start with a letter.
    - can use letters, numbers, hyphens, and underscores.
    - **cannot** contain spaces.
    - inside code blocks or inline code are ignored.
- !!! info "How many content tags? #tip"
    - Content tags group repeated content types; they are not for flagging important terms.
        - A maximum of 5 content tags is allowed.

# [[Content tags]] and [[search]]
- [[Search]] understands content tags.
    - Searching `frequency table #code` finds code sections about frequency tables.
    - Searching `frequency table code` can also find `#code` sections.
- Content tags do not create [[glossary]] entries or [[graphs|graph]] nodes.
    - They label content.
    - They do not become concepts.

# [[Content tags]] #settings
- Content tags are customized in [[zensical.toml]] file.
     ```toml linenums="1" hl_lines="2 3 5 7 8 9 11 12 13"
    [project.extra.knotis.content-tags]
    enabled = true
    nav_chips = true
    order = ["content-tag-1", "content-tag-2"]
    [project.extra.knotis.content_tags.colors.default]
    content-tag-1 = "#067647"
    content-tag-2 = "#b45309"
    [project.extra.knotis.content_tags.colors.slate]
    content-tag-1 = "#79d7a7"
    content-tag-2 = "#ffbf7d"
    ```
        - **Line 2:** Default is `true`. `false` turns off the generated content tags page.
            - Panes and search can still use content tags.
        - **Line 3:** Default is `true`. `false` hides tag chips in the sidebar.
        - **Line 5:** Optional argument to change the order of the tag chips in the sidebar.
            - Replace here with the actual content tags: `content-tag-1`, `content-tag-2`, and so on.
        - **Lines 7-8-9:** Optional argument to change the colors of the tag chips in light mode.
        - **Lines 11-12-13:** Optional argument to change the colors of the tag chips in dark mode.