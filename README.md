# Bikemate Landing Page Maintenance Guide

This guide will help you maintain and customize the Bikemate landing page. It's written for beginners and provides step-by-step instructions for common updates.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the main navigation and logo. To update:

1. **Logo Text**: Find this line and change "Bikemate" to your brand name:
```html
<a href="#" class="text-2xl font-bold text-indigo-600">Bikemate</a>
```

2. **Navigation Links**: Locate these lines to modify menu items:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-indigo-600 transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-indigo-600 transition-colors duration-300">Voordelen</a>
    <a href="#faq" class="text-gray-600 hover:text-indigo-600 transition-colors duration-300">FAQ</a>
</div>
```

### Hero Section
The hero section is your main banner area. To update:

1. **Main Heading**: Find and modify:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-6 bg-gradient-to-r from-indigo-600 to-purple-600 bg-clip-text text-transparent">
    Bikemate Fietstas
</h1>
```

2. **Subheading**: Update this line:
```html
<p class="text-xl md:text-2xl text-gray-600 mb-8">Tijdelijk 10% Korting | Nog maar beperkte voorraad beschikbaar!</p>
```

### Understanding Tailwind Classes
Common classes used in this page:

- Text sizes: `text-sm`, `text-xl`, `text-2xl`, etc.
- Colors: `text-indigo-600`, `bg-white`, etc.
- Spacing: `px-4`, `py-2`, `mb-8`, etc.
- Responsive prefixes: `md:`, `lg:` (for different screen sizes)

Example of modifying text size and color:
```html
<!-- Original -->
<p class="text-xl text-gray-600">

<!-- Making text larger and blue -->
<p class="text-2xl text-blue-600">
```

## Managing Links

### Navigation Links
1. Internal links use hashtags (#) to scroll to sections:
```html
<!-- Current internal links -->
<a href="#features">Features</a>
<a href="#benefits">Voordelen</a>
<a href="#faq">FAQ</a>
```

2. To update the product link, find all instances of:
```html
<a href="https://amzn.to/3Gsbp9O"
```
Replace with your new product URL.

### Footer Links
Located at the bottom of the page:
```html
<ul class="space-y-2">
    <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>
```

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
1. Create two new files:
   - `privacy.html`
   - `terms.html`

### Step 2: Update Footer Links
Replace the placeholder "#" with proper file paths:
```html
<!-- Original -->
<a href="#">Privacy Policy</a>

<!-- Updated -->
<a href="privacy.html">Privacy Policy</a>

<!-- Original -->
<a href="#">Terms of Service</a>

<!-- Updated -->
<a href="terms.html">Terms of Service</a>
```

### Step 3: Maintain Consistent Styling
Copy these classes to maintain the same hover effect:
```html
class="hover:text-white transition-colors duration-300"
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Ensure section IDs match the href attributes
   - Check for typos in IDs
   ```html
   <!-- Link -->
   <a href="#features">
   <!-- Must match -->
   <section id="features">
   ```

2. **Responsive Design Issues**
   - Check mobile view using browser dev tools
   - Verify responsive classes are correct:
   ```html
   <!-- Example of correct responsive classes -->
   <div class="text-sm md:text-base lg:text-lg">
   ```

3. **Style Changes Not Working**
   - Verify Tailwind CDN is loading
   - Check for typos in class names
   - Make sure classes are within quotation marks

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Validate HTML at [W3C Validator](https://validator.w3.org/)
- Test responsive design using browser developer tools

Remember to always test changes across different devices and browsers before publishing updates.