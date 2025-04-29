# Landing Page Maintenance Guide

This guide will help you maintain and customize the Kruidvat Nachtbril landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common maintenance tasks.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the main navigation and logo. To update:

1. **Logo Text:**
```html
<!-- Find this line in the header -->
<a href="/" class="text-2xl font-bold text-blue-600">Nachtbril</a>
```
Simply replace "Nachtbril" with your desired text.

2. **Navigation Menu Items:**
```html
<a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-200">Kenmerken</a>
```
Update the text between `<a>` tags to change menu items.

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl sm:text-5xl lg:text-6xl font-extrabold text-gray-900 mb-8 leading-tight">
    Kruidvat Nachtbril
    <span class="block text-blue-600">Nu 10% Korting!</span>
</h1>
```
- Change "Kruidvat Nachtbril" for the main heading
- Modify "Nu 10% Korting!" for the promotional text
- The `text-4xl` class controls text size (options: text-sm, text-base, text-lg, text-xl, etc.)

### Tailwind CSS Tips for Beginners
- `text-{color}-{shade}`: Changes text color (e.g., `text-blue-600`)
- `bg-{color}-{shade}`: Changes background color
- `p-{number}`: Adds padding (p-4 = 1rem padding)
- `m-{number}`: Adds margin
- `font-{weight}`: Changes text weight (e.g., font-bold)

## Managing Links

### Updating Navigation Links
Current navigation links in the header:
```html
<div class="hidden md:flex items-center space-x-8">
    <a href="#features">Kenmerken</a>
    <a href="#benefits">Voordelen</a>
    <a href="#faq">FAQ</a>
    <a href="https://nachtbril.com/shop">Bestel Nu</a>
</div>
```

To update:
1. Internal links (starting with #) point to section IDs on the same page
2. External links (starting with http) point to other websites
3. Replace `href` values with your desired destinations

### Call-to-Action Buttons
Main CTA buttons are located in two places:
```html
<!-- Hero section -->
<a href="https://nachtbril.com/shop" class="inline-flex items-center justify-center px-8 py-4...">
    Claim Je Korting
</a>

<!-- Bottom section -->
<a href="https://nachtbril.com/shop" class="inline-flex items-center justify-center px-8 py-4...">
    Bestel Nu Met 10% Korting
</a>
```
Update both `href` attributes to point to your shop or checkout page.

## Adding Privacy and Terms Pages

### Step 1: Add Footer Links
Locate the footer section and add new links:
```html
<div class="border-t border-gray-800 mt-12 pt-8 text-sm text-gray-400">
    <p>&copy; 2024 Kruidvat Nachtbril. Alle rechten voorbehouden.</p>
    <!-- Add these lines -->
    <div class="mt-4 space-x-4">
        <a href="/privacy.html" class="hover:text-white transition-colors duration-200">Privacy Policy</a>
        <a href="/terms.html" class="hover:text-white transition-colors duration-200">Terms & Conditions</a>
    </div>
</div>
```

### Step 2: Create Policy Pages
1. Create two new files in your root directory:
   - `privacy.html`
   - `terms.html`
2. Use the same header and footer as `index.html`
3. Add your policy content in the main section

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links:**
   - Ensure section IDs match the href attributes
   - Example: `href="#features"` needs a matching `id="features"` in the HTML

2. **Responsive Design Issues:**
   - Check for proper responsive classes:
   ```html
   text-4xl sm:text-5xl lg:text-6xl
   ```
   - The above means:
     - Mobile: text-4xl
     - Small screens (sm): text-5xl
     - Large screens (lg): text-6xl

3. **Missing Styles:**
   - Verify the Tailwind CSS link is correct:
   ```html
   <link href="https://unpkg.com/tailwindcss@^2/dist/tailwind.min.css" rel="stylesheet">
   ```

### Need Help?
If you encounter issues:
1. Check the browser's developer tools (F12) for errors
2. Verify all files are in the correct directory
3. Ensure all links point to valid URLs
4. Test the page across different devices and browsers

Remember to always make a backup before making significant changes to your code.