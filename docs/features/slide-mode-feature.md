---
title: "Slide mode feature"
icon: lucide/presentation
tags:
  - Features
---
<!-- slide-break font=60px -->
# [[Slide mode]]
- Slide mode turns a page into a full-screen slideshow without a separate deck.
    - Slides are built for instructors, to present directly from the site.
    - Users can still read the same page as an ordinary lesson.
- !!! Info "Click "Slides""
    - This page is customized as slideshow.
        - Click "Slides" button at the header.
<!-- slide-break -->
# [[Slide view]]
- ![Slide mode shown in three stages: 1 a full-screen individual slide with controls to return to the slide overview or exit; 2 the slide overview with multiple slides and a Slideshow control; 3 the regular lesson page with Continue Slides and a return control in the header.](../assets/attachments/features/slides-feature/slideshow.png)
<!-- slide-break -->
    1. Open a lesson page that has slides enabled.
        1. Click **Slides** in the header.
        1. The slideshow opens full-screen.
            1. Click burger menu to see the slide titles and change the slides
            1. Press ++esc++ or click the close button to exit the full screen.
    1. Exiting full screen makes slides as scrollable cards.
        1. Click burger menu to see the slide titles and change the slides and open as full screen
        1. Scroll the slide cards and click the one to open as full screen
        1. Press ++esc++ or click the close button to go back to the page content, at the same spot.
    1. Exiting from the scrollable cards view will land to the exact page content.
        1. Click **"Continue slides"** to return to the same slide.
        1. A small restart button (↻) appears next to Continue Slides. Click it to open a slideshow of a different page.
<!-- slide-break -->
# Enabling slides #settings
- Slides are turned on and customized in [[zensical.toml]] file.
    - ```r linenums="1" 
    [project.extra.knotis.slides]
    enabled = true
    include_paths = []
    exclude_paths = []
    fit_min_font_px = 26
    fit_max_font_px = 42
    content_fill = 0.99
    content_inset = [2, 2, 2, 2]
    ```
        - **Line 2:** Default is `false`. `true` turns the slides feature.
        - **Line 3:** Sections or pages that may show slides.
            - `"lessons"`
            - `"lessons/lesson-1.md"`
        - **Line 4:** Pages to remove from `include_paths`.
        - **Line 5:** Smallest preferred text size. Dense slides may go smaller so everything stays visible.
        - **Line 6:** Largest text size for short slides.
        - **Line 7:** How much of the slide area short content should grow to fill (from `0.35` to `1.0`).
            - Higher values use more of the screen; lower values leave more empty space.
        - **Line 8:** Margins around slide content as percentages: `[top, right, bottom, left]`.
            - Smaller values give content more room. Each value can be `0` through `20`.
<!-- slide-break font=60px-->
# [[Preparing slides]]
- Slides are built from the module page content.
    - There are two types of slides based on control.
<!-- slide-break -->
## [[Automatic slides]]
- The system decides slide boundaries automatically.
- Each major heading (H1, H2, H3) and its body content can become a slide.
    - Long sections are split into several slides.
    - Large items such as tables, code blocks, diagrams, and admonition boxes usually get their own slide.
    - Long code lines keep the page layout and pan horizontally without wrapping or showing a scrollbar track.
    - The page-style copy control remains visible at the right edge of slide code blocks.
- Slides appear in the same order as the content on the page.
- There is no way to exclude certain headings/sections.
<!-- slide-break -->
## [[Manual slides]] #settings
- Exact control over what appears on each slide with following markers:
    - | Marker | Effect |
      | --- | --- |
      | `<!-- slide-break -->` | Opens a slide; the next `<!-- slide-break -->` closes it. <br> Content between those markers is one slide. |
      | `<!-- slide-end -->` | Closes the current slide without starting another. <br> This is to omit sections and end the slideshow. |
      | `<!-- slide-break click -->` | Lists items reveal one at a time on the next ++arrow-right++. |
      | `<!-- slide-break step -->` | Treats each top-level as one step on the next ++arrow-right++. |
      | `font=` | `<!-- slide-break font=32px -->` <br><br> Fixes the slide's text size (`8px` to `99px`) instead of auto-fitting between `fit_min_font_px` and `fit_max_font_px`. |
      | `fill=` | `<!-- slide-break fill=90% -->` <br><br> Overrides `content_fill` for specific slides only. <br>Accepts `35%` to `100%`, or `0.35` to `1.0`.|
        - !!! tip "Combination #tip" 
            - Options can be combined on one marker:
                - `<!-- slide-break step font=30px fill=80% -->`
<!-- slide-end -->
