# 3D E-Commerce Website

A modern e-commerce website featuring a 3D robot theme, built for selling digital products with Facebook ads integration.

## Features

- **3D Robot Theme**: Consistent 3D robot branding across all pages using Spline 3D viewer
- **Product Catalog**: Dynamic product management with local storage
- **Shopping Cart**: Full cart functionality with persistent storage
- **Payment Processing**: Simulated payment system with multiple payment methods
- **Admin Panel**: Complete order and customer management dashboard
- **Responsive Design**: Mobile-first design that works on all devices
- **Developer Friendly**: Easy product management with console commands

## Quick Start

1. **Start Local Server**:
   ```bash
   python -m http.server 8000
   ```
   
2. **Open in Browser**:
   Navigate to `http://localhost:8000`

## Pages Overview

- **`index.html`** - Landing page with 3D robot and navigation
- **`products.html`** - Product catalog with shopping functionality
- **`checkout.html`** - Payment page with 3D robot in CRT display
- **`order-confirmation.html`** - Order success page
- **`admin.html`** - Admin dashboard for order management

## Developer Commands

Open browser console on any page and use these commands:

### Product Management
```javascript
// Add a new product
productManager.addProduct({
    name: "New Digital Course",
    price: 49.99,
    description: "Amazing course content",
    image: "https://via.placeholder.com/300x200",
    category: "education"
});

// Remove a product
productManager.removeProduct("product-id");

// Get all products
productManager.getProducts();
```

### Cart Management
```javascript
// Add item to cart
cartManager.addToCart(productId, quantity);

// View cart contents
cartManager.getCart();

// Clear cart
cartManager.clearCart();
```

### Admin Functions
```javascript
// Get all orders
adminManager.getOrders();

// Get analytics data
adminManager.generateAnalytics();

// Export orders to CSV
adminManager.exportOrders();
```

## File Structure

```
├── index.html              # Landing page
├── products.html           # Product catalog
├── checkout.html           # Payment page
├── order-confirmation.html # Success page
├── admin.html             # Admin dashboard
├── css/
│   ├── products.css       # Product page styles
│   ├── checkout.css       # Checkout page styles
│   ├── confirmation.css   # Confirmation page styles
│   └── admin.css         # Admin panel styles
├── js/
│   ├── cart.js           # Cart management
│   ├── products.js       # Product management
│   ├── checkout.js       # Payment processing
│   ├── confirmation.js   # Order confirmation
│   ├── admin.js         # Admin functionality
│   └── backend.js       # API simulation
└── style.css            # Main styles
```

## Customization

### Adding New Products
Products are stored in `js/products.js`. You can modify the sample products or use the console commands to add new ones dynamically.

### Payment Integration
The payment system is currently simulated. To integrate real payments:
1. Replace the `processPayment` method in `js/backend.js`
2. Add your payment provider's SDK
3. Update the checkout form validation as needed

### 3D Robot Model
The 3D robot is loaded from Spline. To change the model:
1. Create your 3D scene in Spline
2. Get the embed URL
3. Update the `src` attribute in the `<spline-viewer>` elements

### Styling
- Main theme colors and styles are in `style.css`
- Page-specific styles are in the `css/` folder
- The design uses CSS Grid and Flexbox for responsive layouts

## Browser Support

- Chrome 80+
- Firefox 75+
- Safari 13+
- Edge 80+

## Notes

- All data is stored in localStorage (no backend required)
- The 3D robot requires WebGL support
- Payment processing is simulated for demo purposes
- Admin panel shows sample analytics data

## License

This project is for demonstration purposes. Customize as needed for your use case.