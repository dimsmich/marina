# Jetox Education - UI Component Catalog
**Extracted from:** https://education.jetox.ae/home
**Date:** 2025-10-17

---

## Component Architecture Overview

### CSS Naming Convention
- **Base Prefix:** `.learnworlds-` or `.lw-`
- **Component Pattern:** `[prefix]-[component]-[variant]-[modifier]`
- **State Classes:** `.js-` prefix for JavaScript-enhanced elements
- **Responsive Suffixes:** `-tp`, `-tl`, `-sl`, `-sp`

---

## 1. Navigation Components

### 1.1 Topbar (Header Navigation)

#### Component Structure
```html
<section class="js-learnworlds-section learnworlds-section lw-topbar 
                lw-body-bg stretched-bg js-change-image-node 
                transparent-onStart sticky-topbar">
  <div class="lw-h-row js-same-content-wrapper">
    <div class="learnworlds-section-content js-learnworlds-section-content wide">
      <!-- Logo, Menu, Actions -->
    </div>
  </div>
</section>
```

#### CSS Classes
| Class | Purpose |
|-------|---------|
| `.lw-topbar` | Main navigation bar container |
| `.sticky-topbar` | Enables sticky scroll behavior |
| `.transparent-onStart` | Transparent until scroll |
| `.stretched-bg` | Full-width background |
| `.lw-body-bg` | Applies body background color |

#### Responsive Behavior
- **Desktop:** Full horizontal menu with logo, links, and CTA
- **Tablet/Mobile:** Logo + hamburger menu icon
- **Hidden Classes:** `.hide-tp`, `.hide-sl`, `.hide-sp`

---

### 1.2 Logo Component

#### HTML Structure
```html
<div class="lw-topbar-logo-col col flex-item">
  <div class="lw-topbar-logo-wrapper flex-item va-c">
    <a class="js-linked-node">
      <div class="learnworlds-element lw-logo js-change-image-node cursor-pointer">
        <!-- Logo Image -->
      </div>
    </a>
  </div>
</div>
```

#### Properties
- **Position:** Left-aligned in topbar
- **Cursor:** Pointer (clickable)
- **Vertical Alignment:** Center (`.va-c`)
- **Responsive:** May scale down on mobile

---

### 1.3 Navigation Menu

#### HTML Structure
```html
<div class="lw-topbar-menu-wrapper flexible-cnt-wrapper js-lw-flexible-wrapper">
  <nav class="lw-topbar-menu with-hover">
    <div class="lw-topbar-options">
      <div class="lw-topbar-option">
        <a class="lw-topbar-option-link learnworlds-main-text-normal 
                  js-menu-item lw-brand-text text-only js-linked-node">
          <span class="lw-topbar-option-link-lbl nowrap">Home</span>
        </a>
      </div>
      <!-- Repeat for Courses, About Us -->
    </div>
  </nav>
</div>
```

#### Link Variants
| Variant | Classes | Appearance |
|---------|---------|------------|
| Text Link | `.text-only .lw-brand-text` | Plain text, navy color |
| Button Link | `.button-like .learnworlds-button-solid-brand` | Solid button styling |

