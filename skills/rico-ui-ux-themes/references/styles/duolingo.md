# Duolingo Style

Playful, Gamified, Friendly, Vibrant, Fun

---

## Design Philosophy

### Brand Philosophy

**"Learning Through Play"**

Duolingo's design philosophy makes learning fun through gamification. Design conveys a friendly, playful, and energetic brand image through high saturation colors, rounded shapes, and fun animations, eliminating the boredom of learning.

### Design Philosophy

1. **Gamification - Make Learning Fun**
   - Progress bars, achievements, streak systems
   - Cartoon mascot Duo
   - Instant feedback and rewards

2. **High Saturation Colors - Attract Attention**
   - Bright and vivid green
   - Colorful accent colors
   - Visual stimulation, enhances memory

3. **Large Border Radius - Friendly and Approachable**
   - 16px border-radius buttons
   - No sharp corners
   - Reduces learning pressure

4. **Fun Animations - Interactive Feedback**
   - Bounce, zoom, rotation
   - Celebration animations
   - Makes operations enjoyable

### Core Keywords

- Playful
- Gamified
- Friendly
- Vibrant
- Fun

---

## Overview

Duolingo style originates from the Duolingo language learning platform—playful, friendly, gamified. Suitable for educational products, learning tools, and gamified applications.

---

## Color System

### Brand Color

```css
--color-primary: #58CC02;       /* Duolingo Green */
--color-primary-hover: #46A302;
--color-primary-dark: #3EA801;
```

#### Usage Guidelines

**When to Use:**

- Primary buttons ("Start Learning")
- Progress bars
- Success states
- Correct answer feedback
- Mascot Duo

**Avoid Using:**

- Large area backgrounds (too harsh)
- Text color (not enough contrast)
- Error prompts

**Usage Principle:** Moderate, about 15-20% of page area

**Why High Saturation Green?**
- Brand identity: Duo is a green owl
- Positive association: Green = correct, success
- Attracts attention: High saturation is more eye-catching
- Distinction: Stands out on white background

### Accent Colors

```css
--color-accent-blue: #1CB0F6;   /* Blue */
--color-accent-purple: #A928E8;  /* Purple */
--color-accent-red: #FF4B4B;     /* Red */
--color-accent-yellow: #FFC800;  /* Yellow */
--color-accent-orange: #FF9600;  /* Orange */
--color-accent-pink: #FF8FB1;   /* Pink */
```

#### Colorful Usage Guidelines

**Functional and Emotional Colors Combined:**

- Blue: Neutral, information
- Purple: Magic, special
- Red: Error, failure, heart
- Yellow: Achievement, stars
- Orange: Warning, streak
- Pink: Fun, decoration

**Use Cases:**
- Course categories (colorful cards)
- Achievement badges
- Streak flames (orange)
- Progress indicators (colorful)

**Why So Many Colors?**
- Gamification needs rich visuals
- Distinguish different course types
- Increase fun
- Reduce learning pressure

---

## Interaction Philosophy

### Animation Principles

**Fun, Feedback, Celebration**

#### Button Feedback

- Hover: Slight zoom (scale 1.05)
- Click: Press effect (scale 0.95)
- Bounce: Important buttons have bounce animation

#### Answer Feedback

- Correct: Green checkmark + bounce + sound effect
- Wrong: Red X + shake
- Streak: Flame animation + particle effects

#### Celebration Animations

- Complete lesson: Confetti
- Level up: Glow effect
- Achievement: Badge popup

#### Transition Duration

- Fast: 150ms (buttons)
- Normal: 200ms (panels)
- Slow: 300ms (celebration animations)

**Why Emphasize Animations?**
- Increases fun
- Instant feedback reinforces learning
- Reduces boredom
- Gamified experience

### Feedback Mechanisms

**Instant, Fun, Encouraging**

- Operation success: Green + bounce
- Operation failure: Red + shake
- Progress update: Progress bar animation
- Streak reward: Flame + number

---

## Layout Principles

### Spacing Strategy

**Generous but Not Wasteful**

**Standard Spacing:**

