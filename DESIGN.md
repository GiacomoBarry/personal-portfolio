---
name: Jack Barry
description: A career filed as an auditable incident record, with ruled fields, a reference, states and work notes.
colors:
  paper: "#F4F4F1"
  ink: "#141414"
  ink-2: "#4A4A46"
  rule: "#BDBDB6"
  rule-soft: "#DCDCD6"
  blue: "#1D3FA8"
  red: "#C4261D"
  carbon-paper: "#141514"
  carbon-ink: "#E9E9E4"
  carbon-ink-2: "#A4A49D"
  carbon-rule: "#474843"
  carbon-rule-soft: "#2A2B28"
  carbon-blue: "#93A8F4"
  carbon-red: "#F0685E"
typography:
  display:
    fontFamily: "Schibsted Grotesk, ui-sans-serif, system-ui, -apple-system, Helvetica Neue, Arial, sans-serif"
    fontSize: "clamp(2.5rem, 5.2vw, 3.6rem)"
    fontWeight: 700
    lineHeight: 1
    letterSpacing: "-0.035em"
  headline:
    fontFamily: "Schibsted Grotesk, ui-sans-serif, system-ui, sans-serif"
    fontSize: "1.375rem"
    fontWeight: 600
    lineHeight: 1.2
    letterSpacing: "-0.015em"
  title:
    fontFamily: "Schibsted Grotesk, ui-sans-serif, system-ui, sans-serif"
    fontSize: "1.3rem"
    fontWeight: 650
    lineHeight: 1.2
    letterSpacing: "-0.01em"
  lead:
    fontFamily: "Source Serif 4, Georgia, Times New Roman, serif"
    fontSize: "clamp(1.4rem, 2.5vw, 1.95rem)"
    fontWeight: 400
    lineHeight: 1.35
    letterSpacing: "-0.005em"
  body:
    fontFamily: "Source Serif 4, Georgia, Times New Roman, serif"
    fontSize: "17px"
    fontWeight: 400
    lineHeight: 1.6
  field-value:
    fontFamily: "Schibsted Grotesk, ui-sans-serif, system-ui, sans-serif"
    fontSize: "1.05rem"
    fontWeight: 500
    lineHeight: 1.3
  label:
    fontFamily: "Schibsted Grotesk, ui-sans-serif, system-ui, sans-serif"
    fontSize: "0.72rem"
    fontWeight: 600
    letterSpacing: "0.06em"
  data:
    fontFamily: "Martian Mono, ui-monospace, SFMono-Regular, Menlo, Consolas, monospace"
    fontSize: "0.8125rem"
    fontWeight: 400
    letterSpacing: "0"
    fontFeature: "tnum"
    fontVariation: "wdth 87.5"
  data-figure:
    fontFamily: "Martian Mono, ui-monospace, SFMono-Regular, Menlo, Consolas, monospace"
    fontSize: "1.2rem"
    fontWeight: 400
    lineHeight: 1.2
    fontFeature: "tnum"
    fontVariation: "wdth 87.5"
rounded:
  none: "0"
  control: "2px"
spacing:
  xs: "8px"
  sm: "12px"
  md: "16px"
  lg: "24px"
  gutter: "clamp(24px, 4vw, 64px)"
  part: "clamp(88px, 11vw, 136px)"
  axis: "13rem"
  sheet: "1180px"
