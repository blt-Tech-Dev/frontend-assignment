# Frontend Take-Home Assignment

## E-commerce Product Listing & Cart

Build a product listing page with a shopping cart. We want to see how you handle layout, state management, and user interactions.

**Time expectation:** 4-6 hours  
**Submission:** GitHub repo + README

---

## What You'll Build

A product catalog where users can browse items, filter results, and manage a shopping cart.

---

## Core Requirements (Must Have - 60%)

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
  - Under 1,000
  - 1,000-5,000
  - Over 5,000

---

## Intermediate Features (Nice to Have - 30%)

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

Add a "View Summary" or "Export Cart" button that shows cart data in a flattened format for debugging or export purposes.

Example output:

```json
{
  "totalItems": 3,
  "totalPrice": 15000,
  "items.0.id": "prod_123",
  "items.0.name": "Laptop",
  "items.0.price": 10000,
  "items.0.quantity": 1,
  "items.1.id": "prod_456",
  "items.1.name": "Mouse",
  "items.1.price": 500,
  "items.1.quantity": 2,
  "appliedFilters.category": "electronics",
  "appliedFilters.priceRange": "5000+"
}
```

This tests your ability to:

- Transform nested objects into flat key-value pairs
- Handle arrays in the flattening logic
- Think about data structures for export/logging scenarios

---

## Advanced Features (Bonus - 10%)

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

## What We're Looking For

**CSS/Tailwind Skills:**

- Proper responsive design that works across all screen sizes
- Clean use of Tailwind utilities
- Smooth animations and transitions
- Layout doesn't break on edge cases

**React Patterns:**

- Clean component composition
- Appropriate use of hooks (useMemo, useCallback where needed)
- Proper cleanup of side effects (timers, subscriptions)
- Performance-aware decisions

**Data Manipulation:**

- Ability to transform complex nested structures
- Handle edge cases (empty objects, arrays, null values)
- Write reusable utility functions

**Code Quality:**

- Correct TypeScript types
- Consistent naming
- Organized file structure
- Readable code

---

## Common Pitfalls to Avoid

- Setting state inside render causing infinite loops
- Not cleaning up timers/subscriptions on unmount
- Using `any` types everywhere
- Hard-coded values that should be responsive
- Layout breaking on mobile devices

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

- Deploy to Vercel
- Include screenshots

---

## Time Management

Don't over-engineer. We'd rather see something clean and working than half-finished fancy features.

**Rough guide:**

- Hours 1-2: Core functionality (grid, cart, add to cart)
- Hours 3-4: Filters and state management
- Hours 5-6: Polish and responsive design

---

## Evaluation Criteria

We're looking for:

- Clean, maintainable code
- Good UX decisions
- Performance awareness
- Attention to detail

We're NOT looking for:

- Pixel-perfect design
- Complex state management libraries
- Backend implementation
- Perfect test coverage

---

## Questions?

If anything is unclear, feel free to ask.

Good luck!
