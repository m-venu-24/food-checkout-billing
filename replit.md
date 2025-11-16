# Restaurant Management System

A complete restaurant point-of-sale and management system built with React, Express, and TypeScript.

## Overview

Full-featured restaurant management application with menu ordering, billing with QR code payments, and comprehensive sales reporting.

## Features Implemented

### Customer-Facing Features
- **Interactive Menu**: Grid layout displaying all menu items with appetizing food images
- **Shopping Cart**: Real-time cart with quantity controls, running total, and item management
- **Click-to-Add**: Single-click to add items to cart with visual feedback
- **Billing & Payment**: 
  - Itemized bill with quantities and prices
  - UPI QR code generation for payments
  - Printable bill format
  - Order confirmation flow

### Management Features
- **Menu CRUD Operations**:
  - Add new menu items with name, price, description, image, category
  - Edit existing items
  - Delete items with confirmation
  - Real-time updates across the application
  
### Analytics & Reporting
- **Sales Dashboard**:
  - Total revenue and order count
  - Average order value
  - Popular items ranking
- **Visual Charts**:
  - Daily sales trend line chart
  - Popular items bar chart
  - Top selling items table with revenue breakdown

## Technical Stack

### Frontend
- **React** with TypeScript
- **TanStack Query** for data fetching and caching
- **Wouter** for client-side routing
- **Shadcn UI** components with Tailwind CSS
- **Recharts** for data visualization
- **QRCode.react** for QR code generation
- **react-to-print** for bill printing

### Backend
- **Express.js** with TypeScript
- **In-memory storage** using Map data structures
- **Zod** for request validation
- **Drizzle ORM** schemas for type safety

## Data Models

### MenuItem
- id (UUID)
- name
- price (decimal as string)
- description (optional)
- image (key for image mapping)
- category (optional)

### Order
- id (UUID)
- items (JSON stringified CartItem array)
- total (decimal as string)
- timestamp
- paymentMethod
- status

### CartItem (frontend only)
- menuItemId
- name
- price
- quantity

## API Endpoints

### Menu Items
- `GET /api/menu-items` - Fetch all menu items
- `GET /api/menu-items/:id` - Fetch single item
- `POST /api/menu-items` - Create new item
- `PUT /api/menu-items/:id` - Update item
- `DELETE /api/menu-items/:id` - Delete item

### Orders
- `POST /api/orders` - Create new order
- `GET /api/orders` - Fetch all orders

### Sales Reports
- `GET /api/sales` - Get sales analytics (supports optional date range)

## Default Menu Items

The system initializes with 6 South Indian cuisine items:
1. Idly - ₹30 (Soft steamed rice cakes)
2. Poori - ₹60 (Fluffy fried bread)
3. Dosai - ₹40 (Crispy rice crepe)
4. Coffee - ₹20 (South Indian filter coffee)
5. Vadai - ₹30 (Fried lentil donuts)
6. Pattu - ₹50 (Layered flaky bread)

## Design System

### Colors
- Primary: Orange (#D97706) - Warm, inviting restaurant theme
- Typography: Poppins for headings, Inter for body text
- Semantic color tokens for consistency across light/dark modes

### Layout
- Responsive grid layouts (1-4 columns based on screen size)
- Sticky navigation bar
- Fixed cart sidebar on desktop, drawer on mobile
- Max-width container (7xl) for optimal readability

### Components
- Uses Shadcn UI components exclusively
- Consistent spacing (p-2, p-4, gap-6, py-8)
- Hover and active elevation effects
- Skeleton loading states
- Beautiful empty states

## User Journeys

### Customer Ordering Flow
1. Browse menu items on homepage
2. Click items to add to cart
3. Adjust quantities using +/- buttons
4. Click "Pay Now" to review order
5. See QR code for UPI payment
6. Complete order
7. Print bill (optional)

### Menu Management Flow
1. Navigate to Management page
2. View all current menu items
3. Add/Edit/Delete items as needed
4. Changes reflect immediately across the app

### Sales Review Flow
1. Navigate to Reports page
2. View summary statistics
3. Analyze daily sales trends
4. Review popular items performance

## Recent Changes

### November 16, 2025
- Initial implementation of complete restaurant management system
- Generated high-quality food images for all menu items
- Built responsive frontend with menu, management, and reports pages
- Implemented full backend API with validation
- Added QR code payment integration
- Created comprehensive sales reporting with charts
- Completed end-to-end testing - all features working

## Project Structure

```
client/
  src/
    components/
      billing-modal.tsx - Order billing with QR code
      printable-bill.tsx - Print-optimized bill format
      ui/ - Shadcn UI components
    pages/
      menu-page.tsx - Main ordering interface
      management-page.tsx - Menu CRUD operations
      sales-report-page.tsx - Analytics dashboard
    App.tsx - Routing and navigation
    
server/
  routes.ts - API endpoints
  storage.ts - In-memory data storage
  
shared/
  schema.ts - TypeScript types and Zod schemas
```

## Testing

All core functionality verified through end-to-end tests:
- ✅ Menu browsing and display
- ✅ Cart management (add, update quantity, remove, clear)
- ✅ Order placement and confirmation
- ✅ QR code generation
- ✅ Menu item CRUD operations
- ✅ Sales reporting accuracy
- ✅ Navigation between pages
- ✅ Responsive layouts

## Future Enhancements

Potential improvements for next phase:
- Table management for dine-in orders
- Customer details capture for delivery
- Order history with date filtering
- Advanced analytics (weekly/yearly trends)
- Payment gateway integration
- Multi-language support
- Dark mode toggle
- Export reports to PDF/Excel