components:
  field:
    backgroundColor: "{colors.paper}"
    textColor: "{colors.ink}"
    typography: "{typography.field-value}"
    rounded: "{rounded.none}"
    padding: "14px 16px 18px"
  field-hover:
    backgroundColor: "{colors.ink}"
    textColor: "{colors.paper}"
  stamp:
    backgroundColor: "{colors.ink}"
    textColor: "{colors.paper}"
    rounded: "{rounded.none}"
    padding: "1px 5px 2px"
  stamp-inverted:
    backgroundColor: "{colors.paper}"
    textColor: "{colors.ink}"
  button-copy:
    backgroundColor: "transparent"
    textColor: "{colors.ink}"
    rounded: "{rounded.control}"
    padding: "6px 9px"
  button-copy-hover:
    backgroundColor: "{colors.blue}"
    textColor: "{colors.paper}"
  link-action:
    textColor: "{colors.blue}"
  nav-link:
    textColor: "{colors.ink-2}"
    padding: "15px 0 13px"
  nav-link-active:
    textColor: "{colors.ink}"
  priority-code:
    textColor: "{colors.red}"
    typography: "{typography.data}"
---

# Design System: Jack Barry

## Overview

**Creative North Star: "The Incident Record"**

The whole site is one filed record: a reference number and a live "Viewed" stamp on the form title line, a ruled field grid under the name, then parts ruled off by a black line, each with its label column on the left and the record body on the right. Nothing is a card and nothing floats. Structure comes from 1px rules on grey-white form stock, and emphasis comes from weight and one-bit inversion (ink ground, paper type), never from tint, radius or shadow.

Three voices share the page, each with one job: a firm grotesk for labels, headings and field values; a serif for reading; a narrow mono only for data such as refs, dates, figures and priority codes. Colour follows one law: black ink does everything, ballpoint blue marks what can be acted on, and red appears only on a priority code. Dark mode is a carbon copy of the same form, not a new palette.

Density varies on purpose. The header grid is tight and tabular, the summary is a quiet spread of large serif, the work notes are dense ruled lists, and the capabilities part is a ruled table. Motion is kept to evidence: the rules draw in once on load, rows invert under the pointer, and the only thing that keeps moving is the UK clock on the Viewed stamp.

**Key Characteristics:**
- Ruled form stock: 1px rules for fields, a 2px ink rule to open a form block, a 1px ink rule to open a part.
- A 13rem label column is the dominant axis on wide screens.
- State is shown by weight and inversion, never by pills, tints or badges.
- Blue means action, red means priority code; nothing else takes colour.
- Square corners everywhere except the 2px control.
- One continuous motion: the live Viewed timestamp.

## Colors

Grey-white form stock, typed black ink, pencil-grey rules, with two pens used under strict law.

### Primary
- **Ballpoint Blue** (`blue`; dark `carbon-blue`): links, the copy button's hover fill, focus outlines, text selection and caret. It marks what the reader can act on and nothing else.

### Secondary
- **Priority Red** (`red`; dark `carbon-red`): priority codes (P1, P2, P3) set in mono inside work notes. Never a heading, border, state or warning colour.

### Neutral
- **Form Stock** (`paper`; dark `carbon-paper`): the page ground, the sticky bar ground, and the type colour of any inverted row or stamp.
- **Typed Ink** (`ink`; dark `carbon-ink`): all primary text, the 2px form-opening rule, the 1px part-opening rule, the active nav underline, and the ground of every inverted state.
- **Faded Ink** (`ink-2`; dark `carbon-ink-2`): labels, secondary prose, nav links at rest, the form title line and footer.
- **Ruled Line** (`rule`; dark `carbon-rule`): field borders, meta grid top and bottom rules, table row rules, the bar's bottom rule.
- **Faint Rule** (`rule-soft`; dark `carbon-rule-soft`): separators between work-note lines, the lightest structure on the page.

Dark mode follows `prefers-color-scheme` and can be forced with `data-theme="dark"` or `data-theme="light"` on the root; every role swaps to its carbon counterpart and no other rule changes.

### Named Rules
**The One Law Rule.** Blue is only for actions (links, button hover, focus, selection). Red is only for priority codes. If an element is neither, it is ink, faded ink or rule.

**The Carbon Copy Rule.** Dark mode inverts the stock and lightens the two pens; it adds no new hues, tints or surfaces.

## Typography

