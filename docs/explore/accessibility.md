---
title: "Accessibility"
icon: fontawesome/solid/universal-access
tags:
  -
---

# Conformance status
- Knotis’s runtime and generated interface components have been evaluated against the applicable Web Content Accessibility Guidelines (WCAG) 2.2 Level A and Level AA success criteria within the scope described below.
- Automated checks, source review, rendered checks, graph-equivalence checks, and human testing found no known WCAG 2.2 Level A or AA violations in the Knotis-owned features that were evaluated.
    - The current status is therefore: **verified for WCAG 2.2 Level A and Level AA within the stated Knotis-runtime scope**.

# Scope of verification
- The evaluation covers Knotis generated page structure, navigation, search, wikilinks, context panes, glossary controls, graphs and their accessible tables, slides, media controls, read aloud controls, dialogs, keyboard behavior, focus behavior, responsive layout, theme colors, and reduced-motion behavior.
- It does not cover text, images, videos, tables, custom HTML, content colors, third-party embeds, or external services supplied by a site author.
    - Those materials must be evaluated by the site author.

# Accessibility features
- Knotis currently includes the following accessibility-oriented features in its generated interface where the relevant feature is enabled:
    - Semantic page, navigation, article, search, pane, and dialog structures;
    - Keyboard paths for search, wikilinks, pane controls, graph controls, slides, media controls, and read-aloud controls;
    - A compact universal-access icon control with paginated graph nodes and relationships;
    - Labelled buttons, inputs, view switches, filters, and dialog controls;
    - Visible focus styling for custom Knotis controls;
    - Escape handling for dismissible overlays and dialogs;
    - Focus restoration for search, slide view, graph dialogs, and image lightboxes;
    - Keyboard containment while graph and image dialogs are open;
    - Native links and buttons for generated search continuation, wikilink, content-tag, glossary, and pane interactions;
    - Support for `prefers-reduced-motion` for nonessential Knotis animation and transitions;
    - Keyboard controls for Knotis GIF players; and
    - Support for captions supplied through supported sibling WebVTT files.
- These features describe the Knotis runtime. Site authors remain responsible for the accessibility of the content they add to a generated site.

# Verification summary
- An isolated Knotis scaffold was crawled across 14 generated routes at 320px, 768px, and 1280px.
- Its WCAG A/AA axe scans reported zero violations at each viewport.
- Human testing covered keyboard workflows, focus behavior, contrast, zoom, reflow, text spacing, screen-reader interaction, and graph equivalence for the Knotis-owned features in scope, with no known violations identified.
- Author content and third-party services remain outside this statement.

# Content-author responsibilities
- Site authors are responsible for providing accessible content, including:
    - meaningful alternative text, or an intentional empty alternative for decorative images;
    - captions and, where appropriate, transcripts or audio descriptions for media;
    - logical heading structure and descriptive link text;
    - table headers and appropriate table structure;
    - sufficient contrast for custom colors and content tags; and
    - accessible alternatives or explanations for third-party applications and embedded content.

