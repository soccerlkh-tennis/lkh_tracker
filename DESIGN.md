# Header 1
## Header 2
### Header 3

version: alpha name: Toss-inspired Product UI description: >- Clean, text-first product UI derived from Toss's design language and the Apps in Toss developer guidelines. Primary goal: avoid the patterns that make a design read as AI-generated — default blue, decorative gradients, uniform 3-column grids, and formulaic section structures.
colors:
TODO: replace primary with the brand accent BEFORE designing.
Never fall back to blue — it is the AI default. Ask the user if unknown.
primary: "#191F28" on-primary: "#FFFFFF" light: background: "#FFFFFF"      # 6 — base surface: "#F2F4F6"         # 3 — sub-background (also used instead of borders) on-surface: "#191F28" on-surface-muted: "#4E5968" on-surface-subtle: "#8B95A1" dark: # Not pure black — tint toward the brand accent once primary is set. background: "#17171C" surface: "#202027" on-surface: "#F2F4F6" on-surface-muted: "#B0B8C1" on-surface-subtle: "#7E8794" error: "#E5484D"
typography: headline-display: fontFamily: Pretendard fontSize: 32px fontWeight: 700 lineHeight: 1.3 letterSpacing: -0.02em headline-lg: fontFamily: Pretendard fontSize: 26px fontWeight: 700 lineHeight: 1.35 letterSpacing: -0.02em headline-md: fontFamily: Pretendard fontSize: 22px fontWeight: 700 lineHeight: 1.4 body-lg: fontFamily: Pretendard fontSize: 17px fontWeight: 400 lineHeight: 1.6 body-md: fontFamily: Pretendard fontSize: 15px fontWeight: 400 lineHeight: 1.6 body-sm: fontFamily: Pretendard fontSize: 14px fontWeight: 400 lineHeight: 1.55 label-md: fontFamily: Pretendard fontSize: 13px fontWeight: 500 lineHeight: 1.5 label-sm: fontFamily: Pretendard fontSize: 12px fontWeight: 400 lineHeight: 1.5
rounded: none: 0px sm: 8px md: 12px lg: 16px full: 9999px
spacing: xs: 4px sm: 8px md: 16px lg: 24px xl: 40px
components: button-primary: backgroundColor: "{colors.primary}" textColor: "{colors.on-primary}" typography: "{typography.body-md}" rounded: "{rounded.md}" height: 52px padding: 16px button-secondary: backgroundColor: "{colors.light.surface}" textColor: "{colors.light.on-surface}" typography: "{typography.body-md}" rounded: "{rounded.md}" height: 52px padding: 16px card: backgroundColor: "{colors.light.surface}" rounded: "{rounded.lg}" padding: 20px list-item: typography: "{typography.body-md}" height: 56px padding: 16px icon: size: 24px icon-lg: size: 40px
DESIGN.md
Overview
A calm, text-first product UI in the spirit of Toss: black/white base tones, one brand accent, generous but purposeful whitespace. Every visual element must earn its place by helping users understand the screen — context first, decoration never.
Before starting any design, confirm the brand accent color with the user and update colors.primary. The token values above are defaults; the rules below are the point.
Colors
6:3:1 ratio — background : surface : primary (accent). The accent is the 1, not the default fill.
No default blue. Blue is what AI tools reach for. Use the brand's color.
Dark mode is never pure black — mix a small amount of the brand accent into dark.background and dark.surface.
Survive both modes. Graphics and logos must read clearly in light and dark; prefer mid-tone colors.
Gradients are rare. Only where emphasis is genuinely needed. Decorative gradients read as noise.
Typography
Families: Pretendard first; Asta, Noto Sans, or Spoqa Han Sans as alternatives. Never system fonts.
Body copy lives in 14–17px (body-sm → body-lg), on a 13px baseline (label-md).
12px (label-sm) is reserved for low-priority info only — legal disclaimers, footnotes.
Layout
Vary the rhythm across sections. Alternate image position (left/right), drop a card grid between plain-text sections.
Match density to content type.
Browse/search screens (e.g. job listings): minimal filter + list UI.
Editorial/content hubs (e.g. blog): hero image + curated card grid.
Footer is the fixed anchor. Keep it structurally identical across all subpages.
One logical resolution. Design for a portrait baseline of ~360×640 to 420×740 and scale. Handle notches and the Dynamic Island with Safe Area.
Assets: 1x + 2x only. Add 3x selectively when graphic quality is critical.
Never compute UI from physical pixels, maintain per-device layouts, or multiply asset resolution groups. These cause broken UI, letterboxing, and maintenance cost.
Elevation & Depth
Depth comes from tone, not lines: separate layers with surface on background.
Cards are fully borderless — no border, and no partial color accents such as a colored top edge.
Shapes
Corner radius stays moderate (rounded.md–rounded.lg). Avoid pill-everything, overly soft UI.
Logos inside a host platform are square, with no rounded corners (see the appendix).
Motion & Micro-interaction
Motion must reflect real state. No loading animations when nothing is loading.
No meaningless particles or flourishes that add complexity without meaning.
Voice & Content Strategy
Korean copy follows Toss's official voice & tone guidelines.
Principle
Rule
Example
해요체
Every string uses 해요체 — no exceptions by context
확인하세요 → 확인해요
Active voice
Prefer active; passive only in defined exceptions
됐어요 → 했어요, drop '~었'
Positive framing
Reframe blockers as conditions
"안 돼요/없어요" → "~하면 할 수 있어요"
Casual honorifics
Drop excessive honorifics
계시다 → 있다, 께 → 에게, ~시겠어요? ✕
No noun stacking
Unpack Sino-Korean compounds into verb phrases
{명사}+{명사} → {명사}가 {명사}해서
Dialog buttons
Left button is always 닫기, never 취소 (취소 implies the task is canceled)
—
Benefit eligibility
When the service works but one benefit doesn't apply, frame it positively — users skim and assume the whole product is blocked
—

