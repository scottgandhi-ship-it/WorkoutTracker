# UI/Visual Design Overhaul — Clean & Minimal

Full redesign of the 531 Workout Tracker with an iOS/Apple-inspired clean & minimal aesthetic. All changes are CSS-only or HTML-template-only — no logic changes.

## Design Direction
- **Palette**: Shift from harsh dark (#0f0f0f) to a softer dark background (#111113) with slightly warm grays. Subtle accent tinting. Reduce the rainbow of status colors to a more muted, cohesive set.
- **Typography**: Increase use of font weight variation. Larger section headers. More generous line-height. Tighter letter-spacing on headings. SF Pro / system font stack stays.
- **Spacing**: More generous padding throughout (cards, rows, sections). Consistent 20px card padding. Wider gaps between sections.
- **Cards**: Remove visible borders entirely. Use subtle elevation with very faint box-shadow instead. Larger border-radius (16px). Background just slightly lighter than page.
- **Buttons**: Softer corners (12px). Slightly less saturated accent color. Ghost/outline buttons get a subtle tinted background on hover. Active states use scale + opacity.
- **Inputs**: Taller (44px), bigger touch targets. Softer border. Focus ring uses a subtle glow rather than just border color.
- **Tab Bar**: Frosted-glass effect (backdrop-filter). Slightly taller. Larger icons. Remove hard border-top, use shadow instead.
- **Set Rows**: More padding. Checkbox buttons become rounded circles instead of squares. Completed state is softer green.
- **Animations**: Add smooth transitions for view switches, card interactions, and modal open/close. CSS only.

## Specific Changes

### 1. CSS Variables (Color System)
Replace the current variables with a refined palette:
- Softer dark background, warmer card surface
- Muted accent blue (less saturated)
- Refined semantic colors (success, warning, danger) — less neon
- Add `--text-secondary` and `--surface-elevated` tokens

### 2. App Shell & Tab Bar
- Header: remove border, use shadow. Larger title. Badge gets a pill shape with more padding.
- Tab bar: `backdrop-filter: blur(20px)` with semi-transparent background. Drop shadow on top. Taller touch targets (56px). Larger icons (26px).
- Main content: slightly larger side padding (20px).

### 3. Cards
- Remove `border` property.
- Add `box-shadow: 0 1px 3px rgba(0,0,0,0.3), 0 0 0 1px rgba(255,255,255,0.03)`.
- Increase padding to 20px. Increase border-radius to 16px. Increase gap between cards to 16px.

### 4. Workout View
- Week selector pills: taller (40px), bigger radius (12px), use soft tinted background for active state instead of solid color.
- Day selector: same treatment. Active state is accent-tinted background rather than solid fill.
- Set rows: more vertical padding (14px). Set number becomes a subtle circle. Weight text slightly larger. Check buttons become 40px circles.
- AMRAP input: keep the distinctive styling but soften the border color.
- Accessory section: cleaner layout with more spacing. Rest timer button more prominent.
- Log Workout button: full-width, taller (52px), subtle gradient or just solid with softer color.

### 5. History View
- History cards: add left color accent bar (4px) based on lift type.
- Date styling: lighter weight, use relative dates for recent ("Today", "Yesterday").
- Expand/collapse gets a subtle rotation animation on chevron.

### 6. Progress View
- Stat cards: larger numbers (32px). Add subtle gradient tinting per lift color.
- Chart: slightly rounded container. Softer grid lines.
- Projection table: more padding, alternating row backgrounds.

### 7. Settings View
- Setting rows: taller (48px). Inputs and selects get consistent 44px height.
- Destructive buttons (Reset) get more visual warning with danger background tint.
- Template selector cards: softer selection state.

### 8. Modals
- Add entrance animation (scale from 0.95 + fade in).
- Overlay is slightly more opaque. Blur the background.
- Modal padding increased to 28px.

### 9. Timer Banner
- Frosted glass effect matching tab bar.
- Larger timer display (32px). Pill-shaped buttons.

### 10. Micro-interactions
- All interactive elements get `transition: all 0.2s ease`.
- Buttons: active state `transform: scale(0.97)`.
- Cards: subtle hover/active brightness change.
- Tab switching: opacity fade transition.
