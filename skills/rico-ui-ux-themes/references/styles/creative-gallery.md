# Creative Gallery Style

Visual First, Grid Layout, Creative Inspiration, Resource Aggregation

---

## Design Philosophy

### Brand Philosophy

**"Show, Don't Tell"**

Creative Gallery design philosophy creates a content-first style for design resources and inspiration display. Through large image grid layout and minimal distraction design, creative works become the hero, quickly conveying visual inspiration.

### Design Philosophy

1. **Visual First - Content is King**
   - Large image display, maximize visual impact
   - Remove redundant decoration, let content speak
   - Image quality prioritizes over interface design

2. **Grid Layout - Efficient Browsing**
   - Unified card sizes
   - Responsive grid system
   - Adapt to various screen sizes

3. **Quick Discovery - Instant Inspiration**
   - Clear categories and tags
   - Efficient search and filtering
   - Fast loading, smooth browsing

4. **Professional Quality - Design-Oriented**
   - Restrained interface elements
   - High-quality image processing
   - Fits designer aesthetics

### Core Keywords

- Visual
- Gallery
- Creative
- Inspiration
- Curated

---

## Overview

Creative Gallery style is designed for design resource sites, inspiration galleries, and portfolio showcases. Large image grid layout, visual first, suitable for scenarios that need to display lots of images and visual content.

---

## Color System

### Brand Color

```css
/* Creative Gallery Deep Blue-Purple - Brand Primary Color */
--color-primary: #6366F1;
--color-primary-hover: #4F46E5;
--color-primary-light: #818CF8;
--color-primary-lighter: #EEF2FF;
```

#### Usage Guidelines

**When to Use:**

- CTA buttons (Submit, Favorite)
- Links and clickable elements
- Tags and categories
- Selected states, active states
- Brand identity

**Avoid Using:**

- Large area backgrounds (interferes with image display)
- Image borders (too flashy)
- Decorative elements

**Usage Principle:** About 5-8% of page area

**Why Deep Blue-Purple?**
- Creativity: Purple represents creativity and imagination
- Professionalism: Deep tones maintain professional quality
- Visual effect: Clear on white/gray background
- Industry characteristic: Common color for design tools and creative products

### Background Colors

```css
/* Light mode - Minimal white/gray */
--color-bg: #FFFFFF;
--color-bg-secondary: #F9FAFB;
--color-bg-tertiary: #F3F4F6;
--color-bg-elevated: #FFFFFF;

/* Dark mode */
--color-bg-dark: #111827;
--color-bg-secondary-dark: #1F2937;
--color-bg-tertiary-dark: #374151;
```

### Text Colors

```css
/* Light mode */
--color-text: #111827;
--color-text-secondary: #6B7280;
--color-text-tertiary: #9CA3AF;
--color-text-disabled: #D1D5DB;

/* Dark mode */
--color-text-dark: #F9FAFB;
--color-text-secondary-dark: #D1D5DB;
--color-text-tertiary-dark: #9CA3AF;
```

### Border Colors

```css
/* Light mode - Very light borders */
--color-border: #E5E7EB;
--color-border-light: #F3F4F6;
--color-border-focus: #6366F1;

/* Dark mode */
--color-border-dark: #374151;
--color-border-subtle-dark: #1F2937;
```

### Accent Colors

```css
/* Creative Gallery Functional Colors */
--color-accent-green: #10B981;   /* Green - Free/Public */
--color-accent-yellow: #F59E0B;  /* Yellow - Featured/Recommended */
--color-accent-red: #EF4444;     /* Red - Paid/Premium */
--color-accent-pink: #EC4899;    /* Pink - Trending/New */
--color-accent-cyan: #06B6D4;    /* Cyan - Tools/Plugins */
```

#### Functional Color Guidelines

- Free/Public: Green #10B981
- Featured/Recommended: Yellow #F59E0B
- Paid/Premium: Red #EF4444
- Trending/New: Pink #EC4899
- Tools/Plugins: Cyan #06B6D4

---

## Interaction Philosophy

### Animation Principles

**Smooth, Quick, Non-Intrusive**

Image galleries need a smooth browsing experience, animations should be quick and not distract from content.

#### State Feedback

