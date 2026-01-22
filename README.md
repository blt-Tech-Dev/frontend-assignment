# Frontend Take-Home Assignment

## E-commerce Product Listing & Cart

Build a simple product listing page with a shopping cart. We want to see how you handle layout, state, and user interactions.

---

## What You'll Build

A product catalog where users can browse items, filter/search, and manage a shopping cart.

---

## Core Requirements (60%)

### 1. Product Listing Page

- Display products in a grid layout (cards)
- Each card shows: image, name, price, "Add to Cart" button
- Responsive breakpoints:
  - Mobile: 1 column
  - Tablet: 2 columns
  - Desktop: 3-4 columns
- Show a loading state while fetching data

### 2. Shopping Cart (Sidebar or Modal)

- List selected items
- Each item shows: name, price, quantity control (+/-)
- Display total price
- Remove item button
- Handle empty cart state gracefully

### 3. Filter & Search

- Search by product name (real-time filtering)
- Filter by category (dropdown or tabs)
- Filter by price range (simple tiers: under 1000, 1000-5000, 5000+)

---

## Intermediate (30%)

### 4. CSS Touches

- Skeleton loading instead of spinners
- Smooth hover effects
- Cart animation when adding items
- Sticky header with cart icon + item count badge
- Toast notification on add to cart

### 5. State Management

- Persist cart state to localStorage
- Sync filters to URL params (so links are shareable)

---

## Advanced (10%)

### 6. Extra Features

- Infinite scroll or pagination
- Product quick-view modal
- Sort options (by price, name)
- Debounced search input
- Image lazy loading

---

## Tech Stack

- **Next.js 15+** (App Router)
- **TypeScript** (strict mode)
- **Tailwind CSS** — no component libraries allowed
- **React hooks** for state management
- **Mock API data** — provided JSON file or use [Fake Store API](https://fakestoreapi.com)

---

## CSS Skills We're Checking

You should be comfortable with:

1. **Responsive grid** — columns adjust per breakpoint
2. **Flexbox/Grid** — complex layouts without hacks
3. **CSS transitions** — smooth animations
4. **Positioning** — badge on cart icon, sticky header
5. **Custom scrollbar** — for cart sidebar
6. **Skeleton loaders** — content placeholders

---

## What We're Looking For

**CSS/Tailwind:**

- Proper use of utility classes
- Thoughtful responsive design
- Smooth animations and transitions
- Layout doesn't break at any screen size

**React Patterns:**

- Clean component composition
- Custom hooks used appropriately (useMemo, useCallback where it matters)
- Sensible state management
- Performance-aware code

**Code Quality:**

- Correct TypeScript types
- Consistent naming conventions
- Organized file structure
- Clean git history

---

## Deliverables

- Public GitHub repo
- README that includes:
  - Setup instructions
  - Features you implemented
  - How long it took
  - Trade-offs and decisions you made
- Live demo on Vercel (bonus)

---

## Time Expectation

This should take roughly 4-6 hours. Don't over-engineer it — we'd rather see something clean and working than half-finished bells and whistles.

---

## Questions?

Reach out if anything's unclear. Good luck!
