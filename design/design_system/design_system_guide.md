# Design System Documentation

## Overview

The Employee App Catalog design system provides a comprehensive foundation for creating consistent, accessible, and scalable user interfaces across the platform. Built on modern design principles, it balances enterprise professionalism with consumer-grade usability.

## Design Principles

### 1. Clarity & Simplicity
- **Clear Visual Hierarchy**: Use typography, spacing, and color to guide user attention
- **Minimal Cognitive Load**: Present information progressively and contextually
- **Scannable Content**: Design for quick scanning and task completion

### 2. Accessibility & Inclusion
- **WCAG 2.1 AA Compliance**: Meet or exceed accessibility standards
- **High Contrast Ratios**: Ensure readability for users with visual impairments
- **Keyboard Navigation**: Full functionality without mouse interaction
- **Screen Reader Support**: Semantic markup and proper ARIA labels

### 3. Enterprise Professionalism
- **Business-Appropriate Aesthetics**: Professional visual language
- **Data-Dense Interfaces**: Efficiently display complex enterprise information
- **Security Indicators**: Clear visual cues for security and compliance status

### 4. Progressive Enhancement
- **Mobile-First Design**: Core functionality optimized for mobile devices
- **Responsive Layouts**: Seamless experience across all screen sizes
- **Performance Optimization**: Fast loading and smooth interactions

## Typography

### Font Family
**Primary**: Inter
- Optimized for user interfaces and high legibility
- Excellent readability at small sizes
- Wide language support for international users

### Type Scale
```
Display Large:    48px / 3rem    (Hero headings)
Display Medium:   40px / 2.5rem  (Page titles)  
Display Small:    32px / 2rem    (Section headers)
Heading 1:        24px / 1.5rem  (Primary headings)
Heading 2:        20px / 1.25rem (Secondary headings)
Heading 3:        16px / 1rem    (Tertiary headings)
Body Large:       16px / 1rem    (Primary body text)
Body Medium:      14px / 0.875rem (Secondary body text)
Body Small:       12px / 0.75rem (Captions, labels)
```

### Font Weights
- **Regular (400)**: Body text, descriptions
- **Medium (500)**: Interface labels, secondary headings  
- **Semibold (600)**: Primary headings, buttons
- **Bold (700)**: Emphasis, alerts, key metrics

## Color System

### Primary Palette
```css
/* Primary Blues - Core brand and actions */
--color-primary-50:  #eff6ff;
--color-primary-100: #dbeafe;
--color-primary-200: #bfdbfe;
--color-primary-300: #93c5fd;
--color-primary-400: #60a5fa;
--color-primary-500: #3b82f6; /* Primary brand color */
--color-primary-600: #2563eb;
--color-primary-700: #1d4ed8;
--color-primary-800: #1e40af;
--color-primary-900: #1e3a8a;
```

### Neutral Palette
```css
/* Grays - Interface elements, text */
--color-neutral-50:  #f9fafb;
--color-neutral-100: #f3f4f6;
--color-neutral-200: #e5e7eb;
--color-neutral-300: #d1d5db;
--color-neutral-400: #9ca3af;
--color-neutral-500: #6b7280;
--color-neutral-600: #4b5563; /* Body text */
--color-neutral-700: #374151; /* Headings */
--color-neutral-800: #1f2937;
--color-neutral-900: #111827;
```

### Semantic Colors
```css
/* Success - Approvals, positive states */
--color-success-50:  #f0fdf4;
--color-success-500: #22c55e;
--color-success-600: #16a34a;

/* Warning - Pending, caution states */
--color-warning-50:  #fffbeb;
--color-warning-500: #f59e0b;
--color-warning-600: #d97706;

/* Error - Rejections, error states */
--color-error-50:   #fef2f2;
--color-error-500:  #ef4444;
--color-error-600:  #dc2626;

/* Info - Information, neutral alerts */
--color-info-50:   #eff6ff;
--color-info-500:  #3b82f6;
--color-info-600:  #2563eb;
```

## Layout System

### Grid & Spacing
**Base Unit**: 4px (0.25rem)
**Grid System**: 12-column responsive grid with flexible gutters

```css
/* Spacing Scale (based on 4px unit) */
--spacing-1:  4px;   /* 0.25rem */
--spacing-2:  8px;   /* 0.5rem */
--spacing-3:  12px;  /* 0.75rem */
--spacing-4:  16px;  /* 1rem */
--spacing-5:  20px;  /* 1.25rem */
--spacing-6:  24px;  /* 1.5rem */
--spacing-8:  32px;  /* 2rem */
--spacing-10: 40px;  /* 2.5rem */
--spacing-12: 48px;  /* 3rem */
--spacing-16: 64px;  /* 4rem */
--spacing-20: 80px;  /* 5rem */
--spacing-24: 96px;  /* 6rem */
```

### Breakpoints
```css
/* Mobile First Responsive Breakpoints */
--breakpoint-sm: 640px;   /* Small devices */
--breakpoint-md: 768px;   /* Medium devices */  
--breakpoint-lg: 1024px;  /* Large devices */
--breakpoint-xl: 1280px;  /* Extra large devices */
--breakpoint-2xl: 1536px; /* Ultra wide displays */
```

### Container Widths
```css
--container-sm:  640px;
--container-md:  768px;
--container-lg:  1024px;
--container-xl:  1280px;
--container-2xl: 1536px;
```

## Component Library

### Buttons