- Focus: Border highlight (deep blue-purple)
- Hover: Image slight zoom (scale 1.05) + info overlay
- Click: Slight scale (scale 0.98)

#### Transition Duration

- Fast: 150ms (button hover)
- Normal: 200ms (image zoom)
- Slow: 300ms (page transition)

**Why This Design?**
- Fast response improves browsing experience
- Image zoom needs slightly longer (avoid dizziness)
- Maintain smoothness

#### Animations to Avoid

- Rotation, bounce (distracts from content)
- Complex 3D effects (too flashy)
- Long animations (> 300ms)
- Modal animations that block browsing

### Feedback Mechanisms

**Instant, Clear, Lightweight**

- Button click: Immediate background change
- Image hover: Immediately show info overlay
- Operation success: Green prompt (1.5s auto-dismiss)
- Operation failure: Red prompt + error explanation
- Loading state: Skeleton screen (image position)

---

## Layout Principles

### Spacing Strategy

**8px Grid System**

- All spacing is multiples of 8
- Ensures consistent grid alignment
- Suitable for image gallery standards

**Common Spacing:**

- Small spacing: 8px, 16px (grid gaps)
- Medium spacing: 24px, 32px (inside components)
- Large spacing: 48px, 64px (between modules)

### Grid Layout

**Responsive Grid System**

Image galleries need to adapt to various screens:

- Mobile: 2-column grid
- Tablet: 3-4 column grid
- Desktop: 4-5 column grid
- Large screen: 6-column grid

**Why This Design?**
- Maximize image display
- Adapt to various screen sizes
- Maintain consistent visual rhythm

### Image Specifications

**Unified Card Sizes**

- Card width: Adaptive to grid
- Card height: Fixed ratio (16:9 or 4:3)
- Image cropping: cover (fill)
- Image quality: Optimized loading

**Why Fixed Ratio?**
- Keeps grid neat
- Avoids layout jumping
- Easy batch processing

### Content Max Width

- Gallery area: Unlimited (full width)
- Content area: 1400px (max container)
- Sidebar: 320px
- Mobile: 100% (full width)

---

## Component Design Decisions

### Image Cards

#### Why Card Layout?

- Unified display unit
- Easy grid arrangement
- Clear boundaries

#### Why Hover Zoom?

- Enhances interaction feedback
- Highlights current content
- Improves browsing experience

#### Why Show Info Overlay?

- Doesn't disturb static display
- Provides more info on hover
- Keeps interface clean

### Tags and Categories

#### Why Small Tags?

- Quickly identify content type
- Doesn't take much space
- Clear visual rhythm

#### Why Colorful Tags?

- Quickly distinguish categories
- Enhances visual recognition
- Improves browsing efficiency

### Filter and Search

#### Why Fixed at Top?

- Always available
- Doesn't affect browsing
- Matches user habits

#### Why Minimal Design?

- Doesn't compete with content
- Quick operation
- Maintains focus

### Favorite Button

#### Why Fixed at Top-Right?

- Easy to click
- Doesn't block content
- Consistent position

#### Why Heart Icon?

- Universal symbol
- Clear and understandable
- Emotional connection

---

## Application Scenarios

### Scenario 1: Design Resource Sites

**Core Applications:**

- Large image grid layout
- Categories and tag system
- Favorite and share functions
- Quick search and filtering

**Adjustments:**

- Maintain image quality
- Optimize loading speed
- Strengthen category functions

### Scenario 2: Inspiration Gallery

**Core Applications:**

- Visual-first layout
- Minimal distraction design
- High-quality image display
- Smooth browsing experience

**Adjustments:**

- Add masonry layout
- Optimize image loading
- Strengthen discovery features

### Scenario 3: Portfolio Showcase

**Core Applications:**

- Personal brand display
- Project case display
- Contact information
- Social media links

**Adjustments:**

- Add personal introduction
- Strengthen project descriptions
- Optimize mobile experience

### Scenario 4: Product Screenshot Display

**Core Applications:**

- Product feature screenshots
- Multi-image carousel
- Detailed descriptions
- Download and share

**Adjustments:**

- Add image zoom function
- Optimize image annotations
- Strengthen download function

