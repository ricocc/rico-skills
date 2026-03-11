# Spotify Style

Bold Colors, Gradients, Dynamic Feel, Youthful Energy

---

## Design Philosophy

### Brand Philosophy

**"Music for Everyone"**

Spotify's design philosophy conveys the passion and energy of music through bold dark backgrounds and vibrant green. Design emphasizes immersive experience, letting users focus on content while the interface recedes.

### Design Philosophy

1. **Dark Immersion - Content is King**
   - Deep black background (#121212)
   - Let album covers and images be the hero
   - Reduce eye strain

2. **Bold Green - Brand Identity**
   - High saturation green (#1DB954)
   - Extremely prominent on dark background
   - Youthful, energetic, trendy

3. **Gradient Aesthetics - Dynamic Feel**
   - Subtle gradient transitions
   - Hero section gradient backgrounds
   - Adds visual depth

4. **Circular Cards - Modern Feel**
   - No border-radius or minimal border-radius
   - Compact layout
   - Information density first

### Core Keywords

- Bold
- Immersive
- Vibrant
- Modern
- Dynamic

---

## Overview

Spotify style originates from the Spotify music platform—bold green brand color + dark background, full of youthful energy. Suitable for music, entertainment, and media products.

---

## Color System

### Brand Color

```css
/* Spotify Green - Brand Primary Color */
--color-primary: #1DB954;       /* Spotify Green */
--color-primary-hover: #1ED760;
--color-primary-dark: #169C46;
```

#### Usage Guidelines

**When to Use:**

- Primary buttons ("Play", "Follow")
- Progress bars
- Active states, selected states
- Links and interactive elements
- Brand identity

**Avoid Using:**

- Large area backgrounds (too harsh)
- Non-critical operations
- Decorative elements

**Usage Principle:** Restrained but prominent, about 5-8% of page area

**Why Such Vibrant Green?**
- Brand identity: Spotify's signature green
- Extremely prominent on dark background
- Conveys youth, energy, trendiness
- Strong contrast with dark background

### Background Colors

```css
/* Dark mode primary */
--color-bg: #121212;           /* Main background - Deep black */
--color-bg-elevated: #181818;  /* Card background */
--color-bg-hover: #282828;     /* Hover background */
--color-bg-highlight: #333333; /* Highlight background */

/* Light mode */
--color-bg-light: #FFFFFF;
--color-bg-secondary-light: #F8F8F8;
```

### Text Colors

```css
/* Dark mode */
--color-text: #FFFFFF;           /* Primary text */
--color-text-secondary: #B3B3B3; /* Secondary text */
--color-text-tertiary: #727272;  /* Auxiliary text */

/* Light mode */
--color-text-light: #121212;
--color-text-secondary-light: #535353;
```

### Border Colors

```css
--color-border: #282828;
--color-border-light: #D9D9D9;
```

### Accent Colors

```css
/* Spotify Signature Accents */
--color-accent: #1DB954;        /* Green accent */
--color-accent-purple: #AF2896; /* Purple - Podcasts */
--color-accent-blue: #509BF5;   /* Blue */
--color-accent-orange: #E8115B; /* Pink */
--color-accent-yellow: #F59B23; /* Yellow */
```

### Gradients

```css
/* Spotify Signature Gradients */
--gradient-green: linear-gradient(135deg, #1DB954 0%, #1ED760 100%);
--gradient-hero: linear-gradient(180deg, #1DB954 0%, #121212 100%);
--gradient-card: linear-gradient(180deg, #333333 0%, #121212 100%);
```

#### Gradient Usage Guidelines

**Subtle, Non-Intrusive:**

- Hero section: Green to black gradient
- Card backgrounds: Dark gray to black gradient
- Button hover: Green gradient
- Playlist headers: Gradient overlay

**Why Use Gradients?**
- Adds visual depth
- Creates immersive feel
- Modern aesthetics
- Subtle without stealing attention

---

## Interaction Philosophy

### Animation Principles

**Smooth, Responsive, Immersive**

#### Playback Feedback

- Click play: Button turns green
- Card hover: Slight lift (2px)
- Progress bar: Real-time updates

#### Interface Animations

- Page transitions: Fade in/out (200ms)
- Sidebar expand: Slide in (250ms)
- Modals: Scale + fade (150ms)

#### Transition Duration

- Fast: 100ms (button hover)
- Normal: 150ms (card interaction)
- Slow: 250ms (panel switching)

**Why So Smooth?**
- Immersive experience
- Doesn't interrupt music appreciation
- Modern feel
- Youthful energy

### Feedback Mechanisms

**Instant, Subtle**

- Button click: Immediately turns green
- Card hover: Background brightens (#282828 → #333333)
- Playback controls: Highlighted
- Loading state: Skeleton screen (dark gray)

---

## Layout Principles

### Spacing Strategy

**Compact but Breathing**

**Standard Spacing:**

- Minimum: 4px
- Small spacing: 8px, 12px
- Medium spacing: 16px, 24px
- Large spacing: 32px, 48px

**Why More Compact Than Notion?**
- Media content is primary
- Information density first
- Immersive experience

### Dark Immersion

**Deep Black as Primary:**

- Main background: #121212 (deep black)
- Card background: #181818 (slightly lighter)
- Hover background: #282828 (even lighter)

**Why Dark?**
- Immersive experience
- Makes album covers pop
- Reduces eye strain
- Matches music app conventions

### Border Radius System

**Minimal or No Border Radius**

- Buttons: 500px (nearly circular) or 4px
- Cards: No border-radius or 4px
- Images: No border-radius
- Inputs: 4px

**Why Such Small Border Radius?**
- Modern feel
- Information density first
- Distinguishes from "rounded friendly" styles
- Matches media app trends

### Content Max Width

- Main content: Full width (media stream)
- Sidebar: 280px
- List view: 1400px (centered)

---

## Component Design Decisions

### Buttons

#### Why Green Buttons?

- Brand identity
- Extremely prominent on dark background
- Youthful energy
- Classic player color

#### Why Circular Buttons (Play)?

- Play/Pause: Circular, 48px
- Other buttons: Pill shape, 32px
- Classic player design

### Cards/Album Covers

#### Why No Border Radius or Minimal?

- Modern feel
- Doesn't compete with content
- Information density first
- Matches media applications

#### Why Hover Lift?

- Provides interaction feedback
- Adds depth
- Doesn't interrupt browsing
- Subtle not abrupt

### Progress Bar

#### Why Green Gradient?

- Playback progress visualization
- Brand color reinforcement
- Instant feedback
- Immersive experience

**Design Features:**
- Green gradient
- 2px height
- Real-time updates

### Navigation

#### Why Sidebar + Bottom Playback Bar?

- Sidebar: 280px (navigation, lists)
- Bottom playback bar: 90px height (fixed)
- Classic music app layout

---

## Application Scenarios

### Scenario 1: Music Player

**Core Applications:**

- Deep black background (#121212)
- Green play button
- Fixed bottom playback bar
- Album cover stream

**Adjustments:**

- Emphasize immersion
- Large album cover images
- Lyrics display

### Scenario 2: Podcast App

**Core Applications:**

- Purple accent (#AF2896)
- Podcast covers
- Episode lists
- Playback progress

**Adjustments:**

- Use purple as secondary
- Fast forward/rewind
- Speed control

### Scenario 3: Video Streaming

**Core Applications:**

- Dark background
- Green play button
- Video thumbnails
- Gradient overlay

**Adjustments:**

- Video fullscreen mode
- Auto-play
- Picture-in-picture

### Scenario 4: Entertainment Content Platform

**Core Applications:**

- Immersive dark theme
- Colorful content categories
- Recommendation algorithm feed
- Personalized covers

**Adjustments:**

- Horizontal scrolling cards
- Hero banner
- Personalized recommendations

### Scenario 5: Mobile Music App

**Key Adjustments:**

- Bottom playback bar: Fixed
- Sidebar: Full screen drawer
- Gestures: Swipe to change tracks

**Keep Unchanged:**

- Dark background
- Green brand color
- Immersive experience

---

## Common Mistakes

### Common Errors

#### Error 1: Using Light Background

- Wrong: White or light gray background
- Correct: Deep black background (#121212)
- Reason: Loses immersion, doesn't feel like media app

#### Error 2: Using Other Colors

- Wrong: Blue, red primary buttons
- Correct: Spotify Green (#1DB954)
- Reason: Loses brand identity

#### Error 3: Large Border Radius

- Wrong: 12px, 16px border-radius
- Correct: No border-radius or 4px
- Reason: Loses modern feel, not media-oriented enough

#### Error 4: Excessive Whitespace

- Wrong: Lots of whitespace, like Notion
- Correct: Compact layout, high information density
- Reason: Wastes space, doesn't match media apps

#### Error 5: Missing Gradients

- Wrong: Solid color backgrounds
- Correct: Subtle gradients
- Reason: Loses visual depth and immersion

#### Error 6: Too Many Animations

- Wrong: Bounce, rotation, celebration animations
- Correct: Smooth, subtle, non-intrusive
- Reason: Interrupts immersive experience

### Negative Checklist

- Don't use light background, use deep black (#121212)
- Don't use other brand colors, use Spotify Green (#1DB954)
- Don't use large border-radius (> 4px), use none or minimal
- Don't overdo whitespace, maintain compact layout
- Don't remove gradients, use subtle gradients
- Don't use flashy animations, keep smooth and subtle
- Don't compete with content, let media be the hero

---

## Visual Design Specifications

### Color System

#### Brand Color

```css
/* Spotify Green - Brand Primary Color */
--color-primary: #1DB954;       /* Spotify Green */
--color-primary-hover: #1ED760;
--color-primary-dark: #169C46;
```

#### Accent Colors

```css
/* Spotify Signature Accents */
--color-accent: #1DB954;        /* Green accent */
--color-accent-purple: #AF2896; /* Purple - Podcasts */
--color-accent-blue: #509BF5;   /* Blue */
--color-accent-orange: #E8115B; /* Pink */
--color-accent-yellow: #F59B23; /* Yellow */
```

#### Gradients

```css
/* Spotify Signature Gradients */
--gradient-green: linear-gradient(135deg, #1DB954 0%, #1ED760 100%);
--gradient-hero: linear-gradient(180deg, #1DB954 0%, #121212 100%);
--gradient-card: linear-gradient(180deg, #333333 0%, #121212 100%);
```

#### Background Colors

```css
--font-size-xs: 10px;
--font-size-sm: 12px;
--font-size-base: 14px;
--font-size-md: 16px;
--font-size-lg: 18px;
--font-size-xl: 24px;
--font-size-2xl: 28px;
--font-size-3xl: 32px;
--font-size-4xl: 48px;
--font-size-5xl: 64px;
--font-size-6xl: 96px;  /* Hero large titles */
```

### Font Weights

```css
--font-weight-normal: 400;
--font-weight-medium: 500;
--font-weight-bold: 700;
--font-weight-black: 900;  /* Spotify often uses bold */
```

### Font Family

```css
--font-family: 'Circular', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
```

---

## Spacing System

```css
--space-1: 4px;
--space-2: 8px;
--space-3: 12px;
--space-4: 16px;
--space-5: 20px;
--space-6: 24px;
--space-8: 32px;
--space-10: 40px;
--space-12: 48px;
--space-16: 64px;
```

---

## Border Radius System

```css
--radius-sm: 4px;
--radius-md: 8px;
--radius-lg: 12px;
--radius-xl: 16px;
--radius-2xl: 24px;
--radius-full: 9999px;  /* Circular avatars */
```

---

## Component Specifications

### Buttons

```css
.btn-primary {
  background: #1DB954;
  color: #121212;
  height: 48px;
  padding: 0 32px;
  border-radius: 9999px;
  font-weight: 700;
  font-size: 14px;
  text-transform: uppercase;
  letter-spacing: 0.1em;
  transition: all 0.2s ease;
}

.btn-primary:hover {
  background: #1ED760;
  transform: scale(1.04);
}

.btn-secondary {
  background: transparent;
  color: #FFFFFF;
  height: 48px;
  padding: 0 32px;
  border: 1px solid #727272;
  border-radius: 9999px;
  font-weight: 700;
  font-size: 14px;
}

.btn-secondary:hover {
  border-color: #FFFFFF;
  transform: scale(1.04);
}

.btn-ghost {
  background: transparent;
  color: #B3B3B3;
  height: 32px;
  font-weight: 400;
}

.btn-ghost:hover {
  color: #FFFFFF;
}
```

### Cards

```css
.card {
  background: #181818;
  border-radius: 8px;
  padding: 16px;
  transition: background 0.3s ease;
}

.card:hover {
  background: #282828;
}

.card-image {
  border-radius: 8px;
  width: 100%;
  aspect-ratio: 1;
  object-fit: cover;
  box-shadow: 0 8px 24px rgba(0, 0, 0, 0.5);
}
```

### Inputs

```css
.input {
  background: #3E3E3E;
  border: none;
  border-radius: 4px;
  height: 40px;
  padding: 0 12px;
  font-size: 14px;
  color: #FFFFFF;
}

.input::placeholder {
  color: #B3B3B3;
}

.input:focus {
  outline: none;
  background: #4A4A4A;
}
```

### Player Controls

```css
.player-control {
  width: 32px;
  height: 32px;
  color: #B3B3B3;
  transition: color 0.2s ease, transform 0.2s ease;
}

.player-control:hover {
  color: #FFFFFF;
  transform: scale(1.06);
}

.player-control-play {
  width: 56px;
  height: 56px;
  background: #1DB954;
  border-radius: 50%;
  color: #121212;
}

.player-control-play:hover {
  background: #1ED760;
  transform: scale(1.06);
}
```

---

## Animations

```css
--duration-fast: 0.2s;
--duration-normal: 0.3s;
--duration-slow: 0.5s;

--ease-out: cubic-bezier(0.4, 0, 0.2, 1);
--ease-in-out: cubic-bezier(0.4, 0, 0.2, 1);
```

### Animation Characteristics

- **Hover Scale**: Cards, buttons slightly enlarge on hover (scale 1.04-1.06)
- **Gradient Transitions**: Background color gradient transitions
- **Pulse Animation**: Playing state pulse effect
- **Slide In**: Content slides in from below

---

## Best For

- Music/Entertainment products
- Media platforms
- Young user demographic products
- Dark mode first applications
- Products needing energetic feel
