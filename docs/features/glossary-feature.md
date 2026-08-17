---
title: "Glossary feature"
icon: lucide/arrow-down-a-z
tags:
  - Features
---
# Glossary
- The [[glossary]] is a site-wide list of every concept, generated from the [[wikilink|wikilinks]].
    - A new wikilink concept appears in the glossary on the next build.

# [[Glossary views]]
1. [[By page]]
2. [[Alphabetical]]
3. [[By importance]]
- | View | Groups concepts by | Good for |
    | --- | --- | --- |
    | By page | The page where the concept first appears | Reviewing one topic |
    | Alphabetical | A to Z | Looking a term up |
    | By importance | Most to least | Looking most used concepts |

## [[By page]] view
- ![Glossary organized by the page where each concept first appears, with concepts listed under module headings.](../assets/attachments/features/glossary-feature/glossary-by-page.png){ width="500" }
    - This view also shows recurring concepts in a different color
        - ![In the By page view, recurring concepts are shown in a different color from newly introduced concepts.](../assets/attachments/features/glossary-feature/glossary-by-page-recur.png){ width="500" }

## [[Alphabetical]] view
- ![Glossary organized alphabetically, with each concept followed by the number of pages containing it and links to those pages.](../assets/attachments/features/glossary-feature/glossary-alphabetical.png){ width="500" }

## [[By importance]] view
- ![Glossary ranked by most-mentioned concepts, showing each concept’s number of mentions, number of pages, and links to those pages.](../assets/attachments/features/glossary-feature/glossary-importance.png){ width="500" }

# Glossary #settings
- Glossary is customized in [[zensical.toml]] file.
    - ```toml linenums="1" 
    [project.extra.knotis.glossary]
    enabled = true
    default_view = "by_page"
    page_view_label = "Pages"
    exclude_paths = []
    order = []
    ```
        - **Line 2:** Default is `true`. `false` turns the glossary feature.
            - When enabled, Knotis generates a `glossary.md` page.
        - **Line 3:** Starting view: `alphabetical` or `by_page`.
        - **Line 4:** Label on the by-page view button.
        - **Line 5:** Skip concepts that appear only on these paths.
        - **Line 6:** In the **by page** view, sections or pages are ordered.