### Scenario 5: Photography Portfolio

**Core Applications:**

- High-quality images
- EXIF info display
- Photographer info
- Work categories

**Adjustments:**

- Add dark mode
- Optimize image display
- Strengthen share function

---

## Common Mistakes

### Common Errors

#### Error 1: Overusing Colors

- Wrong: All tags, all buttons use colors
- Correct: Restrained accents, highlight key points
- Reason: Loses focus, appears cluttered

#### Error 2: Cards Too Small

- Wrong: Too small image cards
- Correct: Adequate card size (minimum 280px)
- Reason: Affects browsing experience, loses visual impact

#### Error 3: Grid Gaps Too Large

- Wrong: 32px, 48px grid gaps
- Correct: 8-16px grid gaps
- Reason: Wastes space, low browsing efficiency

#### Error 4: Animations Too Slow

- Wrong: 300ms, 500ms slow transitions
- Correct: 150-200ms fast response
- Reason: Affects browsing efficiency

#### Error 5: Info Overlay Too Heavy

- Wrong: Dark background, large text info overlay
- Correct: Semi-transparent background, concise text
- Reason: Blocks images, affects browsing

#### Error 6: Ignoring Image Quality

- Wrong: Over-compressed, blurry images
- Correct: High-quality image optimization
- Reason: Loses visual impact

### Negative Checklist

- Don't use too small cards (< 280px), use appropriate size (280-400px)
- Don't use too large grid gaps (> 24px), use compact gaps (8-16px)
- Don't use slow animations (> 300ms), use fast (150-200ms)
- Don't over-decorate, let images speak
- Don't ignore image quality, optimize loading
- Don't use heavy info overlays, use lightweight overlays
- Don't ignore mobile experience, optimize touch interaction

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
/* Modern design font */
--font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
--font-family-display: 'Cal Sans', 'Inter', sans-serif;
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
```

---

## Border Radius System

```css
--radius-sm: 4px;
--radius-md: 8px;
--radius-lg: 12px;
--radius-xl: 16px;
```

---

## Shadows

```css
--shadow-sm: 0 1px 3px rgba(0, 0, 0, 0.1);
--shadow-md: 0 4px 6px rgba(0, 0, 0, 0.1);
--shadow-lg: 0 10px 15px rgba(0, 0, 0, 0.1);
--shadow-hover: 0 20px 25px rgba(0, 0, 0, 0.15);
```

---

## Component Specifications

### Image Cards

```css
.card {
  position: relative;
  border-radius: 12px;
  overflow: hidden;
  background: white;
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.1);
  transition: all 0.2s ease-out;
  cursor: pointer;
}

.card:hover {
  transform: translateY(-4px);
  box-shadow: 0 20px 25px rgba(0, 0, 0, 0.15);
}

.card-image {
  width: 100%;
  aspect-ratio: 16 / 9;
  object-fit: cover;
  transition: transform 0.2s ease-out;
}

.card:hover .card-image {
  transform: scale(1.05);
}

.card-overlay {
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  background: linear-gradient(to top, rgba(0, 0, 0, 0.8), transparent);
  padding: 24px 16px 16px;
  opacity: 0;
  transition: opacity 0.2s ease-out;
}

.card:hover .card-overlay {
  opacity: 1;
}

.card-title {
  color: white;
  font-size: 16px;
  font-weight: 600;
  margin-bottom: 4px;
}

.card-meta {
  color: rgba(255, 255, 255, 0.8);
  font-size: 14px;
}
```

### Tags

```css
.tag {
  display: inline-block;
  padding: 4px 12px;
  font-size: 12px;
  font-weight: 500;
  border-radius: 16px;
  background: #F3F4F6;
  color: #6B7280;
  transition: all 0.15s ease-out;
}

.tag:hover {
  background: #E5E7EB;
}

.tag-primary {
  background: #EEF2FF;
  color: #6366F1;
}

.tag-success {
  background: #D1FAE5;
  color: #10B981;
}

.tag-warning {
  background: #FEF3C7;
  color: #F59E0B;
}

.tag-error {
  background: #FEE2E2;
  color: #EF4444;
}
```

### Buttons

```css
.btn {
  height: 40px;
  padding: 0 16px;
  font-size: 14px;
  font-weight: 500;
  border-radius: 8px;
  transition: all 0.15s ease-out;
}

