# Vibrant Commerce Style

Energetic Promotions, Visual Impact, Urgent Action, Large Image Display

---

## Design Philosophy

### Brand Philosophy

**"Action & Excitement"**

Vibrant Commerce design philosophy stimulates purchase desire and action. In e-commerce, shopping, and retail, the key is to attract user attention and drive conversions. Design uses orange-red tones and striking visual elements to create a vibrant, urgent, and exciting shopping atmosphere.

### Design Philosophy

1. **Visual Impact - Attract Attention**
   - Orange-red primary color (psychologically stimulates appetite and purchase)
   - Large image display (product-focused)
   - High contrast design

2. **Urgent Action - Drive Conversion**
   - Prominent CTA buttons
   - Countdown timers, limited quantity indicators
   - Striking price tags
   - Fast animations (100-150ms)

3. **Information Dense - Quick Browsing**
   - Compact layout (high information density)
   - Clear price comparisons
   - Prominent discount labels
   - Efficient information hierarchy

4. **Promotion Oriented - Stimulate Spending**
   - Yellow accents (deals, promotions)
   - Red emphasis (markdowns, hot sellers)
   - Eye-catching badges (NEW, HOT)
   - Social proof elements

### Core Keywords

- Energetic
- Urgent
- Bold
- Promotional
- Visual

---

## Overview

Vibrant Commerce style is designed for e-commerce, shopping, retail, group buying, and other conversion-focused industries. Orange-red primary tone stimulates purchase desire, yellow accents convey promotions, and large image display highlights products.

---

## Color System

### Brand Color

```css
/* Vibrant Commerce Orange-Red - Stimulate Action */
--color-primary: #FF5722;
--color-primary-hover: #F4511E;
--color-primary-dark: #E64A19;
--color-primary-light: #FF8A65;

/* Secondary Color - Promotion Yellow */
--color-secondary: #FFC107;
--color-secondary-hover: #FFB300;
```

#### Usage Guidelines

**When to Use:**

- CTA buttons ("Buy Now", "Add to Cart")
- Price tags
- Discount indicators
- Hot/Limited time indicators
- Links and clickable elements

**Avoid Using:**

- Large area backgrounds (too harsh)
- Long text reading (contrast issues)
- Non-critical information
- Decorative elements

**Usage Principle:** About 25-30% of page area (more than other themes)

**Why Orange-Red?**
- Psychology: Stimulates appetite, promotes purchasing, creates urgency
- Industry standard: Common color for e-commerce and retail
- Visual effect: Striking, energetic, impossible to ignore
- Differentiation: Distinguishes from professional finance and health colors

### Background Colors

```css
/* Light mode - Warm yellow-white */
--color-bg: #FFFFFF;           /* Main background - Pure white */
--color-bg-secondary: #FFF8E1; /* Secondary background - Light yellow */
--color-bg-tertiary: #FFF3E0;   /* Auxiliary background */
--color-bg-elevated: #FFFFFF;   /* Floating layer - Pure white */

/* Dark mode */
--color-bg-dark: #121212;
--color-bg-secondary-dark: #1E1E1E;
--color-bg-tertiary-dark: #2C2C2C;
```

**Why Light Yellow Background Instead of Pure White?**
- Conveys promotional atmosphere
- Distinguishes from regular content
- Adds warmth
- Shopping excitement

### Text Colors

```css
/* Light mode */
--color-text: #212121;           /* Primary text - Deep black */
--color-text-secondary: #757575; /* Secondary text */
--color-text-tertiary: #BDBDBD;  /* Auxiliary text */
--color-text-disabled: #E0E0E0;

/* Dark mode */
--color-text-dark: #FFFFFF;
--color-text-secondary-dark: #BDBDBD;
--color-text-tertiary-dark: #757575;
```

**Why Deep Black Instead of Dark Gray?**
- High contrast (ensures readability)
- Striking, uncompromising
- Price display more prominent

### Border Colors

```css
/* Light mode */
--color-border: #E0E0E0;
--color-border-light: #EEEEEE;
--color-border-focus: #FF5722; /* Orange-red on focus */

/* Dark mode */
--color-border-dark: #424242;
--color-border-subtle-dark: #333333;
```

### Accent Colors

```css
/* Vibrant Commerce Signature Accents */
--color-accent-orange: #FF5722;  /* Orange-Red - Primary accent */
--color-accent-yellow: #FFC107;  /* Yellow - Promotions/Deals */
--color-accent-red: #D32F2F;     /* Red - Hot sellers/Markdowns */
--color-accent-green: #4CAF50;   /* Green - New arrivals/In stock */
--color-accent-blue: #2196F3;    /* Blue - Trust/Official */
--color-accent-purple: #9C27B0;  /* Purple - Premium/VIP */
```

