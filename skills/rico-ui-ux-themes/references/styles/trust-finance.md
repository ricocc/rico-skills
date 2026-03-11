# Trust Finance Style

Secure, Trustworthy, Professional, Stable, Reliable

---

## Design Philosophy

### Brand Philosophy

**"Security & Trust"**

Trust Finance design philosophy conveys security and professionalism. In fintech, payments, and B2B sectors, what users care about most is trust and reliability. Design conveys a professional, secure, and trustworthy brand image through deep blue tones and gold accents.

### Design Philosophy

1. **Security First - Building Trust**
   - Deep blue primary color (psychologically represents trust, security)
   - Restrained, professional design style
   - Clear, transparent information display

2. **Professional & Stable - Reliable Image**
   - Small border-radius (6-8px) conveys professionalism
   - Generous whitespace creates stability
   - Restrained animations avoid flashiness

3. **Clear & Transparent - Information First**
   - High contrast text ensures readability
   - Clear information hierarchy
   - Data visualization priority

4. **Modern Tech - Contemporary**
   - Slight gradients add modern feel
   - Subtle shadows enhance quality
   - Moderate animations keep it fresh

### Core Keywords

- Trust
- Secure
- Professional
- Reliable
- Stable

---

## Overview

Trust Finance style is designed for fintech, banking, insurance, B2B, and other industries that need to build strong trust. Deep blue primary tone conveys security and reliability, gold accents convey success and wealth.

---

## Color System

### Brand Color

```css
/* Trust Finance Deep Blue - Trust & Security */
--color-primary: #0052CC;
--color-primary-hover: #0065FF;
--color-primary-dark: #0747A6;
--color-primary-light: #DEEBFF;

/* Secondary Color - Gold Wealth */
--color-secondary: #FFAB00;
--color-secondary-hover: #FFC400;
```

#### Usage Guidelines

**When to Use:**

- CTA buttons (primary actions like "Open Account Now", "Pay")
- Navigation bar active states
- Important data highlights
- Links and clickable elements
- Chart primary color

**Avoid Using:**

- Large area backgrounds (deep blue is too heavy)
- Non-critical action buttons
- Decorative elements
- Small text (contrast issues)

**Usage Principle:** About 15-20% of page area

**Why Deep Blue?**
- Psychology: Deep blue represents trust, security, professionalism
- Industry convention: Common color for banks, financial institutions
- Visual effect: Stable, calm, rational
- Differentiation: Distinguishes from entertainment, consumer product vibrant colors

### Background Colors

```css
/* Light mode - Cool gray-white */
--color-bg: #FAFBFC;           /* Main background - Very light blue-gray */
--color-bg-secondary: #F4F5F7; /* Secondary background */
--color-bg-tertiary: #EBECF0;   /* Auxiliary background */
--color-bg-elevated: #FFFFFF;   /* Floating layer - Pure white */

/* Dark mode */
--color-bg-dark: #121212;
--color-bg-secondary-dark: #1F1F1F;
--color-bg-tertiary-dark: #2C2C2C;
```

**Why Cool Gray-White vs Pure White?**
- Reduces harshness
- Conveys professionalism, calmness
- Distinguishes from consumer product pure white

### Text Colors

```css
/* Light mode */
--color-text: #172B4D;           /* Primary text - Deep blue-black */
--color-text-secondary: #5E6C84; /* Secondary text */
--color-text-tertiary: #97A0AF;  /* Auxiliary text */
--color-text-disabled: #B3BAC5;

/* Dark mode */
--color-text-dark: #FAFBFC;
--color-text-secondary-dark: #A0AEC0;
--color-text-tertiary-dark: #718096;
```

**Why Deep Blue-Black vs Pure Black?**
- Soft but maintains contrast
- Fits the blue tone system
- Avoids being too harsh

### Border Colors

```css
/* Light mode */
--color-border: #DFE1E6;
--color-border-light: #EBECF0;
--color-border-focus: #0052CC; /* Blue on focus */

/* Dark mode */
--color-border-dark: #4A5568;
--color-border-subtle-dark: #2D3748;
```