**Display Font:** Schibsted Grotesk (with ui-sans-serif, system-ui, Helvetica Neue, Arial)
**Body Font:** Source Serif 4 with optical sizing (with Georgia, Times New Roman)
**Label/Mono Font:** Martian Mono at 87.5% width with tabular figures (with ui-monospace, SFMono-Regular, Menlo, Consolas)

**Character:** A form's printed grotesk labels, a typed serif narrative, and a narrow machine mono for anything a system would have logged.

### Hierarchy
- **Display** (700, clamp 2.5rem to 3.6rem, line-height 1, tracking -0.035em): the name only, once per page. It is a form heading, not a hero.
- **Headline** (600, 1.375rem, 1.2): part names in the label column (Summary, Work notes, Next action).
- **Title** (650, 1.3rem, 1.2): record titles (role, degree, project).
- **Lead** (serif 400, clamp 1.4rem to 1.95rem, 1.35, max 32ch): the opening statement of a spread. The same voice at clamp 1.5rem to 2.2rem, max 26ch, closes the page; the one-line description under the name sits at clamp 1.15rem to 1.4rem, max 44ch.
- **Body** (serif 400, 17px, 1.6): reading text; work notes are held to 70ch, client lines to 68ch.
- **Field value** (sans 500, 1.05rem, 1.3): what a field holds when it is words; meta values drop to 0.925rem.
- **Label** (sans 600, 0.72rem, 0.06em tracking, uppercase, faded ink): field and meta labels (`dt`), and the "In progress" qualifier in the capabilities table.
- **Data** (mono 400, 0.8125rem, 87.5% width, tabular): refs, periods, record counts, the form title line and footer. **Data figure** (mono 400, 1.2rem; 1.05rem under 560px) for the headline figures in the field grid.

### Named Rules
**The Three Voices Rule.** Grotesk labels and names things, serif is read, mono is data. Mono never sets a sentence of prose and serif never sets a label.

**The Filed Name Rule.** The name is the largest type on the page and stays near 3.5rem; no display size exceeds it.

## Layout

A single sheet, max 1180px, with page padding of clamp(16px, 4vw, 48px). A sticky 52px top bar carries the name and plain nav, ruled off below.

The record header stacks: form title line (ref left, Viewed stamp right, ruled beneath), the name, the one-line description, a four-column ruled field grid (two rows of four), then the action links. Each part below is a two-column grid: a 13rem label column holding the headline and any data note, and a body column, separated by a clamp(24px, 4vw, 64px) gutter. Parts sit clamp(88px, 11vw, 136px) apart. On wide screens the label column header is sticky at 72px from the top.

Records use a meta grid with fixed tracks (4rem, 10.5rem, 18rem, 7.5rem, auto), gap 28px by 12px, ruled top and bottom, so Ref, Period, Organisation, Location and State line up across every record like a box archive. Records inside a part are spaced clamp(56px, 7vw, 80px).

Spacing is small and rhythmic: 8, 12, 16 and 24px inside components, 14/18px vertical padding inside fields and rows.

**Responsive.** At 900px and below the label column collapses above its body, the field grid becomes two columns with the State and Contact fields spanning full width, the summary spread goes to one column, and meta becomes three equal columns. At 560px and below the bar wraps (name on top, nav below, the first nav item hidden), part scroll offset becomes 96px, the contact grid goes to one column, meta becomes two columns, and the capabilities table unstacks into label-over-text rows.

**Print.** The bar and buttons are removed, the page prints black on white at 11pt, link URLs print after external links, and stamps become a 1px black outline instead of a solid fill.

### Named Rules
**The Label Axis Rule.** Every part hangs from the same 13rem label column; nothing breaks the axis on wide screens.

**The One Grid Rule.** Every record uses the same meta tracks and the same label set order, whatever it records.

## Elevation & Depth

Flat. There are no shadows, gradients, glows or blurs anywhere. Depth is conveyed by rule weight (1px rule, 1px ink, 2px ink) and by inversion: a hovered row or a state stamp swaps to an ink ground with paper type. The sticky bar separates itself with its paper ground and a bottom rule only.

