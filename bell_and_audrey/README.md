
## 📚 Demo 1: Bell & Audrey’s Library (using `@media` queries)

**Step-by-step approach:**

1.  **Add viewport meta tag**
    
    html
    
    ```
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    ```
    
2.  **Flexible images**
    
    css
    
    ```
    img {
      max-width: 100%;
      height: auto;
    }
    ```
    
3.  **Responsive layout with Flexbox**
    
    css
    
    ```
    .section {
      display: flex;
      flex-wrap: wrap;
    }
    .section div {
      flex: 1 1 300px;
      margin: 10px;
    }
    ```
    
4.  **Navigation adapts with media queries**
    
    css
    
    ```
    nav ul {
      display: flex;
      justify-content: space-around;
    }
    @media (max-width: 768px) {
      nav ul {
        flex-direction: column;
        align-items: center;
      }
    }
    ```
    

👉 This demo shows  how **manual control** works: they write the rules, test breakpoints, and see the site adapt.

---

# Responsive Design Implementation


## Key Changes Made

### HTML Structure
- Replaced `<ul class="header">` with semantic `<header>` and `<nav>` elements
- Added `<main>` wrapper for main content
- Used `<section>` for hero and content areas
- Replaced generic divs with semantic `.card` components

### CSS Classes Added
- `.navbar` - Flexbox navigation container
- `.nav-brand` - Logo and title grouping
- `.nav-menu` - Navigation links container
- `.hero-section` - Main intro section
- `.content-grid` - CSS Grid for responsive cards
- `.card` - Individual content cards

### Responsive Features
- CSS Grid with `auto-fit` and `minmax()` for flexible layouts
- Mobile-first navigation that stacks vertically on small screens
- Responsive images with `max-width: 100%`
- Flexible gap spacing that adapts to screen size

### Breakpoint
- 768px breakpoint for mobile/tablet optimization
- Navigation switches from horizontal to vertical layout
- Grid becomes single column on mobile devices


---


## Bulma CSS Implementation

### Key Bulma Classes Used
- `navbar` and `navbar-brand` - Responsive navigation system
- `hero is-medium` - Hero section with built-in responsive behavior
- `columns is-multiline` - Flexible grid system that wraps on mobile
- `column is-one-third` - Three-column layout that stacks on mobile
- `card` - Pre-styled card components
- `container` - Centered content with responsive margins

### Responsive Features with Bulma
- Automatic mobile navigation (navbar collapses on mobile)
- Column system automatically stacks on tablets and mobile
- Built-in responsive typography with `title` and `subtitle` classes
- Responsive images with `image` and `figure` classes
- No custom CSS breakpoints needed - Bulma handles responsiveness

### Bulma Benefits
- Zero custom responsive CSS required
- Built-in mobile-first design
- Consistent spacing and typography
- Automatic accessibility features