- Minimum: 8px
- Small spacing: 12px, 16px
- Medium spacing: 24px, 32px
- Large spacing: 48px, 64px

**Why Larger than Linear?**
- Educational products need breathing room
- Reduces visual pressure
- Suitable for long learning sessions

### Border Radius System

**Super Rounded**

- Buttons: 16px (larger than other styles)
- Cards: 16-20px
- Inputs: 12px
- Small elements: 8px

**Why Such Large Border Radius?**
- Friendly and approachable
- Reduces learning pressure
- Gamified feel
- Distinguishes from serious tools

### Content Max Width

- Learning content: 600px (focused)
- Course list: 900px
- Mobile: Full width

---

## Component Design Decisions

### Buttons

#### Why 16px Border Radius?

- Twice as large as Airbnb (8px)
- Nearly circular, super friendly
- Reduces seriousness
- Increases fun

#### Why High Saturation Green?

- Brand identity
- Positive association (correct, success)
- Eye-catching on white background
- Gamification element

#### Why Bounce on Click?

- Increases fun
- Instant feedback
- Gamified experience
- Makes operations enjoyable

### Progress Bars

#### Why So Prominent?

- Learning progress visualization
- Gamification element
- Motivates users to continue
- Instant feedback

**Design Features:**
- High saturation green
- Rounded ends (16px)
- Animated updates

### Cards/Courses

#### Why Colorful Cards?

- Visually distinguish course types
- Increases fun
- Reduces learning pressure
- Gamified feel

**Color Usage:**
- Language courses: Green
- Math courses: Blue
- Music courses: Purple
- And so on...

---

## Application Scenarios

### Scenario 1: Language Learning App

**Core Applications:**

- High saturation green primary button
- Rounded buttons (16px)
- Colorful course cards
- Progress bars and achievement system

**Adjustments:**

- Emphasize gamification elements
- Use mascot Duo
- Streak and consecutive day systems

### Scenario 2: Educational Platform

**Core Applications:**

- Course categories (colorful cards)
- Learning path visualization
- Achievement badge system
- Progress tracking

**Adjustments:**

- Add social elements
- Leaderboards
- Study groups

### Scenario 3: Kids Learning App

**Core Applications:**

- Super large border-radius (16-20px)
- Cartoon icons
- Simplified interface
- Sound feedback

**Adjustments:**

- Larger font sizes (16-18px)
- Larger touch targets (48px+)
- Voice guidance

### Scenario 4: Skills Training

**Core Applications:**

- Gamified learning
- Progress visualization
- Achievement system
- Instant feedback

**Adjustments:**

- Lower color saturation (for adults)
- Reduce playful elements
- Maintain gamification core

### Scenario 5: Mobile Learning

**Key Adjustments:**

- Buttons: 44px (touch-friendly)
- Spacing: Relatively compact
- Bottom navigation
- Gesture operations

**Keep Unchanged:**

- High saturation colors
- Super large border-radius
- Fun animations

---

## Common Mistakes

### Common Errors

#### Error 1: Using Low Saturation Colors