#### Functional Color Guidelines

- Promotions/Deals: Yellow #FFC107
- Hot sellers/Markdowns: Red #D32F2F
- New arrivals/In stock: Green #4CAF50
- Official/Self-operated: Blue #2196F3
- Premium/VIP: Purple #9C27B0

**E-commerce Color Meanings:**
- Orange-red: Stimulates purchase, CTA
- Yellow: Deals, promotions, discounts
- Red: Hot sellers, markdowns, urgency
- Green: New arrivals, in stock, eco-friendly

---

## Interaction Philosophy

### Animation Principles

**Fast, Powerful, Attractive**

E-commerce products need quick response to user actions, animations should be fast and powerful.

#### State Feedback

- Focus: Border highlight (orange-red) + glow (prominent)
- Hover: Noticeable background change (#FFF3E0)
- Click: Quick scale (scale 0.95)

#### Transition Duration

- Fast: 100ms (button hover)
- Normal: 150ms (panel expand)
- Slow: 200ms (page transition)

**Why So Fast?**
- Quick response to user actions
- Reduces waiting feeling
- Improves conversion rate
- Maintains shopping pace

#### Animations to Avoid

- Slow transitions (> 300ms)
- Complex animations (dragging)
- Flashy effects (distracting)
- Long loading times
- Blocking operations

### Feedback Mechanisms

**Instant, Noticeable, Rewarding**

- Button click: Immediate background change + scale
- Input focus: Immediate border highlight
- Add to cart: Animation + quantity update
- Operation success: Green prompt + checkmark animation
- Operation failure: Red prompt + shake

---

## Layout Principles

### Spacing Strategy

**Compact 4px/8px Grid System**

- All spacing is multiples of 4
- Values tend to be smaller (compact)
- High information density

**Common Spacing:**

- Small spacing: 4px, 8px (related elements)
- Medium spacing: 12px, 16px (inside components)
- Large spacing: 24px, 32px (between modules)
- Page edges: 24px (mobile), 48px (desktop)

### Compact Layout

**Information Density First**

E-commerce needs to display lots of product information, layout is relatively compact:

- Product card spacing: 16px
- Product info spacing: 8px
- Price tags prominent
- Ratings/sales clear

**Why So Compact?**
- Display more products per screen
- Reduce scrolling
- Improve browsing efficiency
- Promote discovery and purchase

### Content Max Width

- Product list: 1400px (display more)
- Product detail: 1200px
- Shopping cart: 1000px
- Articles: 800px (campaign info)

---

## Component Design Decisions

### Buttons

#### Why 44-48px Height?

- Touch-friendly (mobile)
- Visually prominent (can't be ignored)
- Follows e-commerce standards

#### Why 8px Border Radius?

- Moderate roundness (not too rounded)
- Maintains energetic feel
- Distinguishes from finance (small) and health (large)

#### Why Orange-Red Primary Button?

- Stimulates purchase (psychology)
- Striking, impossible to ignore
- Industry standard
- Conveys urgency

### Product Cards

#### Why Large Image Display?

- Product-focused (visual impact)
- Stimulates purchase desire
- Improves click-through rate
- Industry standard

#### Why Compact Information Layout?

- Price, discount, sales visible at a glance
- Reduces scrolling
- Improves browsing efficiency
- Promotes comparison decisions

### Price Tags

#### Why Prominent Design?

- Orange-red primary price
- Large font size (20-24px)
- Bold display
- Compare with original price (strikethrough)

#### Why Yellow Discount Tags?

- Yellow represents promotion
- High contrast (attracts attention)
- Urgency (limited time offers)
- Industry standard

### Badges/Tags

#### Why Eye-catching Design?

- NEW (new arrivals): Green background
- HOT (hot sellers): Red background
- Limited: Red countdown
- VIP: Purple background

---

## Application Scenarios

### Scenario 1: E-commerce Platform

**Core Applications:**

- Orange-red CTA ("Buy Now")
- Prominent price tags
- Yellow discount indicators
- Compact product cards

**Adjustments:**

- Optimize product image quality
- Highlight price and discounts
- Add social proof (reviews)

### Scenario 2: Shopping/Retail

**Core Applications:**

- Large image display (product-focused)
- Prominent promotion info
- Compact product list
- Fast checkout flow

**Adjustments:**

- Highlight product features
- Optimize mobile experience
- Simplify checkout process

### Scenario 3: Group Buying/Flash Sales

**Core Applications:**

- Red countdown (urgency)
- Limited quantity indicator (stock)
- Prominent discounts
- Social proof (sold count)

**Adjustments:**

- Strengthen urgency elements
- Highlight social interaction
- Optimize sharing features

### Scenario 4: Brand Website

**Core Applications:**

- Large image visual impact
- Brand storytelling
- Product series display
- Store locator

**Adjustments:**

- Add brand personality
- Optimize visual design
- Highlight product series

### Scenario 5: O2O Services

**Core Applications:**

- Orange-red action buttons
- Clear service list
- Prominent pricing
- User review display

**Adjustments:**

- Highlight service features
- Optimize mobile experience
- Strengthen trust elements

---

## Common Mistakes

### Common Errors

#### Error 1: Using Low Saturation Colors

- Wrong: Soft orange, gray tones
- Correct: High saturation orange-red (#FF5722)
- Reason: Loses urgency, cannot stimulate purchase

#### Error 2: Information Layout Too Loose

- Wrong: Lots of whitespace, sparse layout
- Correct: Compact layout, information dense
- Reason: Low browsing efficiency, affects conversion

#### Error 3: Animations Too Slow

- Wrong: 300ms+ slow transitions
- Correct: 100-150ms fast response
- Reason: Dragging feeling, affects purchase pace

#### Error 4: Price Tags Not Prominent

- Wrong: Small font size, low contrast
- Correct: Large font size, orange-red, bold
- Reason: Misses key information, affects decisions

#### Error 5: Missing Promotional Elements

- Wrong: No discounts, no badges, no countdown
- Correct: Yellow discounts, red hot sellers, countdown
- Reason: Loses urgency, lowers conversion

#### Error 6: Poor Image Quality

- Wrong: Blurry, small images, multiple image collage
- Correct: HD large images, single image focus
- Reason: Loses visual impact, affects purchase desire

### Negative Checklist

- Don't use low saturation colors, use high saturation orange-red
- Don't use loose layout, use compact layout
- Don't use slow animations (> 200ms), use fast (100-150ms)
- Don't make price tags subtle, make them prominent
- Don't miss promotional elements (discounts, badges, countdown)
- Don't use poor quality images, use HD large images
- Don't over-decorate, keep product-focused

---

## Typography Scale

```css
--font-size-xs: 10px;
--font-size-sm: 12px;
--font-size-base: 14px;
--font-size-md: 16px;
--font-size-lg: 18px;
--font-size-xl: 20px;
--font-size-2xl: 24px;
--font-size-3xl: 32px;
--font-size-4xl: 48px;
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
/* Modern, compact font */
--font-family: 'Inter', 'Roboto', -apple-system, sans-serif;
--font-family-mono: 'JetBrains Mono', 'Roboto Mono', monospace;
```

---

## Spacing System

```css
--space-1: 4px;
--space-2: 8px;
--space-3: 12px;
--space-4: 16px;
--space-5: 24px;
--space-6: 32px;
--space-8: 48px;
--space-10: 64px;
```

---

## Border Radius System

```css
--radius-sm: 4px;
--radius-md: 8px;
--radius-lg: 12px;
--radius-xl: 16px;
--radius-2xl: 24px;
--radius-full: 9999px;
```

---

## Shadows

```css
--shadow-sm: 0 1px 3px rgba(0, 0, 0, 0.12);
--shadow-md: 0 4px 8px rgba(0, 0, 0, 0.15);
--shadow-lg: 0 8px 16px rgba(0, 0, 0, 0.18);
--shadow-xl: 0 16px 32px rgba(0, 0, 0, 0.22);

/* Colored shadows - Vibrant feature */
--shadow-accent: 0 4px 16px rgba(255, 87, 34, 0.3);
--shadow-glow: 0 0 20px rgba(255, 87, 34, 0.4);
```

---

## Component Specifications

### Buttons

```css
.btn-primary {
  background: #FF5722;
  color: white;
  height: 48px;
  padding: 0 24px;
  border-radius: 8px;
  font-weight: 700;
  font-size: 16px;
  transition: all 0.15s cubic-bezier(0.4, 0, 0.6, 1);
  box-shadow: 0 2px 8px rgba(255, 87, 34, 0.3);
}

.btn-primary:hover {
  background: #F4511E;
  transform: translateY(-2px);
  box-shadow: 0 4px 16px rgba(255, 87, 34, 0.4);
}

.btn-primary:active {
  transform: scale(0.95);
}

.btn-secondary {
  background: #FFC107;
  color: #212121;
  height: 48px;
  padding: 0 24px;
  border-radius: 8px;
  font-weight: 700;
}

.btn-secondary:hover {
  background: #FFB300;
}

.btn-outline {
  background: transparent;
  color: #FF5722;
  border: 2px solid #FF5722;
  height: 48px;
  padding: 0 24px;
  border-radius: 8px;
  font-weight: 700;
}

.btn-outline:hover {
  background: #FF5722;
  color: white;
}

.btn-ghost {
  background: transparent;
  color: #757575;
  height: 44px;
  padding: 0 20px;
}

.btn-ghost:hover {
  background: #F5F5F5;
  color: #212121;
}
```

### Product Cards

```css
.product-card {
  background: white;
  border: 1px solid #E0E0E0;
  border-radius: 8px;
  overflow: hidden;
  transition: all 0.2s ease;
}

.product-card:hover {
  box-shadow: 0 4px 16px rgba(0, 0, 0, 0.15);
  transform: translateY(-4px);
}

.product-image {
  width: 100%;
  aspect-ratio: 1;
  object-fit: cover;
}

.product-info {
  padding: 16px;
}

.product-title {
  font-size: 14px;
  font-weight: 500;
  color: #212121;
  margin-bottom: 8px;
  line-height: 1.4;
  height: 40px;
  overflow: hidden;
}

.product-price {
  font-size: 20px;
  font-weight: 700;
  color: #FF5722;
  margin-bottom: 4px;
}

.product-price-original {
  font-size: 14px;
  color: #BDBDBD;
  text-decoration: line-through;
  margin-left: 8px;
}

.product-badge {
  position: absolute;
  top: 8px;
  left: 8px;
  padding: 4px 8px;
  border-radius: 4px;
  font-size: 10px;
  font-weight: 700;
  color: white;
}

.badge-new {
  background: #4CAF50;
}

.badge-hot {
  background: #D32F2F;
}

.badge-sale {
  background: #FFC107;
  color: #212121;
}
```

### Price Tags

```css
.price-tag {
  display: inline-flex;
  align-items: baseline;
}

.price-current {
  font-size: 24px;
  font-weight: 700;
  color: #FF5722;
  line-height: 1;
}

.price-original {
  font-size: 16px;
  color: #BDBDBD;
  text-decoration: line-through;
  margin-left: 8px;
}

.price-discount {
  background: #FFC107;
  color: #212121;
  padding: 2px 8px;
  border-radius: 4px;
  font-size: 12px;
  font-weight: 700;
  margin-left: 8px;
}
```

### Badges/Tags

```css
.badge {
  display: inline-flex;
  align-items: center;
  height: 24px;
  padding: 0 8px;
  border-radius: 4px;
  font-size: 11px;
  font-weight: 700;
  color: white;
}

.badge-new {
  background: #4CAF50;
}

.badge-hot {
  background: #D32F2F;
}

.badge-sale {
  background: #FF5722;
}

.badge-limited {
  background: #D32F2F;
  animation: pulse 1s infinite;
}

@keyframes pulse {
  0%, 100% {
    opacity: 1;
  }
  50% {
    opacity: 0.7;
  }
}
```

### Inputs

```css
.input {
  height: 48px;
  padding: 0 16px;
  border: 2px solid #E0E0E0;
  border-radius: 8px;
  font-size: 16px;
  background: white;
  transition: all 0.2s ease;
}

.input:focus {
  outline: none;
  border-color: #FF5722;
  box-shadow: 0 0 0 3px rgba(255, 87, 34, 0.2);
}

.input-search {
  height: 52px;
  border-radius: 9999px;
  padding: 0 24px;
}
```

---

## Animations

```css
--duration-fast: 0.1s;
--duration-normal: 0.15s;
--duration-slow: 0.2s;

--ease-out: cubic-bezier(0.25, 0.1, 0.25, 1);
--ease-in-out: cubic-bezier(0.4, 0, 0.2, 1);
```

### Animation Characteristics

- **Quick Response**: 100-150ms transitions
- **Scale Click**: Button press (scale 0.95)
- **Lift on Hover**: Card lift (translateY -4px)
- **Colored Shadow**: Brand color shadow on hover
- **Pulse Animation**: Countdown, limited indicators

```css
/* Add to cart animation */
@keyframes cart-bounce {
  0% {
    transform: scale(1);
  }
  50% {
    transform: scale(1.2);
  }
  100% {
    transform: scale(1);
  }
}

/* Countdown pulse */
@keyframes countdown-pulse {
  0%, 100% {
    opacity: 1;
  }
  50% {
    opacity: 0.6;
  }
}
```

---

## Best For

- E-commerce platforms
- Shopping/Retail
- Group buying/Flash sales
- Brand websites
- O2O services
- Offline retail
- Social commerce
- Cross-border e-commerce