### Named Rules
**The Ruled Not Raised Rule.** Hierarchy is drawn with rules and inversion, never lifted with shadow or tone.

## Shapes

Square. Every field, row, stamp, table and part is a hard-cornered region defined by its rules (0 radius). The single exception is the copy control at 2px, just enough to read as a pressable key. Link arrows are a 10px inline stroke SVG (1.4 stroke) drawn in the link's colour.

## Components

### Buttons
Small, typed, and quiet until touched.
- **Shape:** near-square (2px).
- **Default:** transparent with a 1px current-colour border, grotesk 600 at 0.75rem, uppercase, 0.04em tracking, 6px by 9px padding. Inherits ink, so it stays legible inside an inverted field.
- **Hover:** fills Ballpoint Blue with paper type (0.12s). **Focus:** 2px blue outline, 3px offset.
- **Feedback:** the label changes to "Copied" for 1.6s and a polite live region announces it; if the clipboard is refused, the address is selected instead.

### Links
- **Style:** Ballpoint Blue, 1px underline at 0.22em offset, thickening to 2px on hover (0.15s). External links carry the 10px arrow. Action links sit in a row with 12px by 28px gaps.

### Navigation
- **Style:** grotesk 500 at 0.875rem in faded ink, no underline. Hover goes to ink. The section in view is marked `aria-current` with ink type and a 2px ink bottom border aligned to the bar's rule. Under 560px the links drop to 0.8125rem and wrap.

### Field (signature)
The unit of the record. A `dt` label over a value, in a cell ruled on its sides and bottom, 14px 16px 18px padding. The first cell of each row has no left padding so text hangs on the rule. On hover the whole cell inverts (ink ground, paper type and label) in 0.12s and gains 12px of left breathing room. The same inversion applies to capabilities table rows.

### State Stamp
- **Style:** the state word in bold on a solid ink block, 1px 5px 2px padding, square. Inside a hovered field it inverts back to paper on ink.
- **Use:** only for the open or in-progress state. Closed and completed states are plain field values at normal weight.

### Priority Code
Mono at 0.8em, 500 weight, 87.5% width, in Priority Red. Inline in prose, no background or border.

### Motion
- **Rule draw:** on load the field grid's 2px ink rule and the form line's 1px rule scale in from the left over 0.9s on cubic-bezier(0.16, 1, 0.3, 1), the second delayed 0.12s. Once only.
- **Live stamp:** the Viewed time ticks every second in Europe/London time (en-GB, 24-hour, with zone). It is the page's only continuous motion.
- **Reduced motion:** all animation and transition is removed and smooth scrolling is turned off.

## Do's and Don'ts

### Do:
- **Do** draw structure with 1px Ruled Line borders and open a block with a 2px ink rule (a part with a 1px ink rule).
- **Do** show state by weight and inversion: an ink stamp for open states, plain text for closed.
- **Do** put every record's facts in the fixed meta grid (Ref, Period, Organisation, Location, State) before its notes.
- **Do** set refs, dates, counts, figures and priority codes in Martian Mono at 87.5% width with tabular numerals.
- **Do** invert whole rows on hover (ink ground, paper type) as the one hover grammar for data regions.
- **Do** keep every colour change inside the carbon-copy token swap for dark mode.

### Don't:
- **Don't** use blue for anything that is not an action, or red for anything that is not a priority code.
- **Don't** use pills, rounded badges, tinted chips or coloured state dots; state is a square stamp or plain text.
- **Don't** add shadows, gradients, glows or card containers; the record is ruled, not raised.
- **Don't** set the name or any heading larger than the ~3.6rem display cap, or build a name hero or stats strip.
- **Don't** add continuous or looping motion beyond the live Viewed stamp.
- **Don't** use green-on-black terminals, fake command prompts, Matrix code or hood and skull imagery.