- Wrong: Soft green, gray tones
- Correct: High saturation green (#58CC02)
- Reason: Loses vitality, doesn't look like Duolingo

#### Error 2: Border Radius Too Small

- Wrong: 4px, 8px border-radius
- Correct: 16px, 20px super large border-radius
- Reason: Loses friendliness, too serious

#### Error 3: Missing Fun Elements

- Wrong: Minimal, no decoration
- Correct: Mascot, celebration animations, colorful cards
- Reason: Loses gamification character

#### Error 4: Too Few Animations

- Wrong: Fast transitions, no feedback
- Correct: Bounce, zoom, celebration animations
- Reason: Loses fun and instant feedback

#### Error 5: Using Pure Black and White

- Wrong: Black text, white background
- Correct: Deep brown-gray (#1A1A1A), light gray background
- Reason: Too high contrast, not friendly enough

#### Error 6: Missing Gamification Elements

- Wrong: Regular learning tool
- Correct: Progress bars, achievements, streaks, leaderboards
- Reason: Loses Duolingo's core character

### Negative Checklist

- Don't use low saturation colors, use high saturation colorful
- Don't use small border-radius (< 12px), use super large (16-20px)
- Don't remove fun elements, maintain gamification
- Don't reduce animations, increase fun feedback
- Don't use pure black and white, use soft deep brown-gray
- Don't make serious design, stay playful and friendly
- Don't skip celebration, add achievements and rewards

---

## Visual Design Specifications

### Color System

#### Brand Color

```css
--color-primary: #58CC02;       /* Duolingo Green */
--color-primary-hover: #46A302;
--color-primary-dark: #3EA801;
```

#### Accent Colors

```css
--color-accent-blue: #1CB0F6;   /* Blue */
--color-accent-purple: #A928E8;  /* Purple */
--color-accent-red: #FF4B4B;     /* Red */
--color-accent-yellow: #FFC800;  /* Yellow */
--color-accent-orange: #FF9600;  /* Orange */
--color-accent-pink: #FF8FB1;   /* Pink */
```

#### Background Colors

```css
/* Light mode */
--color-bg: #FFFFFF;
--color-bg-secondary: #F7F7F7;
--color-bg-tertiary: #EFEFEF;
--color-bg-elevated: #FFFFFF;

/* Dark mode */
--color-bg-dark: #1A1A1A;
--color-bg-secondary-dark: #2D2D2D;
```

#### Text Colors

```css
/* Light mode */
--color-text: #1A1A1A;
--color-text-secondary: #4B4B4B;
--color-text-tertiary: #8B8B8B;
--color-text-disabled: #BDBDBD;

/* Dark mode */
--color-text-dark: #FFFFFF;
--color-text-secondary-dark: #B0B0B0;
```

#### Border Colors

```css
--color-border: #E5E5E5;
--color-border-dark: #4B4B4B;
```

#### Functional Colors

```css
--color-success: #58CC02;
--color-warning: #FFC800;
--color-error: #FF4B4B;
--color-info: #1CB0F6;
```

---

### Typography System

#### Font Family

```css
/* Duolingo uses custom font */
--font-family: 'Duolingo', 'Nunito', -apple-system, BlinkMacSystemFont, sans-serif;

/* Fallback font stack */
--font-family-fallback: 'Nunito', -apple-system, BlinkMacSystemFont, sans-serif;
```

#### Font Size Scale

```css
--font-size-h1: 48px;      /* Hero title */
--font-size-h2: 32px;      /* Section title */
--font-size-h3: 24px;      /* Subtitle */
--font-size-h4: 20px;      /* Card title */
--font-size-body: 16px;     /* Body text */
--font-size-sm: 14px;      /* Small text */
--font-size-xs: 12px;      /* Labels */
```

#### Line Height

```css
--line-height-tight: 1.2;
--line-height-normal: 1.4;
--line-height-relaxed: 1.6;
```

#### Font Weights

```css
--font-weight-bold: 700;
--font-weight-semibold: 600;
--font-weight-medium: 500;
--font-weight-normal: 400;
```

#### Text Alignment

```css
--text-align-left: left;
--text-align-center: center;
--text-align-right: right;
```

---

### Grid and Spacing

#### Base Grid

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
```

#### Component Sizes

```css
--btn-height-sm: 32px;
--btn-height-base: 40px;
--btn-height-lg: 48px;

--input-height: 40px;

--icon-size-sm: 16px;
--icon-size-md: 24px;
--icon-size-lg: 32px;
```

---

### Border Radius and Shadows

#### Border Radius

```css
--radius-sm: 4px;
--radius-md: 8px;
--radius-lg: 12px;
--radius-xl: 16px;
--radius-2xl: 24px;
--radius-full: 9999px;
```

#### Shadows

```css
/* Duolingo style: Soft but layered */
--shadow-sm: 0 1px 2px rgba(0, 0, 0, 0.05);
--shadow-md: 0 2px 4px rgba(0, 0, 0, 0.1);
--shadow-lg: 0 4px 8px rgba(0, 0, 0, 0.15);
--shadow-xl: 0 8px 16px rgba(0, 0, 0, 0.2);
```

---

### Icon and Visual Element Style

```css
/* Cartoon style icons */
--icon-style: cartoon;

/* Stroke width */
--icon-stroke: 2px;

/* Rounded */
--icon-stroke-linecap: round;
--icon-stroke-linejoin: round;
```

---

### Animation Rules

#### Parameters

```css
--duration-fast: 100ms;
--duration-normal: 200ms;
--duration-slow: 300ms;

/* Duolingo uses elastic easing */
--ease-elastic: cubic-bezier(0.68, -0.55, 0.265, 1.55);
--ease-bounce: cubic-bezier(0.34, 1.56, 0.64, 1);
--ease-out: cubic-bezier(0.16, 1, 0.3, 1);
```

#### Allowed Animations

- Button click bounce effect
- Achievement unlock animation
- Progress bar animation
- Character expression changes

#### Forbidden Animations

- Overly complex 3D effects
- Long loading animations
- Flashing effects

---

### Responsive Breakpoints

```css
--breakpoint-sm: 640px;
--breakpoint-md: 768px;
--breakpoint-lg: 1024px;
--breakpoint-xl: 1280px;
```

#### Adaptation Rules

| Device | Breakpoint | Layout |
|--------|-----------|--------|
| Mobile | <768px | Single column, bottom navigation |
| Tablet | 768-1024px | Two columns optional |
| Desktop | >=1024px | Multiple columns, top navigation |

---

## Page Structure and UI Component Specifications

### Overall Layout Structure

- Top navigation + main content
- Bottom fixed navigation (mobile)
- Card-style content display

### Buttons

```css
.btn-primary {
  background: #58CC02;
  color: white;
  height: 48px;
  padding: 0 24px;
  border-radius: 12px;
  font-weight: 700;
  font-size: 16px;
  box-shadow: 0 4px 0 #46A302;
}

.btn-primary:active {
  transform: translateY(4px);
  box-shadow: 0 0 0 #46A302;
}

.btn-secondary {
  background: transparent;
  border: 2px solid #58CC02;
  color: #58CC02;
}

.btn-ghost {
  background: transparent;
  color: #4B4B4B;
}
```

### Cards

```css
.card {
  background: white;
  border: 2px solid #E5E5E5;
  border-radius: 16px;
  padding: 20px;
}

.card-elevated {
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}
```

### Inputs

```css
.input {
  height: 48px;
  padding: 0 16px;
  border: 2px solid #E5E5E5;
  border-radius: 12px;
  font-size: 16px;
}

.input:focus {
  border-color: #58CC02;
  outline: none;
}

.input-error {
  border-color: #FF4B4B;
}
```

### Navigation

```css
/* Top navigation */
.nav {
  height: 60px;
  background: white;
  border-bottom: 1px solid #E5E5E5;
}

/* Bottom navigation */
.nav-bottom {
  height: 64px;
  background: white;
  border-top: 1px solid #E5E5E5;
  position: fixed;
  bottom: 0;
}
```

---

## Design Execution Rules

### Design Decision Principles

1. **Fun First:** Design should make users feel happy and entertained
2. **High Contrast:** Ensure readability and accessibility
3. **Gamification Elements:** Progress, achievements, motivation
4. **Simple and Clear:** Not complex interactions

### Prohibited Items

- Using dull colors
- Overly professional business style
- Complex multi-layer shadows
- Long loading animations
- Overuse of gradients

---

## Implementation Guide

### For Frontend Engineers

1. **Color Usage:** Primary color #58CC02 for main CTAs, other colors only for specific functions
2. **Buttons:** Must have press effect (translateY + shadow change)
3. **Border Radius:** Consistently use 12px-16px large border-radius
4. **Animation:** Can appropriately use elastic effects to increase fun

### For Designers

1. **Stay Playful:** Don't use overly business-like colors
2. **Large and Clear:** Text and buttons should be large enough
3. **Gamification:** Consider adding progress, achievements, and other elements
4. **Consistency:** All buttons and cards use the same border-radius standard

---

## Best For

- Educational products
- Kids apps
- Gamified products
- Fun tools