Headlines
Two layers: an emotional headline first ("쉽게", "간편하게", "무료로", "걱정 없이"), then a concrete, functional subline.
Vary sentence length and tone between sections so the copy itself creates rhythm.
CTAs
The label alone predicts the next action.
Don't repeat the value proposition stated above the button, and don't stack exaggerated helper text on top of it.
Components
Card
Use cards only to group related information. Standalone info that doesn't need grouping goes into a plain grid.
Pair a full card (thumbnail + title + 1–2 line description + optional tag/CTA) with a compact list version elsewhere on the page, so users can both scan and read in depth.
Buttons & Dialogs
button-primary carries the single action the screen exists for; everything else is button-secondary.
Every prompt has a real decline path (see Do's and Don'ts).
Graphics & Icons
One hero graphic per screen; demote the rest to small supporting icons.
Size follows information density: simple graphics small, detailed graphics large.
Icons stay within 24–40px (icon → icon-lg), one at a time — no side-by-side icon/emoji pairs.
Graphics must be accurate to the situation: no exclamation icons for non-errors.
Style: clean, digital, high-resolution, bright and organized. No hand-drawn, overly lyrical, or cartoonish styles.
Graphics never push key content below the fold or outshine text and CTAs.
Do's and Don'ts
Do
Confirm the brand accent before starting.
Vary layout rhythm and copy rhythm section to section.
Keep one hero graphic and one primary action per screen.
Don't
Default to blue, decorative gradients, or emojis (unless the user explicitly asks for emojis).
Force everything into a uniform 3–4 column grid.
Repeat the "eyebrow → title → description → button → content" formula in every section. It pads whitespace and buries the key information.
Use negative or pleading emotional graphics (e.g. a crying character begging users to stay).
Dark patterns — hard rules. Violating any of these is a critical usability failure.
No entry interrupts. No full-screen or bottom-sheet ad (including push-permission prompts) the moment a user enters a screen.
No exit traps. Never intercept the back button with a retention bottom sheet.
Always provide an out. Every prompt has a real decline path.
No surprise ads mid-flow. Never inject a full-screen ad into an expected action path.
Predictable CTAs. Ambiguous labels create hesitation and hurt conversion.
Appendix: Host-Platform Branding
For mini-apps and embedded services living inside a larger product (from the Apps in Toss guide; generalize as needed):
Logo: square, no rounded corners, with an explicit background that works in both light and dark mode.
Brand name: prefer the local language (한글) over romanized names unless there's a specific reason.
Brand color: use the existing brand color. If none exists, extract the dominant color from the logo, and expect automatic contrast correction if it fails accessibility thresholds.
Navigation/tab bars: use the host platform's components so users never confuse the embedded service's chrome with the host app's (e.g. Toss's floating tab bar, 2–5 tabs).
