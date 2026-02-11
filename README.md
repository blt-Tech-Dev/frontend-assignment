# Frontend Take-Home Assignment

## E-commerce Product Listing & Cart

Build a product listing page with a shopping cart. We want to see how you handle layout, state management, and user interactions.

**Time expectation:** 4-6 hours  
**Submission:** GitHub repo + README

---

## What You'll Build

A product catalog where users can browse items, filter results, and manage a shopping cart.

---

## Core Requirements (Must Have + 60%)

### 1. Product Listing

Display products in a grid:

- Each card: image, name, price, "Add to Cart" button
- Responsive layout:
  - Mobile: 1 column
  - Tablet: 2 columns  
  - Desktop: 3-4 columns
- Loading state while fetching

### 2. Shopping Cart (Sidebar or Modal)

- Show selected items with quantity controls (+/-)
- Display item name, price per unit
- Show total price
- Remove item option
- Empty state when cart is empty

### 3. Filter & Search

- Real-time search by product name
- Category filter (dropdown or tabs)
- Price range filter:
  - Under $50
  - $50-$200
  - Over $200
  - **Bonus:** Implement as a draggable price range slider instead of fixed options

---

## Intermediate Features (Nice to Have + 30%)

### 4. Polish the UI

- Skeleton loaders (not just spinners)
- Smooth hover effects on cards
- Cart animation when adding items
- Sticky header with cart icon showing item count
- Toast notification on successful add

### 5. State Persistence

- Save cart to localStorage
- Sync active filters to URL params (shareable links)

### 6. Cart Summary Export

Add an "Export Cart" feature that transforms nested cart state into a flattened format. This simulates preparing data for analytics, logging, or external systems.

**How to export (choose any approach):**

- Download as `.txt` or `.json` file
- Display in a modal/dialog
- Log to browser console

**Example transformation:**

```typescript
// Original nested structure
const cart = {
  items: [
    { id: 'prod_123', name: 'Gaming Monitor', price: 999.99, quantity: 1 },
    { id: 'prod_456', name: 'T-Shirt', price: 22.30, quantity: 2 }
  ],
  filters: {
    category: 'electronics',
    priceRange: '$200+'
  },
  metadata: {
    timestamp: '2026-01-15T10:00:00Z'
  }
};

// After flattening (dot notation)
{
  "items.0.id": "prod_123",
  "items.0.name": "Gaming Monitor",
  "items.0.price": 999.99,
  "items.0.quantity": 1,
  "items.1.id": "prod_456",
  "items.1.name": "T-Shirt",
  "items.1.price": 22.30,
  "items.1.quantity": 2,
  "filters.category": "electronics",
  "filters.priceRange": "$200+",
  "metadata.timestamp": "2026-01-15T10:00:00Z"
}
```

This tests your ability to:

- Transform nested objects into flat key-value pairs
- Handle arrays in the flattening logic
- Think about data structures for export/logging scenarios

---

## Advanced Features (Bonus + 10%)

Pick one or two if you have time:

- Infinite scroll or pagination
- Quick-view modal for products
- Sort options (price, name)
- Debounced search
- Lazy-load images

---

## Required Stack

- **Next.js 15+** with App Router
- **TypeScript** (strict mode enabled)
- **Tailwind CSS** — no component libraries like shadcn, Material-UI, etc.
- **React hooks** for state
- Mock data from JSON file or [Fake Store API](https://fakestoreapi.com)

---

## What We're Evaluating

### Technical Skills

**CSS & Layout (25%)**

- Responsive design that works across all screen sizes
- Clean use of Tailwind utilities without hacks
- Smooth animations and transitions
- Layout handles edge cases gracefully

**React & State Management (35%)**

- Clean component composition
- Appropriate use of hooks (useMemo, useCallback where it makes sense)
- Proper cleanup of side effects (timers, subscriptions)
- Performance-aware decisions

**Data Handling (20%)**

- Transform complex nested structures correctly
- Handle edge cases (empty objects, arrays, null values)
- Write reusable utility functions

**Code Quality (20%)**

- Correct TypeScript types (minimal use of `any`)
- Consistent naming conventions
- Organized file structure
- Readable, maintainable code

### What We Value

✅ Working features over fancy animations  
✅ Clean code over clever tricks  
✅ Good fundamentals over complex patterns  
✅ Thoughtful decisions over completeness  

### What We Don't Expect

❌ Pixel-perfect design  
❌ State management libraries (Redux, Zustand, etc.)  
❌ Backend implementation  
❌ Test coverage  

---

## Common Pitfalls to Avoid

- Setting state inside render (causes infinite loops)
- Not cleaning up timers/subscriptions on unmount
- Using `any` types everywhere
- Hard-coded pixel values instead of responsive units
- Layout breaking on mobile devices
- Updating localStorage on every render

---

## Deliverables

### GitHub Repository

- Clean, documented code
- Organized file structure
- Reasonable commit history

### README Must Include

1. Setup instructions
2. Features implemented
3. Time spent
4. Technical decisions and trade-offs

### Optional But Recommended

- Deploy to Vercel (Bonus)
- Include screenshots

---

## Time Management

Don't over-engineer. We'd rather see something clean and working than half-finished fancy features.

**Suggested breakdown:**

- **Hours 1-2:** Core functionality (grid, cart, add/remove)
- **Hours 3-4:** Filters and state management
- **Hours 5-6:** Polish and responsive design

If you're running short on time, prioritize core features over bonuses.

---

## Changelog

| Date | Change |
|------|--------|
| 2026-02-11 | Adjusted price range filter to match Fake Store API data (Under $50 / $50-$200 / Over $200). Added bonus for price range slider implementation. |

---

## Questions?

If anything is unclear, feel free to ask.

Good luck!
