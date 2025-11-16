# 🍽️ Food Checkout Billing System - Demo Guide

## 🚀 Quick Start

**Access the application:** http://127.0.0.1:5000

---

## 📋 Application Overview

This is a complete Restaurant POS (Point of Sale) system with three main user roles:

1. **Customer** - Browse menu, order food, checkout
2. **Store Manager** - Manage menu, view orders, sales analytics
3. **Maintenance Team** - Manage maintenance tasks and team members

---

## 🎯 Demo Walkthrough

### Step 1: Role Selection (Home Page)

When you first open the application, you'll see three role cards:

- **Customer** - Click to enter customer ordering mode
- **Store Manager** - Click to manage the restaurant
- **Maintenance** - Click to manage maintenance tasks

---

### Step 2: Customer Mode Demo

**Features to demonstrate:**

1. **Browse Menu**
   - View 6 default menu items (Idly, Poori, Dosai, Coffee, Vadai, Pattu)
   - Each item shows:
     - Food image
     - Name and description
     - Price in ₹ (Indian Rupees)
     - Category (Breakfast, Beverages, Snacks)

2. **Search Functionality**
   - Use the search bar to filter items by name or description

3. **Add to Cart**
   - Click "Add" button on any item
   - Items appear in the cart sidebar on the right
   - Adjust quantities using +/- buttons
   - View real-time total calculation

4. **Checkout Process**
   - Click "Checkout" button when cart has items
   - Billing modal opens with:
     - Order summary
     - Payment method selection (UPI)
     - Order confirmation
   - After payment, invoice is generated
   - Option to print the invoice

5. **Exit**
   - Click "Exit" to return to role selection

---

### Step 3: Store Manager Mode Demo

**Features to demonstrate:**

#### Tab 1: Menu & Orders Management

1. **View Menu Items**
   - See all menu items in a table
   - View details: Name, Price, Category, Description

2. **Add New Menu Item**
   - Click "Add Menu Item" button
   - Fill in form:
     - Name (required)
     - Price (required)
     - Description (optional)
     - Image filename (optional)
     - Category (optional)
   - Click "Create" to add

3. **Edit Menu Item**
   - Click "Edit" button on any item
   - Modify details
   - Click "Update" to save changes

4. **Delete Menu Item**
   - Click "Delete" button
   - Confirm deletion

5. **View Orders**
   - See all orders placed by customers
   - View order details:
     - Order ID
     - Items ordered
     - Total amount
     - Payment method
     - Timestamp

#### Tab 2: Sales Report

1. **View Sales Analytics**
   - Total revenue
   - Total number of orders
   - Popular items (top 10)
   - Daily sales breakdown

2. **Filter by Date Range**
   - Select start and end dates
   - View filtered sales data
   - See charts and graphs

---

### Step 4: Maintenance Team Mode Demo

**Features to demonstrate:**

#### Tab 1: Tasks

1. **View Maintenance Tasks**
   - See all tasks with status badges:
     - Pending (orange)
     - In-Progress (blue)
     - Completed (green)

2. **Create New Task**
   - Click "New Task" button
   - Fill in:
     - Task Title (required)
     - Category (e.g., Plumbing, Electrical)
     - Priority (Low, Medium, High, Urgent)
     - Location (optional)
   - Click "Create Task"

3. **Update Task Status**
   - Click "Start" to begin a pending task
   - Click "Complete" to finish an in-progress task
   - Click "Reopen" to restart a completed task

#### Tab 2: Team

1. **View Team Members**
   - See all maintenance team members
   - View details:
     - Name and Role
     - Phone and Email
     - Status (Available/Busy)
     - Join date

2. **Add Team Member**
   - Click "Add Member" button
   - Fill in:
     - Full Name (required)
     - Role (e.g., Plumber, Electrician) (required)
     - Phone Number (optional)
     - Email (optional)
   - Click "Add Member"

3. **Update Member Status**
   - Click "Mark Busy" to set status to busy
   - Click "Mark Available" to set status to available

---

## 🎨 Key Features

### ✅ What Works:

- ✅ Role-based access (Customer, Store Manager, Maintenance)
- ✅ Menu browsing with images
- ✅ Shopping cart functionality
- ✅ Order placement and checkout
- ✅ Invoice generation
- ✅ Menu item CRUD operations
- ✅ Order management
- ✅ Sales reporting with analytics
- ✅ Maintenance task management
- ✅ Team member management
- ✅ Real-time status updates
- ✅ Search and filter functionality

### 🖼️ Default Menu Items:

1. **Idly** - ₹30 - Breakfast
2. **Poori** - ₹60 - Breakfast
3. **Dosai** - ₹40 - Breakfast
4. **Coffee** - ₹20 - Beverages
5. **Vadai** - ₹30 - Snacks
6. **Pattu** - ₹50 - Breakfast

---

## 🔧 Technical Details

- **Frontend:** React + TypeScript + Vite
- **Backend:** Express.js + TypeScript
- **UI Components:** Radix UI + Tailwind CSS
- **State Management:** TanStack Query (React Query)
- **Routing:** Wouter
- **Storage:** In-memory storage (MemStorage)

---

## 📝 Demo Script

### Quick Demo (5 minutes):

1. **Start as Customer** (2 min)
   - Browse menu
   - Add 2-3 items to cart
   - Complete checkout
   - View invoice

2. **Switch to Store Manager** (2 min)
   - View orders
   - Add a new menu item
   - Check sales report

3. **Switch to Maintenance** (1 min)
   - Add a team member
   - Create a maintenance task
   - Update task status

---

## 🎯 Tips for Demo

1. **Start Fresh:** Clear browser session storage to reset roles
2. **Use Real Data:** Add actual menu items and orders
3. **Show Workflow:** Demonstrate complete customer journey
4. **Highlight Features:** Point out search, filters, and real-time updates
5. **Show Responsiveness:** Resize browser to show mobile-friendly design

---

## 🐛 Troubleshooting

If something doesn't work:

1. **Refresh the page** - Sometimes needed after code changes
2. **Check browser console** - Look for any error messages
3. **Verify server is running** - Check terminal for server logs
4. **Clear session storage** - Use browser DevTools to clear storage

---

## 🎉 Enjoy Your Demo!

The application is fully functional and ready to demonstrate all features. Have fun exploring!

