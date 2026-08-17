---
title: "Pane feature"
icon: lucide/panel-right
tags:
  - Features
---
# [[Pane]]
- The pane is the side panel that opens when a [[wikilink]] is clicked.
    - It gathers every place that concept appears across the site and shows them together, without leaving the current page.
    - Wikilinks and [[content tags]] inside the pane are also clickable, so a user can move between concepts without closing the pane.
    - If the concept is defined as [[reference]], the pane only shows the reference card.
- **Why [[outlining]] matters:**
    - The pane builds each occurrence from the bullet and heading hierarchy written in the page.
    - A child bullet is shown nested under its parent.

# [[Pane view]]
- ![Pane showing details for the “Linear regression” concept. Numbered callouts identify the pane header and mention count (1), concept graph (2), return-to-graph control (3), pages in the path (4), concept content and highlighted links (5), share control (6), and close button (7).](../assets/attachments/features/pane-feature/pane-details.png)
    1. This is the pane of "linear regression" wikilink.
        1. This part shows the number of mentions and pages including this concept, with back/forward controls.
    2. Shows the [[concept graph]] of "linear regression" wikilink.
        1. Clicking on the graph preview expands the graph.
    3. **Return button :lucide-undo-2:**: Appears only when the pane was opened from a site, page, or concept graph node click, and returns to that graph.
        1. "Site graph :lucide-undo-2:" appears because linear regression wikilink was clicked on the site graph.
        2. After reviewing this concept in the pane, users can go back to the site graph with that button.
    4. [[Path]]: The pages mentioning this concept.
        1. Clicking on one of the pages on path will scroll the pane.
    5. The content. Wikilinks are highlighted in blue, same concept without wikilinks are highlighted in yellow.
        1. **Minimize cards** :lucide-minus: to scroll through a long list of entries faster.
        2. **Scroll context** with ↑/↓ buttons to read more of the surrounding content, if more context available under the sections.
        3. **Clicking cards** to navigate to that exact location on the page and keeps the pane closed.
    6. **Share:** Pane card state IDs are included the page URL.
        1. Copy the URL to share a specific pane view with users; the link opens that pane and its current cards.
    7. **Close button:** Closes the pane.
        1. It can be reopened with the "Pane" button :lucide-panel-right-open: in the heading.
        2. It restores the views, and the ←/→ buttons navigate backward and forward through the view history.

# Pane #settings
- Pane is customized in [[zensical.toml]] file.
    - ```toml linenums="1" 
    [project.extra.knotis.pane]
    width = 750
    initial_lines = 12
    initial_list_items = 20
    chunk_lines = 4
    order = []
    ```
        - **Line 2:** Pane width in pixels.
        - **Line 3:** Sets how much of each card shows before "show more."
        - **Line 4:** Maximum number of list items shown in the initial card window.
        - **Line 5:** Number of lines revealed per ↓ or ↑ context expansion step.
        - **Line 6:** In the **by page** view, sections or pages are ordered.
            - Example: order = ["features", "workflows", "what-is-knotis.md"] → features pages, then workflows, then that page, then the rest.

# Pane [[path]] #settings
- Pane path is customized in [[zensical.toml]] file.
    - ```toml linenums="1" 
    [project.extra.knotis.pane.path]
    enabled = true
    include_paths = []
    exclude_paths = []
    ```
        - **Line 2:** Default is `true`. `false` turns the path feature off.
        - **Line 3:** Sections or pages that may show path.
        - **Line 4:** Sections or pages to remove from `include_paths`.