### Accent Colors

```css
/* Trust Finance Signature Accents */
--color-accent-blue: #0052CC;    /* Deep blue - Primary accent */
--color-accent-gold: #FFAB00;    /* Gold - Wealth/Success */
--color-accent-green: #36B37E;   /* Green - Growth/Profit */
--color-accent-red: #FF5630;     /* Red - Decline/Loss */
--color-accent-teal: #00875A;    /* Teal - Success/Complete */
--color-accent-purple: #6554C0;  /* Purple - Premium Features */
```

#### Functional Color Guidelines

- Success/Profit: Green #36B37E
- Warning: Gold #FFAB00
- Error/Loss: Red #FF5630
- Info: Deep Blue #0052CC

**Financial Color Meanings:**
- Green represents profit, growth
- Red represents loss, decline
- Gold represents wealth, VIP

---

## Interaction Philosophy

### Animation Principles

**Restrained, Professional, Meaningful**

Financial products need to convey stability, animations cannot be too flashy.

#### State Feedback

- Focus: Border highlight (deep blue) + glow (subtle)
- Hover: Slight background change (#EBECF0)
- Click: Slight scale (scale 0.98)

#### Transition Duration

- Fast: 150ms (button hover)
- Normal: 200ms (panel expand)
- Slow: 300ms (page transition)

**Why So Restrained?**
- Conveys professional stability
- Avoids distraction
- Increases credibility

#### Animations to Avoid

- Rapid flashing (causes anxiety)
- Bounce effects (unprofessional)
- Complex 3D effects (excessive)
- Long animations (> 400ms)
- Colorful gradient animations (too flashy)

### Feedback Mechanisms

**Instant, Clear, Professional**

- Button click: Immediate background change
- Input focus: Immediate border highlight (deep blue)
- Operation success: Green prompt (3s auto-dismiss)
- Operation failure: Red prompt + error explanation
- Loading state: Minimal spinner (deep blue)

---

## Layout Principles

### Spacing Strategy

**8px Grid System**

- All spacing is multiples of 8
- Ensures consistent visual rhythm
- Conveys professional sense of order

**Common Spacing:**

- Small spacing: 8px, 16px (related elements)
- Medium spacing: 24px, 32px (inside components)
- Large spacing: 48px, 64px (between modules)
- Page edges: 64px (desktop)

### Whitespace Principles

**Generous Whitespace, Conveying Stability**

- Page horizontal whitespace: 64px (desktop)
- Content max width: 1200px
- Module spacing: 48-64px
- Inside cards: 24-32px

**Why So Much Whitespace?**
- Conveys stability, unhurriedness
- Improves readability
- Matches high-end financial positioning
- Reduces visual pressure

### Content Max Width

- Dashboard: 1400px (data display)
- Tables: Full width (data dense)
- Articles: 800px (reading experience)
- Forms: 600px (focused)

---

## Component Design Decisions

### Buttons

#### Why 44px Height?

- Touch-friendly (44px is minimum mobile target)
- Works on desktop too (balanced)
- Matches financial product standards

#### Why 6-8px Border Radius?

- Small border-radius conveys professionalism
- More rigorous than Airbnb (8px)
- Avoids being too rounded (not stable)

#### Why Deep Blue Primary Button?

- Builds trust
- Professional, calm
- Distinguishes from entertainment products
- Industry convention

### Inputs

#### Why 44px Height?

- Consistent with button height
- Visual coordination and unity
- Easy input

#### Why Deep Blue Focus Glow?

- Clear state feedback
- Brand color reinforcement
- Soft visual effect
- Doesn't change border thickness (avoids layout jumping)

### Cards

#### Why 8px Border Radius?

- Consistent or slightly larger than buttons (6-8px)
- Creates container feel
- Maintains professional stability

#### Why Subtle Shadows?

- Doesn't compete with content
- Clear hierarchy
- Maintains restraint
- Avoids flashiness

### Data Tables

#### Why Zebra Striping?

- Improves readability
- Essential for data-dense scenarios
- Alternating row backgrounds (#FAFBFC / #FFFFFF)

#### Why Fixed Header?

- Long table experience
- Convenient data comparison
- Essential for financial products

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
--font-size-3xl: 40px;
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
/* Professional modern font */
--font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
--font-family-mono: 'JetBrains Mono', 'SF Mono', Consolas, monospace;
```

---

## Spacing System

```css
--space-1: 4px;
--space-2: 8px;
--space-3: 16px;
--space-4: 24px;
--space-5: 32px;
--space-6: 48px;
--space-8: 64px;
--space-10: 80px;
--space-12: 96px;
```

---

## Border Radius System

```css
--radius-sm: 4px;
--radius-md: 6px;
--radius-lg: 8px;
--radius-xl: 12px;
--radius-2xl: 16px;
--radius-full: 9999px;
```

---

## Shadows

```css
--shadow-sm: 0 1px 3px rgba(0, 0, 0, 0.12);
--shadow-md: 0 4px 6px rgba(0, 0, 0, 0.08);
--shadow-lg: 0 10px 20px rgba(0, 0, 0, 0.10);
--shadow-xl: 0 20px 40px rgba(0, 0, 0, 0.12);

/* Focus shadow */
--shadow-focus: 0 0 0 3px rgba(0, 82, 204, 0.2);
```

---

## Component Specifications

### Buttons

```css
.btn-primary {
  background: #0052CC;
  color: white;
  height: 44px;
  padding: 0 24px;
  border-radius: 6px;
  font-weight: 600;
  font-size: 16px;
  transition: all 0.15s ease-out;
}

.btn-primary:hover {
  background: #0065FF;
  box-shadow: 0 4px 12px rgba(0, 82, 204, 0.3);
}

.btn-secondary {
  background: #FFAB00;
  color: #172B4D;
  height: 44px;
  padding: 0 24px;
  border-radius: 6px;
  font-weight: 600;
}

.btn-secondary:hover {
  background: #FFC400;
  box-shadow: 0 4px 12px rgba(255, 171, 0, 0.3);
}

.btn-ghost {
  background: transparent;
  color: #0052CC;
  height: 44px;
  padding: 0 20px;
}

.btn-ghost:hover {
  background: #DEEBFF;
}

.btn-outline {
  background: transparent;
  color: #0052CC;
  border: 2px solid #0052CC;
  height: 44px;
  padding: 0 24px;
  border-radius: 6px;
  font-weight: 600;
}

.btn-outline:hover {
  background: #0052CC;
  color: white;
}
```

### Inputs

```css
.input {
  height: 44px;
  padding: 0 16px;
  border: 2px solid #DFE1E6;
  border-radius: 6px;
  font-size: 16px;
  background: white;
  transition: all 0.2s ease;
}

.input:focus {
  outline: none;
  border-color: #0052CC;
  box-shadow: 0 0 0 3px rgba(0, 82, 204, 0.1);
}

.input-error {
  border-color: #FF5630;
}

.input-error:focus {
  box-shadow: 0 0 0 3px rgba(255, 86, 48, 0.1);
}
```

### Cards

```css
.card {
  background: white;
  border: 1px solid #DFE1E6;
  border-radius: 8px;
  padding: 24px;
  transition: all 0.3s ease;
}

.card:hover {
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
}

.card-elevated {
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.08);
}

.card-header {
  border-bottom: 1px solid #DFE1E6;
  padding-bottom: 16px;
  margin-bottom: 16px;
}
```

### Data Tables

```css
.table {
  width: 100%;
  border-collapse: collapse;
}

.table th {
  background: #F4F5F7;
  padding: 12px 16px;
  text-align: left;
  font-weight: 600;
  color: #172B4D;
  border-bottom: 2px solid #DFE1E6;
}

.table td {
  padding: 12px 16px;
  border-bottom: 1px solid #DFE1E6;
}

.table tbody tr:hover {
  background: #F4F5F7;
}

.table-zebra tbody tr:nth-child(even) {
  background: #FAFBFC;
}
```

### Tags & Badges

```css
.tag {
  display: inline-flex;
  align-items: center;
  height: 28px;
  padding: 0 12px;
  background: #DEEBFF;
  color: #0052CC;
  border-radius: 4px;
  font-size: 12px;
  font-weight: 600;
}

.tag-success {
  background: #E3FCEF;
  color: #00875A;
}

.tag-warning {
  background: #FFFAE6;
  color: #FF991F;
}

.tag-error {
  background: #FFEBE6;
  color: #FF5630;
}

.tag-vip {
  background: linear-gradient(135deg, #FFAB00 0%, #FFC400 100%);
  color: #172B4D;
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

- **Restrained Animations:** 150-200ms transitions
- **Gentle Hover:** Background change, shadow enhancement
- **Focus Feedback:** Blue glow (3px)
- **Loading States:** Minimal spinner (deep blue)
- **Fade Effects:** Page transitions 300ms

---

## Application Scenarios

### Scenario 1: Fintech

**Core Applications:**

- Deep blue primary button ("Open Account Now", "Top Up")
- Gold accent elements (VIP indicators, profit highlights)
- Clear data display
- Professional form design

**Adjustments:**

- Strengthen data visualization
- Highlight security indicators
- Optimize mobile experience

### Scenario 2: Banking & Payments

**Core Applications:**

- Deep blue primary color conveys security
- Gold accents convey wealth
- Generous whitespace creates stability
- Restrained animations maintain professionalism

**Adjustments:**

- Strengthen security prompts
- Optimize payment flow
- Highlight account information

### Scenario 3: Insurance

**Core Applications:**

- Deep blue builds trust
- Clear plan comparisons
- Friendly form design
- Professional customer service entry

**Adjustments:**

- Add portrait photos (warmth)
- Emphasize coverage content
- Simplify application process

### Scenario 4: B2B SaaS

**Core Applications:**

- Deep blue professionalism
- Data display priority
- Clear functional navigation
- Efficient table interactions

**Adjustments:**

- Strengthen data visualization
- Optimize team collaboration features
- Highlight enterprise features

### Scenario 5: Investment & Wealth Management

**Core Applications:**

- Deep blue stability
- Gold wealth elements
- Clear profit display
- Professional chart analysis

**Adjustments:**

- Highlight profit data
- Green up/Red down (regional convention)
- Optimize investment experience

---

## Common Mistakes

### Common Errors

#### Error 1: Using Vivid Colors

- Wrong: Vivid red, orange, yellow
- Correct: Deep blue, gold and other restrained professional colors
- Reason: Loses trust, appears unprofessional

#### Error 2: Border Radius Too Large

- Wrong: 12px, 16px large border-radius
- Correct: 6-8px small border-radius
- Reason: Loses professionalism, appears insufficiently stable

#### Error 3: Too Many Animations

- Wrong: Flashy animations, bounce, rotation
- Correct: Restrained transitions (150-200ms)
- Reason: Loses professionalism, distracts attention

#### Error 4: Insufficient Whitespace

- Wrong: Dense layout, information overload
- Correct: Generous whitespace (48-64px spacing)
- Reason: Loses stability, reduces credibility

#### Error 5: Using Pure Black

- Wrong: #000000 pure black text
- Correct: #172B4D deep blue-black
- Reason: Too harsh, doesn't fit blue tone system

#### Error 6: Lacking Gold Accents

- Wrong: All deep blue, no secondary color
- Correct: Gold accents (wealth, VIP, success)
- Reason: Loses layering, cannot convey wealth attribute

### Negative Checklist

- Don't use vivid colors, use deep blue and gold
- Don't use large border-radius (> 8px), use small (6-8px)
- Don't use flashy animations, use restrained transitions
- Don't use dense layout, use generous whitespace
- Don't use pure black (#000000), use deep blue-black (#172B4D)
- Don't lack gold accents
- Don't over-decorate, maintain professional simplicity

---

## Best For

- Fintech
- Banking/Payments
- Insurance
- B2B SaaS
- Investment/Wealth Management
- Enterprise Services
- Data Analytics
- Professional Tools