#### States
- **Default:** Navy blue text (#011E41)
- **Hover:** `.with-hover` class enables hover effects
- **Active:** Current page indicator
- **NoWrap:** `.nowrap` prevents text wrapping

---

### 1.4 Hamburger Menu (Mobile)

#### HTML Structure
```html
<div class="js-lw-topbar-hamburger-wrapper js-component bgcolor-inherit">
  <!-- Hamburger icon and slide-out menu -->
</div>
```

#### Behavior
- **Trigger:** Click/tap hamburger icon
- **Action:** Opens slide-out navigation panel
- **Content:** All navigation links stacked vertically

---

## 2. Hero Section Components

### 2.1 Hero Container

#### HTML Structure
```html
<section class="js-learnworlds-section learnworlds-section 
                lw-body-bg stretched-bg learnworlds-size-normal 
                learnworlds-align-left js-change-image-node">
  <div class="js-video-wrapper">
    <!-- Background video/image -->
  </div>
  <div class="learnworlds-section-overlay lw-dark-bg js-learnworlds-overlay"></div>
  <div class="learnworlds-section-content js-learnworlds-section-content wide">
    <!-- Hero content -->
  </div>
</section>
```

#### Size Variants
| Variant | Class | Padding |
|---------|-------|---------|
| Small | `.learnworlds-size-small` | 40px |
| Normal | `.learnworlds-size-normal` | 80px |
| Large | `.learnworlds-size-large` | 120px |
| Extra Large | `.learnworlds-size-extra-large` | 160px |

#### Alignment Options
- `.learnworlds-align-left` - Left-aligned content
- `.learnworlds-align-center` - Center-aligned content
- `.learnworlds-align-right` - Right-aligned content

---

### 2.2 Hero Grid Layout

#### HTML Structure
```html
<div class="lw-cols one-row one-row-tl multiple-rows-tp 
            multiple-rows-sl multiple-rows-sp main js-same-content-wrapper">
  <!-- Left Column (6/12 on desktop, 12/12 on mobile) -->
  <div class="col span_6_of_12 span_6_of_12-tl span_12_of_12-tp 
              mb-4rem-tp span_12_of_12-sl mb-4rem-sl span_12_of_12-sp mb-4rem-sp">
    <!-- Heading, text, CTA -->
  </div>
  <!-- Right Column -->
  <div class="col span_6_of_12 span_6_of_12-tl span_12_of_12-tp">
    <!-- Image or supporting content -->
  </div>
</div>
```

#### Grid Span Classes
| Class | Meaning |
|-------|---------|
| `.span_6_of_12` | 50% width (6 of 12 columns) |
| `.span_12_of_12-tp` | Full width on tablet portrait |
| `.mb-4rem-tp` | 4rem bottom margin on tablet portrait |

#### Row Behavior
- `.one-row` - Single row on desktop
- `.multiple-rows-tp` - Multiple rows (stacked) on tablet portrait
- `.multiple-rows-sl` - Multiple rows on smartphone landscape
- `.multiple-rows-sp` - Multiple rows on smartphone portrait

---

### 2.3 Hero Heading

#### HTML Structure
```html
<h2 class="learnworlds-heading learnworlds-heading-normal learnworlds-element">
  Your Heading Text
</h2>
```

#### Heading Variants
| Class | Font Size | Use Case |
|-------|-----------|----------|
| `.learnworlds-heading-large` | 50px | Main hero title |
| `.learnworlds-heading-normal` | 46px | Standard hero |
| `.learnworlds-heading-small` | 42px | Compact hero |

#### Properties
- **Font:** Forum, bold (700)
- **Color:** Dark navy (#011E41) or white (on dark backgrounds)
- **Line Height:** 1.2
- **Responsive:** Scales down on smaller screens

---

### 2.4 Hero Body Text

#### HTML Structure
```html
<p class="learnworlds-main-text learnworlds-element 
          learnworlds-main-text-normal lw-text-color-fadeout20">
  Your descriptive text here.
</p>
```

#### Text Variants
| Class | Font Size | Use Case |
|-------|-----------|----------|
| `.learnworlds-main-text-huge` | 32px | Extra emphasis |
| `.learnworlds-main-text-very-large` | 26px | Large body |
| `.learnworlds-main-text-large` | 26px | Large readable |
| `.learnworlds-main-text-normal` | 24px | Standard body |
| `.learnworlds-main-text-small` | 18px | Compact text |

#### Color Modifiers
- `.lw-text-color-fadeout20` - 80% opacity (20% fade)
- `.lw-brand-text` - Brand navy color
- `.lw-light-text` - Light/white color

---

### 2.5 Hero CTA Button

#### HTML Structure
```html
<div class="learnworlds-button-wrapper lw-content-block learnworlds-element">
  <a class="learnworlds-button learnworlds-element 
            learnworlds-button-normal learnworlds-button-rounded 
            learnworlds-button-solid-brand">
    Button Text
  </a>
</div>
```

#### Button Size Classes
| Class | Font Size | Padding |
|-------|-----------|---------|
| `.learnworlds-button-large` | 24px | 16px/32px |
| `.learnworlds-button-normal` | 18px | 12px/24px |
| `.learnworlds-button-small` | 16px | 10px/20px |

#### Button Style Classes
| Class | Appearance |
|-------|------------|
| `.learnworlds-button-solid-brand` | Warm brown background, white text |
| `.learnworlds-button-outline-brand` | Navy border, navy text |
| `.learnworlds-button-rounded` | Enhanced border radius |

---

## 3. Content Section Components

### 3.1 Section Container

#### HTML Structure
```html
<section class="js-learnworlds-section learnworlds-section 
                [size-class] [alignment-class] [background-class]">
  <div class="learnworlds-section-content js-learnworlds-section-content [width-class]">
    <!-- Content -->
  </div>
</section>
```

#### Width Classes
- `.wide` - Full-width content (with padding)
- `.narrow` - Constrained width (centered)
- `.full` - Absolute full-width (no padding)

---

### 3.2 Video Background

#### HTML Structure
```html
<div class="js-video-wrapper">
  <video autoplay loop muted playsinline>
    <source src="video.mp4" type="video/mp4">
  </video>
</div>
<div class="learnworlds-section-overlay lw-dark-bg js-learnworlds-overlay"></div>
```

#### Overlay Variants
- `.lw-dark-bg` - Dark overlay (rgba(1, 30, 65, 0.6))
- `.lw-light-bg` - Light overlay (rgba(231, 230, 226, 0.8))

---

## 4. Utility Components

### 4.1 Flexbox Utilities

#### Classes
| Class | Purpose |
|-------|---------|
| `.flex-item` | Flex child item |
| `.flex-none` | No flex grow/shrink |
| `.flex-1` | Flex grow: 1 |
| `.with-flexible-parts` | Contains flexible children |
| `.ai-s` | Align items start |
| `.va-c` | Vertical align center |
| `.justify-content-flex-start` | Justify start |
| `.justify-content-flex-end` | Justify end |
| `.learnworlds-align-center` | Center alignment |
| `.learnworlds-align-right` | Right alignment |

---

### 4.2 Spacing Utilities

#### Classes
| Class | Purpose |
|-------|---------|
| `.mb-4rem-tp` | Margin bottom 4rem (tablet portrait) |
| `.mb-4rem-sl` | Margin bottom 4rem (smartphone landscape) |
| `.mb-4rem-sp` | Margin bottom 4rem (smartphone portrait) |

---

### 4.3 Content Block Utilities

#### Classes
| Class | Purpose |
|-------|---------|
| `.lw-content-block` | Standard content spacing |
| `.js-same-content-wrapper` | Group related content |
| `.js-same-content-child` | Child of grouped content |
| `.learnworlds-element` | Base element class |

---

## 5. Interactive Elements

### 5.1 JavaScript-Enhanced Classes

#### Classes
| Class | Purpose |
|-------|---------|
| `.js-learnworlds-section` | Section with JS behavior |
| `.js-change-image-node` | Lazy loading/image swapping |
| `.js-linked-node` | Clickable element |
| `.js-component` | Generic JS component |
| `.js-menu-item` | Navigation item handler |
| `.js-lw-flexible-wrapper` | Flexible layout JS |
| `.js-same-content-wrapper` | Content synchronization |
| `.js-video-wrapper` | Video player control |
| `.js-learnworlds-overlay` | Overlay control |

---

### 5.2 Cursor & Interaction

#### Classes
| Class | Purpose |
|-------|---------|
| `.cursor-pointer` | Clickable cursor |
| `.with-hover` | Hover effects enabled |
| `.nowrap` | No text wrapping |

---

## 6. Responsive Components

### 6.1 Visibility Classes

#### Hide on Specific Devices
| Class | Hides On |
|-------|----------|
| `.hide-tp` | Tablet portrait |
| `.hide-tl` | Tablet landscape |
| `.hide-sl` | Smartphone landscape |
| `.hide-sp` | Smartphone portrait |

---

### 6.2 Responsive Grid Classes

#### Column Spans
```
.span_[n]_of_12          - Desktop (n columns out of 12)
.span_[n]_of_12-tl       - Tablet landscape
.span_[n]_of_12-tp       - Tablet portrait
.span_[n]_of_12-sl       - Smartphone landscape
.span_[n]_of_12-sp       - Smartphone portrait
```

#### Common Patterns
- **50/50 Split → Full:** `.span_6_of_12 .span_12_of_12-tp`
- **33/33/33 → Full:** `.span_4_of_12 .span_12_of_12-tp`
- **25/75 Split:** `.span_3_of_12 .span_9_of_12`

---

## 7. Background & Overlay Components

### 7.1 Background Classes

#### Classes
| Class | Purpose |
|-------|---------|
| `.lw-body-bg` | Body background color |
| `.lw-brand-bg` | Brand color background |
| `.lw-dark-bg` | Dark background/overlay |
| `.stretched-bg` | Full-width stretched background |

---

### 7.2 Image Node Classes

#### Classes
| Class | Purpose |
|-------|---------|
| `.js-change-image-node` | Responsive image loading |
| `.lw-logo` | Logo image component |

---

## 8. Component Composition Patterns

### Pattern 1: Hero with Two-Column Layout
```html
<section class="learnworlds-section learnworlds-size-normal">
  <div class="learnworlds-section-content wide">
    <div class="lw-cols one-row multiple-rows-tp">
      <div class="col span_6_of_12 span_12_of_12-tp">
        <h2 class="learnworlds-heading-normal">Title</h2>
        <p class="learnworlds-main-text-normal">Text</p>
        <a class="learnworlds-button-solid-brand">CTA</a>
      </div>
      <div class="col span_6_of_12 span_12_of_12-tp">
        <!-- Image/Video -->
      </div>
    </div>
  </div>
</section>
```

### Pattern 2: Sticky Navigation with Transparency
```html
<section class="lw-topbar sticky-topbar transparent-onStart">
  <div class="learnworlds-section-content wide">
    <div class="lw-topbar-logo-col">Logo</div>
    <nav class="lw-topbar-menu with-hover">Menu</nav>
    <div class="lw-topbar-actions">Actions</div>
  </div>
</section>
```

### Pattern 3: Video Background with Overlay
```html
<section class="learnworlds-section stretched-bg">
  <div class="js-video-wrapper">
    <video autoplay loop muted></video>
  </div>
  <div class="learnworlds-section-overlay lw-dark-bg"></div>
  <div class="learnworlds-section-content wide">
    <!-- Content on top of video -->
  </div>
</section>
```

---

## 9. Implementation Guidelines

### Best Practices
1. **Always include base classes:** `.learnworlds-element`, `.js-learnworlds-section`
2. **Use responsive suffixes:** Ensure mobile-first or desktop-first strategy
3. **Combine utility classes:** Flexbox + alignment + spacing
4. **Test breakpoints:** Verify behavior at all 5 breakpoints
5. **Maintain hierarchy:** Proper heading levels and semantic structure

### Common Mistakes to Avoid
1. Missing responsive grid classes on tablets/mobile
2. Forgetting to add `.js-` classes for interactive elements
3. Incorrect flexbox alignment combinations
4. Not testing sticky navigation scroll behavior
5. Overlooking video autoplay/muted attributes

---

**End of Component Catalog**

*This catalog provides all necessary classes and patterns to recreate or adapt Jetox Education's UI components.*
