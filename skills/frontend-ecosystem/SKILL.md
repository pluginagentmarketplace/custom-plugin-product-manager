---
name: frontend-ecosystem
description: Master modern web development with React, Vue, Angular, TypeScript, CSS, and web performance optimization. Use when learning frontend technologies, building interactive UIs, optimizing web performance, or implementing design systems.
---

# Frontend Ecosystem Skill

## Quick Start

Master modern frontend development through structured learning paths covering frameworks, styling, and web standards.

### Essential Frontend Stack

```javascript
// Modern JavaScript with async/await
async function fetchUserData(userId) {
  const response = await fetch(`/api/users/${userId}`);
  return response.json();
}

// React with hooks
import { useState, useEffect } from 'react';

function UserComponent({ userId }) {
  const [data, setData] = useState(null);

  useEffect(() => {
    fetchUserData(userId).then(setData);
  }, [userId]);

  return <div>{data && <h1>{data.name}</h1>}</div>;
}
```

## Learning Domains

### 🎯 **Core Technologies**

**HTML5 & Semantics**
- Semantic markup for accessibility
- Microdata and schema.org
- Web components and custom elements
- Progressive enhancement techniques

**CSS3 & Modern Layouts**
- Flexbox and Grid layouts
- CSS custom properties and variables
- Animations and transitions
- Media queries and responsive design

**JavaScript ES2024**
- Destructuring and spread operators
- Async/await and promises
- Arrow functions and closures
- Modules and imports/exports

**TypeScript**
- Type annotations and interfaces
- Generics and utility types
- Decorators and metadata
- Type safety in React/Vue/Angular

### ⚛️ **Frontend Frameworks**

**React Expertise**
- Functional components and hooks
- State management patterns
- Performance optimization (memoization, code splitting)
- Testing strategies (Jest, React Testing Library)

**Vue 3**
- Composition API mastery
- Reactive systems and watchers
- Component communication
- Performance and bundling

**Angular**
- Dependency injection
- RxJS and reactive patterns
- Change detection strategies
- Module organization and lazy loading

### 🎨 **Styling & Design**

**CSS Frameworks**
- Tailwind CSS utility-first approach
- Bootstrap and Material Design
- SCSS/LESS preprocessing
- CSS-in-JS solutions

**Design Systems**
- Component libraries (Storybook)
- Design tokens and theming
- Accessibility compliance (WCAG)
- Documentation and maintainability

### 📊 **Web Performance**

**Core Web Vitals**
- Largest Contentful Paint (LCP)
- First Input Delay (FID)
- Cumulative Layout Shift (CLS)
- Time to First Byte (TTFB)

**Optimization Techniques**
- Image optimization and lazy loading
- Code splitting and dynamic imports
- Service workers and caching
- Bundle analysis and reduction

### 🔐 **Security & Accessibility**

**Frontend Security**
- XSS prevention
- CSRF protection
- Content Security Policy (CSP)
- Secure cookie handling

**Accessibility (A11y)**
- ARIA attributes and roles
- Keyboard navigation
- Screen reader optimization
- Color contrast and visual clarity

### 🧪 **Testing Strategies**

**Testing Pyramid**
- Unit tests (Jest, Vitest)
- Integration tests
- E2E tests (Cypress, Playwright)
- Accessibility testing (axe, pa11y)

## Skill Development Checklist

- [ ] Build component library with 20+ reusable components
- [ ] Implement responsive design for desktop, tablet, mobile
- [ ] Optimize web vitals and achieve 90+ Lighthouse score
- [ ] Setup comprehensive testing with 80%+ coverage
- [ ] Create accessible interface (WCAG AA compliance)
- [ ] Implement state management solution
- [ ] Deploy optimized production build
- [ ] Handle real-time data updates

## Real-World Scenarios

**E-Commerce Product Page**
```typescript
// Advanced React component with multiple responsibilities
import React, { useState, useCallback, useMemo } from 'react';
import { useQuery, useMutation } from '@tanstack/react-query';
import { ProductCard } from '@components/ProductCard';
import { ShoppingCart } from '@components/ShoppingCart';

interface Product {
  id: string;
  name: string;
  price: number;
  images: string[];
  reviews: Review[];
}

export const ProductPage: React.FC<{ productId: string }> = ({ productId }) => {
  const { data: product, isLoading } = useQuery({
    queryKey: ['product', productId],
    queryFn: () => fetch(`/api/products/${productId}`).then(r => r.json())
  });

  const { mutate: addToCart } = useMutation({
    mutationFn: async (quantity: number) => {
      const response = await fetch('/api/cart', {
        method: 'POST',
        body: JSON.stringify({ productId, quantity })
      });
      return response.json();
    }
  });

  if (isLoading) return <div>Loading...</div>;

  return (
    <div className="grid grid-cols-1 md:grid-cols-2 gap-8">
      <ProductImages images={product.images} />
      <ProductDetails
        product={product}
        onAddToCart={addToCart}
      />
    </div>
  );
};
```

## Practice Projects

1. **Interactive Dashboard**
   - Real-time data updates
   - Complex filtering and sorting
   - Responsive charts and visualizations

2. **Social Media Feed**
   - Infinite scroll or pagination
   - Comment threads and nested replies
   - Real-time notifications

3. **Collaborative Editor**
   - Real-time text editing
   - Conflict resolution
   - Rich text formatting

## Resources

- **13+ Frontend Roadmaps** - React, Vue, Angular, Next.js, TypeScript
- **124+ Content Modules** - From basics to advanced patterns
- **Interactive Code Examples** - Runnable, copy-paste ready snippets
- **Performance Guides** - Web Vitals, optimization checklists
- **Accessibility Guides** - WCAG compliance, testing tools
- **Best Practices** - Community patterns and anti-patterns

## Assessment Criteria

You've mastered this skill when you can:

✓ Build complex, performant React/Vue/Angular applications
✓ Implement responsive, accessible designs from scratch
✓ Optimize web performance (90+ Lighthouse score)
✓ Create comprehensive test suites (unit, integration, E2E)
✓ Architect scalable component systems
✓ Handle complex state management scenarios
✓ Debug performance issues systematically
