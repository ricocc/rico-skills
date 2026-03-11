# Airbnb Style

Warm, Human, Trust, Belonging, Inclusive

---

## Design Philosophy

### Brand Philosophy

**"Belong Anywhere"**

Airbnb's design philosophy centers on "helping anyone belong anywhere." Design is not just about aesthetics—it's about conveying warmth, trust, and human connection.

### Design Philosophy

1. **Photo-First - Let Content Speak**
   - Brand color used sparingly, not exceeding 10% of page area
   - Generous whitespace, make property photos the hero
   - Minimize decorative elements, highlight authentic experiences

2. **Warmth - Warm Gray System**
   - Use Stone gray (#F7F7F7) instead of cool gray (#F5F5F5)
   - Convey human care and sense of belonging
   - Distinguish from the cold feel of tech products

3. **Rounded & Friendly - Approachable Design**
   - Larger border-radius 8-12px, convey openness and inclusivity
   - Gentle shadows, not harsh
   - Avoid sharp edges, create a safe atmosphere

4. **Trust - Clear & Precise**
   - Clear information hierarchy
   - Timely operation feedback
   - High visual consistency

### Core Keywords

- Warm
- Human
- Trust
- Belonging
- Inclusive

---

## Overview

Airbnb style originates from the Airbnb accommodation platform—warm coral red brand color (#FF5A5F) + large image storytelling, conveying human care and trust. Suitable for travel, accommodation, and community products.

---

## Color System

### Brand Color

```css
/* Airbnb Coral Red - Brand Primary Color */
--color-primary: #FF5A5F;       /* Rausch - Brand Red */
--color-primary-hover: #FF7E82;
--color-primary-dark: #E04C51;
--color-primary-light: #FF8A8F;
```

#### Usage Guidelines

**When to Use:**

- CTA buttons (Primary actions)
- Links and clickable elements
- Selected states, active states
- Brand identity
- Star ratings with yellow

**Avoid Using:**

- Large area backgrounds (feels oppressive)
- Decorative elements (use sparingly)
- Non-critical actions
- Text color (unless for emphasis)

**Usage Principle:** Not exceeding 10% of page area

**Why Use Sparingly?**
- Let property photos be the hero
- Avoid visual fatigue
- Maintain a premium feel
- Coral red has high saturation, large areas appear cheap

### Background Colors

```css
/* Light mode primary */
--color-bg: #FFFFFF;           /* Main background */
--color-bg-secondary: #F7F7F7; /* Secondary background */
--color-bg-tertiary: #EBEBEB;  /* Auxiliary background */
--color-bg-elevated: #FFFFFF;  /* Card background */

/* Dark mode */
--color-bg-dark: #141414;
--color-bg-secondary-dark: #222222;
```

### Text Colors

```css
/* Light mode */
--color-text: #222222;           /* Primary text */
--color-text-secondary: #717171; /* Secondary text */
--color-text-tertiary: #B0B0B0;  /* Auxiliary text */
--color-text-disabled: #C4C4C4;

/* Dark mode */
--color-text-dark: #FFFFFF;
--color-text-secondary-dark: #B0B0B0;
```

### Border Colors

```css
--color-border: #EBEBEB;
--color-border-light: #F7F7F7;
--color-border-dark: #DDDDDD;
```

### Accent Colors

#### Why Warm Gray Tone?

**Stone gray (#F7F7F7) vs Cool gray (#F5F5F5)**

- Warm gray conveys warmth and belonging
- Aligns with Airbnb brand tone
- Distinguishes from the cold feel of tech products
- Creates a "home" atmosphere

**Usage Hierarchy:**

- Background: #F7F7F7 (light warm gray) - secondary background
- Border: #DDDDDD (medium warm gray) - dividers
- Text: #717171 (deep warm gray) - secondary text

**Avoid:**

- Pure white #FFFFFF overuse (appears cold)
- Cool gray tones #F5F5F5 (loses warmth)
- Pure black #000000 (too harsh)

```css
/* Airbnb Signature Accents */
--color-accent: #FF5A5F;        /* Coral Red */
--color-accent-teal: #00A699;   /* Teal - Trust */
--color-accent-green: #008A05;  /* Green - Success */
--color-accent-yellow: #FFB400; /* Yellow - Stars */
--color-accent-orange: #FC642D; /* Orange */
```

### Functional Colors

```css
--color-success: #008A05;
--color-warning: #FFB400;
--color-error: #C13515;
--color-info: #428BFF;
```

---

## Interaction Philosophy

### Animation Principles

**Restrained, Natural, Meaningful**

Animations are not for showing off, but for:

- Providing clear state feedback
- Guiding user attention
- Conveying brand character

#### Entrance Animations

- Fade in + translateY
- Duration: 200ms
- Easing: ease-out
- Gentle appearance, not abrupt

#### Hover Feedback

- Cards: translateY(-4px)
- Buttons: Background darkens by 10%
- Icons: Scale 1.05x
- Images: Scale 1.03

#### State Transitions

- Smooth transitions (200ms ease-out)
- Avoid abrupt changes
- Maintain visual continuity

#### Animations to Avoid

- Rapid flashing (causes anxiety)
- Bounce effects (unprofessional)
- Multiple overlapping animations (appears messy)
- Rotating spinners (too common)

### Feedback Mechanisms

**Instant, Clear, Gentle**

#### Button Feedback

- Click: Scale 0.98
- Hover: Background change + slight lift
- Disabled: Opacity 0.5 + not-allowed

#### Input Feedback

- Focus: Border highlight + glow
- Error: Red border + shake animation
- Success: Green border + checkmark icon

#### Loading States

- Gentle pulse (breathing effect)
- Avoid rotating spinners (too common)
- Skeleton screens for content loading

---

## Layout Principles

### Spacing Strategy

**8px Grid System**

- All spacing is multiples of 4
- Ensures consistent visual rhythm
- Simpler development implementation

**Common Spacing:**

- Page edges: 64px (desktop)
- Between modules: 48px
- Between cards: 24px
- Inside cards: 12-16px
- Small element spacing: 8px

### Whitespace Principles

**Generous Whitespace, Let Content Breathe**

#### Horizontal Whitespace

- Desktop: 64px
- Tablet: 40px
- Mobile: 16px

#### Vertical Whitespace

- Page top: 80px (space for navbar)
- Between modules: 48-64px
- Between paragraphs: 24px

#### Why So Much Whitespace?

- Let property photos be the hero
- Convey a calm, elegant lifestyle
- Align with premium travel positioning
- Improve reading comfort

### Content Max Width

- Desktop: 1200px (centered content)
- Card max width: 400px
- Text reading width: 65ch (optimal reading experience)

---

## Component Design Decisions

### Buttons

#### Why 48px Height?

**Touch-Friendly:**

- Minimum touch target on mobile: 44px (Apple HIG)
- 48px is more generous, better experience
- Easy for finger tapping

**Visual Balance:**

- Coordinates with large image scenes
- Doesn't appear too crowded
- Follows generous layout principle

#### Why 8px Border Radius?

**Approachability:**

- More friendly and warm than 4px
- More refined and professional than 12px

**Brand Alignment:**

- Conveys openness and inclusivity
- Aligns with "Belong Anywhere"
- Distinguishes from the sharp feel of financial products

### Cards

#### Why 12px Border Radius?

- More rounded than buttons (8px)
- Creates a container feel
- More gentle and friendly

#### Why overflow: hidden?

- Required for image border-radius
- Prevents content overflow
- Clean and neat appearance

#### Why Hover Lift?

- Provides interaction feedback
- Adds depth
- Encourages user clicks

### Inputs

#### Why 56px Height?

- Taller than buttons (48px)
- Easier for entering content
- More visually prominent

#### Why 12px Border Radius?

- Consistent with cards
- Maintains visual unity
- Friendly but refined

#### Why Focus Glow?

- Clear state feedback
- Doesn't change border thickness (avoids layout jumping)
- Gentle visual effect

---

## Typography Scale

```css
--font-size-xs: 12px;
--font-size-sm: 14px;
--font-size-base: 16px;
--font-size-md: 18px;
--font-size-lg: 20px;
--font-size-xl: 24px;
--font-size-2xl: 30px;
--font-size-3xl: 36px;
--font-size-4xl: 48px;
--font-size-5xl: 60px;
```

### Font Weights

```css
--font-weight-normal: 400;
--font-weight-medium: 500;
--font-weight-semibold: 600;
--font-weight-bold: 700;
```

### Font Family

```css
--font-family: 'Airbnb Cereal', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
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
--space-24: 96px;
```

---

## Border Radius System

```css
--radius-sm: 8px;
--radius-md: 12px;
--radius-lg: 16px;
--radius-xl: 24px;
--radius-2xl: 32px;
--radius-full: 9999px;
```

---

## Shadows

```css
--shadow-sm: 0 1px 2px rgba(0, 0, 0, 0.08);
--shadow-md: 0 2px 8px rgba(0, 0, 0, 0.12);
--shadow-lg: 0 6px 20px rgba(0, 0, 0, 0.15);
--shadow-xl: 0 12px 40px rgba(0, 0, 0, 0.2);
```

---

## Component Specifications

### Buttons

```css
.btn-primary {
  background: #FF5A5F;
  color: white;
  height: 48px;
  padding: 0 24px;
  border-radius: 8px;
  font-weight: 600;
  font-size: 16px;
  transition: all 0.2s ease;
}

.btn-primary:hover {
  background: #FF7E82;
}

.btn-secondary {
  background: white;
  color: #222222;
  height: 48px;
  padding: 0 24px;
  border: 1px solid #DDDDDD;
  border-radius: 8px;
  font-weight: 600;
}

.btn-secondary:hover {
  border-color: #222222;
}

.btn-ghost {
  background: transparent;
  color: #222222;
  height: 40px;
  padding: 0 16px;
}

.btn-ghost:hover {
  background: #F7F7F7;
}

.btn-icon {
  width: 48px;
  height: 48px;
  border-radius: 50%;
  background: white;
  border: 1px solid #DDDDDD;
  display: flex;
  align-items: center;
  justify-content: center;
}

.btn-icon:hover {
  border-color: #222222;
  transform: scale(1.05);
}
```

### Cards

```css
.card {
  background: white;
  border-radius: 12px;
  overflow: hidden;
  transition: transform 0.3s ease;
}

.card:hover {
  transform: translateY(-4px);
}

.card-image {
  width: 100%;
  aspect-ratio: 4/3;
  object-fit: cover;
  border-radius: 12px;
}

.card-image-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-template-rows: 1fr 1fr;
  gap: 2px;
  border-radius: 12px;
  overflow: hidden;
}

.card-title {
  font-size: 16px;
  font-weight: 600;
  color: #222222;
  margin-top: 12px;
}

.card-subtitle {
  font-size: 14px;
  color: #717171;
  margin-top: 4px;
}

.card-price {
  font-size: 16px;
  font-weight: 600;
  color: #222222;
}
```

### Inputs

```css
.input {
  height: 56px;
  padding: 0 16px;
  border: 1px solid #DDDDDD;
  border-radius: 12px;
  font-size: 16px;
  background: white;
  transition: all 0.2s ease;
}

.input:focus {
  outline: none;
  border-color: #222222;
  box-shadow: 0 0 0 2px rgba(34, 34, 34, 0.1);
}

.input-search {
  height: 66px;
  border-radius: 40px;
  padding: 0 24px;
  font-size: 16px;
  box-shadow: 0 1px 2px rgba(0, 0, 0, 0.08), 0 4px 12px rgba(0, 0, 0, 0.05);
}

.input-search:focus {
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1), 0 8px 16px rgba(0, 0, 0, 0.1);
}
```

### Tags

```css
.tag {
  display: inline-flex;
  align-items: center;
  height: 32px;
  padding: 0 12px;
  background: #F7F7F7;
  border-radius: 9999px;
  font-size: 14px;
  color: #222222;
}

.tag-active {
  background: #222222;
  color: white;
}

.tag-with-icon {
  padding-right: 8px;
}

.tag-icon {
  width: 24px;
  height: 24px;
  margin-right: 8px;
}
```

---

## Animations

```css
--duration-fast: 0.15s;
--duration-normal: 0.2s;
--duration-slow: 0.3s;

--ease-out: cubic-bezier(0.25, 0.1, 0.25, 1);
--ease-in-out: cubic-bezier(0.4, 0, 0.2, 1);
```

### Animation Characteristics

- **Card Hover:** Slight lift (translateY -4px)
- **Image Scale:** Image slightly enlarges on hover
- **Search Expand:** Shadow deepens on focus
- **Smooth Transitions:** All state changes transition smoothly

---

## Application Scenarios

### Scenario 1: Travel & Accommodation

**Core Applications:**

- Coral red CTA buttons ("Book Now")
- Large image card layout (property display)
- Warm gray background (#F7F7F7)
- Generous whitespace (64px page edges)
- Rounded cards (12px border-radius)

**Adjustments:**

- Maintain warm tone
- Emphasize photo display
- Use star ratings (yellow + coral red)

### Scenario 2: Community & Sharing Economy

**Core Applications:**

- Approachable design (8-12px border-radius)
- Friendly avatars (circular)
- Trust colors (teal accent #00A699)
- Social elements (likes, comments)

**Adjustments:**

- Add social elements
- Emphasize user avatars and identity
- Use richer functional colors

### Scenario 3: Local Services

**Core Applications:**

- Clear information hierarchy
- Easy-to-use form design (56px input height)
- Clear operation guidance
- Trust elements (reviews, verification)

**Adjustments:**

- Emphasize functionality
- Simplify decoration
- Highlight service provider information

### Scenario 4: Admin Dashboard

**Adjustments Needed:**

- Add dark mode (#141414 background)
- Sidebar navigation (vertical layout)
- Tighter spacing (24px → 16px)
- Data visualization (chart colors)

**Keep Unchanged:**

- Coral red primary color
- Warm gray tone
- Rounded style
- Friendly interaction feedback

### Scenario 5: Mobile App

**Key Adjustments:**

- Button height: 48px → 52px (easier to tap)
- Reduced spacing: 64px → 24px (limited screen space)
- Bottom navigation: fixed navbar
- Gesture interactions: swipe, pull-to-refresh

**Keep Unchanged:**

- Coral red primary color
- Rounded style
- Gentle animations

---

## Common Mistakes

### Common Errors

#### Error 1: Overusing Coral Red

- Wrong: Large area backgrounds, all buttons use coral red
- Correct: Sparingly applied, not exceeding 10% of page area
- Reason: Coral red has high saturation, large areas appear oppressive and cheap

#### Error 2: Using Cool Gray Tones

- Wrong: #F5F5F5 (cool gray) as background
- Correct: #F7F7F7 (warm gray)
- Reason: Loses warmth, cannot convey "home" atmosphere

#### Error 3: Border Radius Too Small

- Wrong: 4px border-radius (appears harsh)
- Correct: 8-12px border-radius
- Reason: Loses approachability, doesn't align with open and inclusive brand tone

#### Error 4: Animations Too Fast

- Wrong: 100ms rapid transitions
- Correct: 200ms calm transitions
- Reason: Loses elegance, appears rushed

#### Error 5: Insufficient Whitespace

- Wrong: Dense layout, minimized spacing
- Correct: Generous whitespace, let content breathe
- Reason: Loses premium feel, appears cheap

#### Error 6: Using Pure Black & White

- Wrong: #000000 text, #FFFFFF background (overused)
- Correct: #222222 dark gray, #F7F7F7 warm gray
- Reason: Too harsh, lacks warmth

### Negative Checklist

- Don't use pure black (#000000), use dark gray (#222222)
- Don't use cool gray tones (#F5F5F5), use warm gray (#F7F7F7)
- Don't use small border-radius (4px), use medium-large (8-12px)
- Don't use fast animations (< 150ms), use calm animations (200ms)
- Don't over-decorate, let content speak
- Don't use sharp edges, keep rounded and friendly
- Don't use rotating spinners, use gentle pulse or skeleton screens

---

## Best For

- Travel/Accommodation platforms
- Community/Sharing economy
- Local services
- Products that need to convey trust
- Products that need human care
- Products focused on large image display