# Feedback and contact
- For reports about accessibility issues, please contact:
    - **Accessibility contact:** Tolga Tezcan
    - **Email:** ttezcan@csumb.edu
    - **Issue tracker:** [Report the issue here](https://github.com/ttezcann/knotis/issues){: target="_blank" rel="noopener" }
        - When reporting a problem, please include feature, the action that caused difficulty, the browser and assistive technology involved if known.

# Integrated audit evidence
## Evaluation method
- Source inspection reviewed ARIA, roles, focus management, keyboard handlers, dialogs, live regions, SVGs, headings, landmarks, motion, media behavior, and generated HTML.
- Targeted JavaScript regression tests, JavaScript syntax checks, and a successful Knotis site build verified the implementation.
- An isolated Knotis scaffold was crawled across 14 generated routes at 320px, 768px, and 1280px, and WCAG A/AA axe scans reported zero violations at each viewport.
- The automated graph-SVG contrast rule was incomplete, so rendered graph states were reviewed manually.
- Human testing covered keyboard workflows, focus restoration, screen-reader interaction, live status behavior, light/dark contrast, focus indicators, 200% and 400% zoom, text spacing, narrow reflow, sticky overlays, media controls, graph equivalence, drag alternatives, and relationship distinctions.
- The accessible graph tables were compared with the corresponding page, concept, and filtered site graph data.

## Verified Knotis-owned areas
- Base page structure and navigation expose generated landmarks, headings, skip links, document language, focus styles, and accessible navigation state.
- Search provides keyboard operation, labelled filters, result status messages, meaningful generated links, and focus restoration.
- Wikilinks, context panes, glossary controls, and image lightboxes provide native controls, accessible names, keyboard operation, focus containment where required, and focus restoration.
- Graphs provide keyboard-openable accessible dialogs with scoped, paginated node and relationship tables, correct page links, concept-pane actions, relationship-pane actions, and preserved visual graph behavior.
- Slides provide labelled dialogs, table-of-contents and navigation controls, slide status messages, keyboard operation, and focus restoration.
- Media controls provide keyboard-operable Knotis GIF controls, native video controls where supported, and sibling WebVTT caption support.
- Read aloud provides labelled controls and status behavior as an optional enhancement and does not replace screen-reader support.
- Theme and responsive behavior were reviewed for reduced motion, contrast, focus visibility, text spacing, zoom, reflow, target size, and sticky-overlay behavior.

## WCAG 2.2 Level A and AA evidence matrix

- | Criterion | Level | Status | Evidence and scope |
  |---|---:|---|---|
  | 1.1.1 Non-text Content | A | Verified in scope | Knotis-owned SVGs and controls have alternatives or are decorative-hidden; author media is excluded. |
  | 1.3.1 Info and Relationships | A | Verified in scope | Generated headings, TOC, glossary, tables, panes, and dialogs were reviewed; authored structure is excluded. |
  | 1.3.2 Meaningful Sequence | A | Verified in scope | Generated page, pane, slide, graph-dialog, and outline sequences were reviewed. |
  | 1.4.3 Contrast (Minimum) | AA | Verified in scope | Knotis-owned light/dark text, controls, focus, and graph states were reviewed with axe and manual rendered checks. |
  | 1.4.10 Reflow | AA | Verified in scope | Generated routes and feature dialogs were checked at narrow layouts and 200%/400% zoom. |
  | 1.4.12 Text Spacing | AA | Verified in scope | Required text-spacing overrides were applied and reviewed without loss of content or functionality. |
  | 2.1.1 Keyboard | A | Verified in scope | Generated navigation, search, panes, graphs, slides, media, and native controls were operated by keyboard. |
  | 2.1.2 No Keyboard Trap | A | Verified in scope | Dialog and overlay focus behavior was reviewed, including Escape and exit paths. |
  | 2.4.1 Bypass Blocks | A | Verified in scope | The generated skip link was present and operable. |
  | 2.4.2 Page Titled | A | Verified in scope | Generated routes had meaningful page titles. |
  | 2.4.3 Focus Order | A | Verified in scope | Search, panes, graphs, slides, lightboxes, and dialog opener restoration were reviewed. |
  | 2.4.4 Link Purpose | A | Verified in scope | Generated links and graph page links have meaningful destinations; author links are excluded. |
  | 2.4.7 Focus Visible | AA | Verified in scope | Knotis-owned controls expose visible focus styling in light and dark modes. |
  | 2.4.11 Focus Not Obscured | AA | Verified in scope | Sticky chrome, panes, dialogs, and expanded graph controls were reviewed at tested viewports. |
  | 2.5.1 Pointer Gestures | A | Verified in scope | Required graph and pointer interactions have keyboard or control alternatives. |
  | 2.5.7 Dragging Movements | AA | Verified in scope | Graph dragging is optional positioning and is not required to access graph information or actions. |
  | 2.5.8 Target Size | AA | Verified in scope | Knotis-owned controls meet the applicable 24×24px minimum or exception. |
  | 3.1.1 Language of Page | A | Verified in scope | Generated pages expose the configured document language. |
  | 4.1.2 Name, Role, Value | A | Verified in scope | Generated controls, dialogs, tables, graph actions, and states expose accessible names, roles, and values. |
  | 4.1.3 Status Messages | AA | Verified in scope | Search, slides, graph pagination, and other generated status messages were reviewed. |

# Date and review
- **Statement published:** 17 September 2026
- **Last reviewed:** 17 September 2026
- **Next review:** After a significant accessibility-related change or a reported issue.