.btn-primary {
  background: #6366F1;
  color: white;
  border: none;
}

.btn-primary:hover {
  background: #4F46E5;
}

.btn-secondary {
  background: white;
  color: #111827;
  border: 1px solid #E5E7EB;
}

.btn-secondary:hover {
  background: #F9FAFB;
}

.btn-icon {
  width: 40px;
  height: 40px;
  padding: 0;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 50%;
  background: white;
  border: 1px solid #E5E7EB;
}
```

### Grid System

```css
.gallery-grid {
  display: grid;
  gap: 16px;
  grid-template-columns: repeat(2, 1fr);
}

@media (min-width: 640px) {
  .gallery-grid {
    grid-template-columns: repeat(3, 1fr);
  }
}

@media (min-width: 1024px) {
  .gallery-grid {
    grid-template-columns: repeat(4, 1fr);
  }
}

@media (min-width: 1280px) {
  .gallery-grid {
    grid-template-columns: repeat(5, 1fr);
  }
}

@media (min-width: 1536px) {
  .gallery-grid {
    grid-template-columns: repeat(6, 1fr);
  }
}
```

### Filter Bar

```css
.filter-bar {
  position: sticky;
  top: 0;
  background: white;
  border-bottom: 1px solid #E5E7EB;
  padding: 16px 0;
  z-index: 100;
  backdrop-filter: blur(8px);
}

.filter-group {
  display: flex;
  gap: 8px;
  overflow-x: auto;
  scrollbar-width: none;
}

.filter-group::-webkit-scrollbar {
  display: none;
}

.filter-btn {
  padding: 8px 16px;
  font-size: 14px;
  font-weight: 500;
  border-radius: 20px;
  background: #F3F4F6;
  color: #6B7280;
  border: none;
  white-space: nowrap;
  cursor: pointer;
  transition: all 0.15s ease-out;
}

.filter-btn:hover {
  background: #E5E7EB;
}

.filter-btn.active {
  background: #6366F1;
  color: white;
}
```

### Search Box

```css
.search-box {
  position: relative;
  width: 100%;
  max-width: 400px;
}

.search-input {
  width: 100%;
  height: 44px;
  padding: 0 16px 0 44px;
  font-size: 14px;
  border: 1px solid #E5E7EB;
  border-radius: 22px;
  background: #F9FAFB;
  transition: all 0.15s ease-out;
}

.search-input:focus {
  outline: none;
  border-color: #6366F1;
  background: white;
  box-shadow: 0 0 0 3px rgba(99, 102, 241, 0.1);
}

.search-icon {
  position: absolute;
  left: 14px;
  top: 50%;
  transform: translateY(-50%);
  color: #9CA3AF;
  pointer-events: none;
}
```

---

## Animations

```css
--duration-fast: 150ms;
--duration-normal: 200ms;
--duration-slow: 300ms;

--ease-out: cubic-bezier(0.16, 1, 0.3, 1);
--ease-spring: cubic-bezier(0.34, 1.56, 0.64, 1);
```

---

## Image Optimization

### Responsive Images

```html
<img
  src="image-800w.jpg"
  srcset="
    image-400w.jpg 400w,
    image-800w.jpg 800w,
    image-1200w.jpg 1200w
  "
  sizes="(max-width: 640px) 50vw,
         (max-width: 1024px) 33vw,
         25vw"
  alt="Description"
  loading="lazy"
/>
```

### Placeholder

```css
.image-placeholder {
  aspect-ratio: 16 / 9;
  background: linear-gradient(
    90deg,
    #F3F4F6 25%,
    #E5E7EB 50%,
    #F3F4F6 75%
  );
  background-size: 200% 100%;
  animation: shimmer 1.5s infinite;
}

@keyframes shimmer {
  0% { background-position: 200% 0; }
  100% { background-position: -200% 0; }
}
```

---

## Best For

- Design resource sites
- Inspiration galleries
- Portfolio showcases
- Product screenshot displays
- Photography portfolios
- Illustration libraries
- UI/UX case studies
- Font showcase sites
