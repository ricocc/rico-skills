# Radio Static Style

Audio Culture, TV Static, Retro Media, Independent Spirit

---

## Design Philosophy

### Brand Philosophy

**"The Sound Alternative"**

Radio Static design philosophy creates a retro media style for community radio and audio media. Through TV static effects and black-white tones, it conveys independent, alternative, authentic sound culture qualities.

### Design Philosophy

1. **Media Retro - Nostalgic Texture**
   - TV static effects
   - Analog signal era aesthetics
   - Traditional media meets modern design

2. **Audio First - Sound Culture**
   - Emphasizes audio content
   - Player in core position
   - Programs and music first

3. **Black-White Contrast - Strong Visual**
   - Black dominant
   - High contrast design
   - Strong visual impact

4. **Independent Spirit - Alternative Culture**
   - Anti-mainstream aesthetics
   - Authentic and unmodified
   - Community culture qualities

### Core Keywords

- Analog
- Independent
- Audio
- Community
- Alternative

---

## Overview

Radio Static style is designed for community radio, audio media, and music platforms. Black dominant, TV static effects, suitable for audio culture products that need to convey independence and authenticity.

---

## Color System

### Brand Color

```css
/* Radio Static Black-White - Brand Primary Color */
--color-primary: #000000;
--color-primary-hover: #1A1A1A;
--color-primary-light: #404040;
--color-primary-lighter: #F5F5F5;
```

#### Usage Guidelines

**When to Use:**

- Main background
- Headings and important text
- Player controls
- Navigation bar
- Brand identity

**Avoid Using:**

- Overusing white (loses black dominance)
- Colored decorative elements
- Non-critical operations

**Usage Principle:** Black occupies about 60-70% of page area

**Why Black and White?**
- Media retro: Black-white represents the analog signal era
- Independent spirit: Anti-colorful mainstream
- Visual impact: High contrast design
- Audio focus: Lets sound content be the star

### Background Colors

```css
/* Black dominant */
--color-bg: #000000;
--color-bg-secondary: #0A0A0A;
--color-bg-tertiary: #141414;
--color-bg-elevated: #1A1A1A;

/* Light mode (optional) */
--color-bg-light: #FFFFFF;
--color-bg-secondary-light: #F5F5F5;
```

### Text Colors

```css
/* Black background mode */
--color-text: #FFFFFF;
--color-text-secondary: #B0B0B0;
--color-text-tertiary: #707070;
--color-text-disabled: #404040;

/* White background mode */
--color-text-light: #000000;
--color-text-secondary-light: #404040;
--color-text-tertiary-light: #707070;
```

### Border Colors

```css
/* Black background mode */
--color-border: #2A2A2A;
--color-border-light: #1A1A1A;
--color-border-focus: #FFFFFF;

/* White background mode */
--color-border-light-mode: #E0E0E0;
--color-border-subtle-light: #F0F0F0;
```

### Accent Colors

```css
/* Radio Static Minimal Accents */
--color-accent-white: #FFFFFF;  /* White - Primary accent */
--color-accent-gray: #B0B0B0;    /* Gray - Secondary */
--color-accent-red: #FF0000;     /* Red - Recording */
--color-accent-green: #00FF00;   /* Green - Playing */
```

#### Functional Color Guidelines

- Primary accent: White #FFFFFF (on black background)
- Secondary: Gray #B0B0B0
- Recording: Red #FF0000
- Playing: Green #00FF00

**Restrained Use of Color:** Maintain black-white dominant, colors only for status indicators

---

## Interaction Philosophy

### Animation Principles

**Retro, Textured, Not Overdone**

Audio media needs smooth playback experience, animations should have retro texture but not be excessive.

#### State Feedback