#### Primary Button
```css
.btn-primary {
  background: var(--color-primary-600);
  color: white;
  border: none;
  padding: 12px 24px;
  border-radius: 8px;
  font-weight: 500;
  transition: all 0.2s ease;
}

.btn-primary:hover {
  background: var(--color-primary-700);
  box-shadow: 0 4px 12px rgba(59, 130, 246, 0.4);
}
```

#### Secondary Button
```css
.btn-secondary {
  background: transparent;
  color: var(--color-primary-600);
  border: 1px solid var(--color-primary-600);
  padding: 12px 24px;
  border-radius: 8px;
  font-weight: 500;
  transition: all 0.2s ease;
}

.btn-secondary:hover {
  background: var(--color-primary-50);
}
```

### Form Elements

#### Input Fields
```css
.form-input {
  border: 1px solid var(--color-neutral-300);
  border-radius: 8px;
  padding: 12px 16px;
  font-size: 16px;
  background: white;
  transition: border-color 0.2s ease;
}

.form-input:focus {
  border-color: var(--color-primary-500);
  box-shadow: 0 0 0 3px rgba(59, 130, 246, 0.1);
  outline: none;
}
```

### Cards & Containers

#### App Card
```css
.app-card {
  background: white;
  border: 1px solid var(--color-neutral-200);
  border-radius: 12px;
  padding: 24px;
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.1);
  transition: all 0.2s ease;
}

.app-card:hover {
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15);
  border-color: var(--color-neutral-300);
}
```

### Navigation

#### Tab Navigation
```css
.tab-nav {
  border-bottom: 1px solid var(--color-neutral-200);
  display: flex;
  gap: 32px;
}

.tab-item {
  padding: 12px 0;
  color: var(--color-neutral-500);
  border-bottom: 2px solid transparent;
  transition: all 0.2s ease;
}

.tab-item.active {
  color: var(--color-primary-600);
  border-bottom-color: var(--color-primary-600);
}
```

## Icons & Imagery

### Icon System
**Icon Library**: Heroicons (outline and solid variants)
**Standard Sizes**: 16px, 20px, 24px, 32px
**Color**: Inherit from parent or semantic colors

### App Icons
- **Size**: 48px × 48px standard, 64px × 64px for featured
- **Format**: SVG preferred, PNG fallback
- **Style**: Rounded corners (8px radius)
- **Background**: White or brand-appropriate color

### Screenshots
- **Aspect Ratio**: 16:9 for consistency
- **Resolution**: Minimum 1280×720, optimized for web
- **Compression**: WebP format with PNG fallback

## States & Interactions

### Interactive States
```css
/* Default state */
.interactive-element {
  transition: all 0.2s ease;
}

/* Hover state */
.interactive-element:hover {
  transform: translateY(-1px);
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15);
}

/* Focus state (accessibility) */
.interactive-element:focus {
  outline: 2px solid var(--color-primary-500);
  outline-offset: 2px;
}

/* Active state */
.interactive-element:active {
  transform: translateY(0);
}
```

### Loading States
```css
.loading-skeleton {
  background: linear-gradient(90deg, #f0f0f0 25%, #e0e0e0 50%, #f0f0f0 75%);
  background-size: 200% 100%;
  animation: loading 1.5s infinite;
}

@keyframes loading {
  0% { background-position: 200% 0; }
  100% { background-position: -200% 0; }
}
```

## Accessibility Guidelines

### Color Contrast
- **Normal text**: Minimum 4.5:1 contrast ratio
- **Large text**: Minimum 3:1 contrast ratio
- **Interactive elements**: Minimum 3:1 contrast ratio

### Focus Management
- **Visible focus indicators**: 2px solid outline
- **Logical tab order**: Sequential navigation
- **Skip links**: Allow keyboard users to skip repetitive content

### Screen Reader Support
```html
<!-- Semantic markup example -->
<button aria-label="Request access to Figma" aria-describedby="app-description">
  Request Access
</button>
<p id="app-description">Professional design and prototyping tool</p>
```

## Implementation Guidelines

### CSS Architecture
**Methodology**: BEM (Block Element Modifier)
**Preprocessor**: Sass/SCSS
**CSS-in-JS**: Styled-components for React components

### Component Development
```jsx
// Example React component with design system
import { Button, Card, Text } from '@/design-system';

const AppCard = ({ app, onRequest }) => (
  <Card variant="elevated" padding="lg">
    <Text variant="heading-3">{app.name}</Text>
    <Text variant="body" color="neutral-600">{app.description}</Text>
    <Button variant="primary" onClick={() => onRequest(app)}>
      Request Access
    </Button>
  </Card>
);
```

### Performance Considerations
- **Critical CSS**: Inline critical styles for above-the-fold content
- **Font Loading**: Use font-display: swap for web fonts
- **Image Optimization**: Responsive images with appropriate formats
- **Component Lazy Loading**: Load non-critical components on demand

## Quality Assurance

### Design Tokens
Maintain consistency through centralized design tokens:
```json
{
  "color": {
    "primary": {
      "500": "#3b82f6",
      "600": "#2563eb"
    }
  },
  "spacing": {
    "4": "16px",
    "6": "24px"
  },
  "typography": {
    "heading-1": {
      "fontSize": "24px",
      "fontWeight": "600"
    }
  }
}
```

### Testing Checklist
- [ ] Visual regression testing across browsers
- [ ] Accessibility audit with automated tools
- [ ] Manual keyboard navigation testing
- [ ] Screen reader compatibility verification
- [ ] Performance benchmarking
- [ ] Mobile device testing
- [ ] Cross-browser compatibility validation

This design system provides the foundation for creating cohesive, accessible, and maintainable user interfaces that meet enterprise requirements while delivering exceptional user experiences.