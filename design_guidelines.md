# Restaurant Management Website Design Guidelines

## Design Approach

**Hybrid Approach**: Customer-facing menu draws inspiration from food delivery platforms (Swiggy/Zomato) for appetizing presentation, while management dashboard follows Material Design principles for data-heavy interfaces.

**Design Philosophy**: Warm, inviting Indian restaurant aesthetic that balances visual appeal with operational efficiency.

## Typography System

**Font Stack**:
- Primary: 'Poppins' (headings, menu items, prices) - Google Fonts
- Secondary: 'Inter' (body text, descriptions, data tables) - Google Fonts

**Hierarchy**:
- Restaurant Name/Logo: text-4xl font-bold
- Section Headers: text-2xl font-semibold
- Menu Item Names: text-xl font-medium
- Prices: text-lg font-bold
- Body Text: text-base font-normal
- Table Data/Labels: text-sm font-medium

## Layout System

**Spacing Units**: Tailwind units of 2, 4, 6, and 8 (p-2, m-4, gap-6, py-8)

**Grid Structure**:
- Menu Grid: grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-6
- Management Dashboard: grid-cols-1 lg:grid-cols-3 gap-8
- Container: max-w-7xl mx-auto px-4

**Section Padding**: py-8 mobile, py-12 desktop

## Component Library

### Navigation
- Sticky top navigation with restaurant logo, active order count badge
- Tab navigation for management sections (Menu, Orders, Reports)
- Mobile: Hamburger menu with slide-out drawer

### Menu Cards
- Rounded-lg cards with shadow-md elevation
- Food image: aspect-ratio-square, object-cover, rounded-t-lg
- Card padding: p-4
- Hover state: transform scale-105 transition-transform
- "Add to Cart" button: Prominent, full-width within card

### Shopping Cart (Fixed Sidebar)
- Right-side fixed panel: w-80 on desktop, full-width drawer on mobile
- Sticky header with "Current Bill" title and item count
- Scrollable item list with quantity controls (+/-) 
- Item rows: flex justify-between with item name, quantity spinner, price
- Subtotal and total rows with clear visual separation (border-t)
- Action buttons: "Clear Cart" (secondary) and "Pay Now" (primary CTA)

### Billing Interface
- Itemized bill table: striped rows for readability
- Columns: Item | Qty | Price | Subtotal
- Total row: Larger font-bold with visual emphasis
- QR Code: Centered, 200x200px container with payment details below
- Print button: Top-right corner with printer icon (use Heroicons)

### Management Dashboard
- Sales metrics cards: 4-column grid showing total revenue, orders, popular items
- Monthly report: Line chart for revenue trends, bar chart for item popularity
- Data tables: Sortable columns, pagination, search functionality
- CRUD forms: Modal overlays for add/edit operations with form validation states

### Forms (Menu Management)
- Input fields: Full-width with labels above, border-2 on focus
- Image upload: Drag-and-drop area with preview
- Price inputs: Number input with rupee symbol prefix
- Submit buttons: Primary styling, disabled state during submission

### Icons
Use Heroicons via CDN:
- Cart icon (shopping bag)
- Print icon
- Add/Remove icons (+/-)
- Edit/Delete icons (pencil/trash)
- QR code icon
- Chart icons for reports

### Modals & Overlays
- Payment QR modal: Centered overlay with backdrop blur
- Print view: Clean, minimal layout optimized for printing
- Delete confirmations: Small centered modal with clear actions

## Images

**Food Photography**:
- Menu items: High-quality, appetizing photos of each dish
- Aspect ratio: 1:1 (square) for consistency
- Style: Natural lighting, close-up shots showing texture and garnish
- Placement: Top of each menu card

**Image Requirements**:
- Idly (steamed rice cakes with chutney)
- Pattu (poori/bread variation)
- Poori (fried bread with curry)
- Coffee (South Indian filter coffee in traditional tumbler)
- Dosai (crispy crepe with filling)
- Vadai (savory fried lentil donuts)

No hero image required - dive straight into functional menu display.

## Interaction Patterns

**Menu Ordering Flow**:
1. Click menu card → Item instantly added to cart with visual feedback (brief scale animation)
2. Cart badge updates with count
3. Cart auto-scrolls to show new item
4. Toast notification: "Item added to cart"

**Checkout Flow**:
1. "Pay Now" → Modal with bill summary
2. Generate QR code with bill amount
3. Options: "Print Bill" or "Complete Order"

**Management Operations**:
- Inline editing for menu items (click to edit mode)
- Delete with confirmation dialog
- Add new item via floating action button (bottom-right)

## Accessibility

- All interactive elements: min 44x44px touch targets
- Form labels: Always visible, not placeholders
- Focus states: Prominent border indication
- ARIA labels for icon-only buttons
- Keyboard navigation throughout

## Responsive Behavior

**Mobile (< 768px)**:
- Single column menu grid
- Cart as slide-up drawer from bottom
- Stacked billing layout
- Management tables: Horizontal scroll wrapper

**Tablet (768px - 1024px)**:
- 2-column menu grid
- Cart as right drawer
- Simplified dashboard layout

**Desktop (1024px+)**:
- 3-4 column menu grid
- Fixed right sidebar cart
- Full multi-column dashboard

## Print Styling

Bill print view includes:
- Restaurant name and address header
- Order date/time and bill number
- Clean table without borders
- Total highlighted
- Footer with thank you message
- Remove all navigation and interactive elements