---
title: "Home"
icon: lucide/house
knotis_content:
  heading_numbering: false
---

![The Knotis logo.](assets/attachments/0-logo/knotis-lockup.png){align=left width="300" }
Knotis is a teaching-focused [Zensical](https://zensical.org) wrapper. 

It turns Markdown notes into a website where ideas are connected.

It is built for **instructional materials**.

[:material-help-circle-outline: What is Knotis?](../getting-started/what-is-knotis.md){ .md-button .md-button--primary }

# Installation
- :lucide-badge-check: **Prerequisite:** Install :fontawesome-brands-python: Python 3.11+ from [python.org](https://www.python.org/downloads/).

    === ":material-apple: macOS"
        - ```bash
        python3 -m venv .venv
        source .venv/bin/activate
        pip install knotis
        ```
            - :lucide-download: [Installation details](../getting-started/install-knotis.md)
    === ":fontawesome-brands-windows: Windows"
        - ```powershell
        python3 -m venv .venv
        .venv\Scripts\activate
        pip install knotis
        ```
            - :lucide-download: [Installation details](../getting-started/install-knotis.md)
    === ":material-linux: Linux"
        - ```bash
        python3 -m venv .venv
        source .venv/bin/activate
        pip install knotis
        ```
            - :lucide-download: [Installation details](../getting-started/install-knotis.md)

# Features

<div class="grid cards" markdown>

-   :lucide-list-tree:{ .lg .middle } __[Outlining](features/outlining-feature.md)__

    ---

    Written as nested bullets, and nesting becomes graph edges and pane context.

-   :lucide-brackets:{ .lg .middle } __[Wikilinks](features/wikilinks-feature.md)__

    ---

    The double-bracket, `[[concept]]` syntax that names a concept and links it everywhere it appears.

-   :lucide-panel-right:{ .lg .middle } __[Pane](features/pane-feature.md)__

    ---

    A side panel that shows every place a concept appears, without leaving
    the page.

-   :lucide-share-2:{ .lg .middle } __[Graphs](features/graphs-feature.md)__

    ---

    Site, page, and concept graphs built from the course outline.

-   :lucide-search:{ .lg .middle } __[Search](features/search-feature.md)__

    ---

    Concept-aware search that ranks concepts and tagged content.

-   :lucide-hash:{ .lg .middle } __[Content tags](features/content-tags-feature.md)__

    ---

    Labels a section or block like `#example` and groups matching sections
    site-wide.

-   :lucide-arrow-down-a-z:{ .lg .middle } __[Glossary](features/glossary-feature.md)__

    ---

    A course glossary generated from the concepts already written in the
    lessons.

-   :lucide-presentation:{ .lg .middle } __[Slide mode](features/slide-mode-feature.md)__

    ---

    Any page can open as a full-screen slideshow.

-   :lucide-headphones:{ .lg .middle } __[Read aloud](features/read-aloud-feature.md)__

    ---

    A built-in text-to-speech button.

-   :lucide-video:{ .lg .middle } __[Video controls](features/video-controls-feature.md)__

    ---

    GIFs and MP4s get play/pause, scrubbing, first-frame previews, playback speed, and captions.

</div>