- Focus: White border + glow
- Hover: Slight background change (#1A1A1A) + text inversion
- Click: Immediate response, slight scale (scale 0.98)

#### Transition Duration

- Fast: 100ms (button hover)
- Normal: 200ms (panel expand)
- Slow: 300ms (page transition)

**Why This Design?**
- Fast response improves interaction experience
- Maintains retro texture
- Doesn't affect audio playback

#### Signature Animations

- TV static effect (page transitions)
- Audio wave animation (playing)
- Tape reel effect (fast-forward/rewind)

### Feedback Mechanisms

**Instant, Obvious, Textured**

- Button click: Immediate background color change
- Playback control: Immediate response
- Operation success: White flash
- Operation failure: Red flash
- Loading state: Retro spinner or audio wave animation

---

## Layout Principles

### Spacing Strategy

**8px Grid System**

- All spacing is multiples of 8
- Ensures consistent visual rhythm
- Suitable for audio media standards

**Common Spacing:**

- Small spacing: 8px, 16px (related elements)
- Medium spacing: 24px, 32px (inside components)
- Large spacing: 48px, 64px (between modules)

### Black Dominant

**Visual Impact First**

Audio media needs strong visual impact:

- Main background: Black (#000000)
- Secondary background: Dark gray (#0A0A0A)
- Text: White (#FFFFFF)
- Maintain high contrast

**Why This Design?**
- Strong visual impact
- Matches retro media aesthetics
- Highlights audio content
- Independent alternative feel

### Content Max Width

- Player area: Unlimited (full width)
- Content area: 1200px
- Sidebar: 320px
- Mobile: 100% (full width)

---

## Component Design Decisions

### Player

#### Why Fixed Bottom?

- Always accessible
- Doesn't obstruct content
- Matches audio app conventions

#### Why Black-White Design?

- Maintains retro texture
- Doesn't distract from content
- Visual unity

#### Why Large Play Button?

- Easy to click
- Visual focus
- Clear action

### Show List

#### Why Timeline Design?

- Clearly shows program times
- Easy browsing and scheduling
- Matches radio use case

#### Why Highlight Current Playing?

- Clear status feedback
- Quick positioning
- Visual hierarchy

### TV Static Effect

#### Why Use Static?

- Retro media texture
- Unique visual identity
- Conveys analog signal era

#### Why Moderate Use?

- Doesn't affect readability
- Maintains restraint
- Avoids being too flashy

### Frequency Tuner Effect

#### Why Use Tuner Design?

- Retro radio element
- Enhances immersion
- Interactive playfulness

#### Why Visual Not Functional?

- Pure visual decoration
- Doesn't add complexity
- Maintains design sense

---

## Application Scenarios

### Scenario 1: Community Radio

**Core Applications:**

- Black dominant design
- TV static effects
- Program schedule
- Live player

**Adjustments:**

- Maintain black-white dominant
- Reinforce program information
- Optimize playback experience

### Scenario 2: Music Podcast

**Core Applications:**

- Playlist
- Episode titles and descriptions
- Playback controls
- Share functionality

**Adjustments:**

- Add album artwork
- Reinforce playlist
- Optimize mobile experience

### Scenario 3: Audio Blog

**Core Applications:**

- Episode archive
- Categories and tags
- Search function
- Subscribe function

**Adjustments:**

- Add text content
- Optimize archive browsing
- Reinforce subscribe function

### Scenario 4: Music Sharing Platform

**Core Applications:**

- User uploads
- Music playback
- Comments and interaction
- Social features

**Adjustments:**

- Add user elements
- Reinforce social features
- Optimize discovery mechanism

### Scenario 5: Sound Art Project

**Core Applications:**

- Immersive experience
- Sound visualization
- Art display
- Interactive design

**Adjustments:**

- Add experimental elements
- Reinforce sound visualization
- Optimize immersive experience

---

## Common Mistakes

### Common Errors

#### Error 1: Overusing Color

- Wrong: Lots of colored elements
- Correct: Maintain black-white dominant
- Reason: Loses retro texture, loses independent spirit

#### Error 2: Excessive Static Effects

- Wrong: Static effects everywhere
- Correct: Moderate use, serving design goals
- Reason: Affects readability, appears flashy

#### Error 3: Insufficient Contrast

- Wrong: Too much gray text, low contrast
- Correct: Maintain high contrast (white text)
- Reason: Affects readability, loses visual impact

#### Error 4: Animations Too Slow

- Wrong: 500ms, 800ms slow transitions
- Correct: 100-200ms fast response
- Reason: Affects interaction experience

#### Error 5: Border Radius Too Large

- Wrong: 12px, 16px large radius
- Correct: 0-4px small radius or square corners
- Reason: Loses retro texture

#### Error 6: Shadows Too Heavy

- Wrong: Heavy shadows, multiple shadows
- Correct: Subtle shadows or no shadows
- Reason: Appears too modern, loses retro feel

### Negative Checklist

- Don't overuse color, maintain black-white dominant
- Don't overuse static effects, use moderately
- Don't reduce contrast, maintain high contrast
- Don't use large radius (> 4px), use small radius (0-4px)
- Don't use heavy shadows, use subtle shadows or no shadows
- Don't use slow animations (> 300ms), use fast animations (100-200ms)
- Don't ignore audio playback functionality, optimize playback experience

---

## Typography Scale

```css
--font-size-xs: 12px;
--font-size-sm: 14px;
--font-size-base: 16px;
--font-size-md: 18px;
--font-size-lg: 20px;
--font-size-xl: 24px;
--font-size-2xl: 32px;
--font-size-3xl: 48px;
```

### Font Weights

```css
--font-weight-normal: 400;
--font-weight-medium: 500;
--font-weight-semibold: 600;
--font-weight-bold: 700;
--font-weight-black: 900;
```

### Font Family

```css
/* Retro media fonts */
--font-family: 'Inter', 'Helvetica Neue', Arial, sans-serif;
--font-family-display: 'Arial Black', 'Impact', sans-serif;
--font-family-mono: 'Courier New', 'Fira Code', monospace;
```

---

## Spacing System

```css
--space-1: 8px;
--space-2: 16px;
--space-3: 24px;
--space-4: 32px;
--space-5: 48px;
--space-6: 64px;
--space-8: 80px;
```

---

## Border Radius System

```css
--radius-none: 0;
--radius-sm: 2px;
--radius-md: 4px;
--radius-lg: 8px;
```

---

## Shadows

```css
--shadow-sm: 0 1px 2px rgba(0, 0, 0, 0.5);
--shadow-md: 0 4px 8px rgba(0, 0, 0, 0.6);
--shadow-lg: 0 8px 16px rgba(0, 0, 0, 0.7);
--shadow-glow: 0 0 20px rgba(255, 255, 255, 0.3);
```

---

## Component Specifications

### Buttons

```css
.btn {
  height: 44px;
  padding: 0 20px;
  font-size: 14px;
  font-weight: 600;
  border-radius: 2px;
  transition: all 0.1s ease-out;
  text-transform: uppercase;
  letter-spacing: 1px;
}

.btn-primary {
  background: white;
  color: black;
  border: 2px solid white;
}

.btn-primary:hover {
  background: transparent;
  color: white;
}

.btn-secondary {
  background: transparent;
  color: white;
  border: 2px solid white;
}

.btn-secondary:hover {
  background: white;
  color: black;
}

.btn-ghost {
  background: transparent;
  color: white;
  border: none;
  text-decoration: underline;
}
```

### Player

```css
.player {
  position: fixed;
  bottom: 0;
  left: 0;
  right: 0;
  background: black;
  border-top: 2px solid white;
  padding: 16px 24px;
  z-index: 1000;
}

.player-controls {
  display: flex;
  align-items: center;
  gap: 16px;
}

.player-btn {
  width: 48px;
  height: 48px;
  border-radius: 50%;
  background: white;
  color: black;
  border: none;
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
  transition: all 0.1s ease-out;
}

.player-btn:hover {
  transform: scale(1.1);
  box-shadow: 0 0 20px rgba(255, 255, 255, 0.5);
}

.player-info {
  flex: 1;
  color: white;
}

.player-title {
  font-size: 16px;
  font-weight: 600;
  margin-bottom: 4px;
}

.player-artist {
  font-size: 14px;
  color: #B0B0B0;
}
```

### Show Card

```css
.show-card {
  background: #0A0A0A;
  border: 2px solid white;
  border-radius: 4px;
  padding: 24px;
  transition: all 0.2s ease-out;
}

.show-card:hover {
  border-color: #B0B0B0;
  box-shadow: 0 0 20px rgba(255, 255, 255, 0.3);
}

.show-time {
  font-family: 'Courier New', monospace;
  font-size: 14px;
  color: #B0B0B0;
  margin-bottom: 12px;
}

.show-title {
  font-size: 20px;
  font-weight: 700;
  color: white;
  margin-bottom: 8px;
}

.show-host {
  font-size: 14px;
  color: #707070;
}
```

### TV Static Effect

```css
.tv-static {
  position: relative;
  overflow: hidden;
}

.tv-static::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-image: url('data:image/svg+xml;utf8,%3Csvg viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg"%3E%3Cfilter id="noise"%3E%3CfeTurbulence type="fractalNoise" baseFrequency="0.9" numOctaves="3" stitchTiles="stitch"/%3E%3C/filter%3E%3Crect width="100%25" height="100%25" filter="url(%23noise)" opacity="0.15"/%3E%3C/svg%3E');
  pointer-events: none;
  animation: static 0.5s steps(5) infinite;
}

@keyframes static {
  0% { transform: translate(0, 0); }
  20% { transform: translate(-2px, 2px); }
  40% { transform: translate(2px, -2px); }
  60% { transform: translate(-2px, -2px); }
  80% { transform: translate(2px, 2px); }
  100% { transform: translate(0, 0); }
}
```

### Audio Wave Animation

```css
.audio-wave {
  display: flex;
  align-items: center;
  gap: 2px;
  height: 20px;
}

.audio-wave-bar {
  width: 2px;
  background: white;
  animation: wave 1s ease-in-out infinite;
}

.audio-wave-bar:nth-child(1) { animation-delay: 0s; height: 8px; }
.audio-wave-bar:nth-child(2) { animation-delay: 0.1s; height: 12px; }
.audio-wave-bar:nth-child(3) { animation-delay: 0.2s; height: 16px; }
.audio-wave-bar:nth-child(4) { animation-delay: 0.3s; height: 20px; }
.audio-wave-bar:nth-child(5) { animation-delay: 0.4s; height: 16px; }
.audio-wave-bar:nth-child(6) { animation-delay: 0.5s; height: 12px; }
.audio-wave-bar:nth-child(7) { animation-delay: 0.6s; height: 8px; }

@keyframes wave {
  0%, 100% { transform: scaleY(1); }
  50% { transform: scaleY(0.5); }
}
```

---

## Animations

```css
--duration-fast: 100ms;
--duration-normal: 200ms;
--duration-slow: 300ms;

--ease-out: cubic-bezier(0.16, 1, 0.3, 1);
```

---

## Best For

- Community radio
- Music podcasts
- Audio blogs
- Music sharing platforms
- Sound art projects
- Independent music platforms
- Radio station websites
- Audio experimental projects
