# Landing Page Maintenance Guide

This guide will help you maintain and customize the Nachtbril landing page. Follow these detailed instructions to make common updates while preserving the page's functionality and design.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Text Content Updates

#### Header Section
```html
<!-- Original announcement bar text -->
<div class="bg-black text-white text-center py-2 text-sm">
    <p>Gratis verzending bij bestellingen boven €50</p>
</div>
```
To update the announcement text, simply modify the content between the `<p>` tags.

#### Hero Section
The hero section contains three main text elements:
```html
<h1 class="text-4xl md:text-6xl font-bold mb-6">Overzetbril Nachtbril</h1>
<p class="text-xl md:text-2xl mb-8">Schrijf Alles In Het Nederlands Over Overzetbril Nachtbril</p>
<a href="https://nachtbril.com/shop">Shop Nu</a>
```
Update these by changing the text between the tags while keeping the surrounding HTML structure intact.

### Tailwind CSS Classes Explained

#### Responsive Design Classes
- `md:` prefix: Applies styles on medium screens (768px and up)
- `lg:` prefix: Applies styles on large screens (1024px and up)

Example:
```html
<div class="text-4xl md:text-6xl">
```
This makes text larger on medium screens (md:text-6xl) while maintaining smaller text (text-4xl) on mobile.

#### Common Class Patterns
1. Spacing Classes:
   - `px-4`: Horizontal padding
   - `py-2`: Vertical padding
   - `mb-6`: Bottom margin
   - `mt-8`: Top margin

2. Flex Classes:
   - `flex`: Creates a flex container
   - `items-center`: Vertically centers items
   - `justify-between`: Spaces items evenly

3. Color Classes:
   - `bg-black`: Black background
   - `text-white`: White text
   - `hover:bg-gray-800`: Dark gray background on hover

## Managing Links

### Current Link Structure
```html
<!-- Navigation Links -->
<div class="hidden md:flex items-center space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="https://nachtbril.com/shop">Shop Now</a>
</div>
```

### Updating Links
1. Internal Links (sections on the same page):
   - Keep the `#` prefix
   - Match the ID of the target section
   ```html
   <a href="#features">Features</a>
   <!-- Links to -->
   <section id="features">
   ```

2. External Links:
   - Replace the full URL in href
   ```html
   <a href="https://nachtbril.com/shop">Shop Now</a>
   ```

### Link Verification
Always test links after updating by:
1. Clicking internal links to ensure smooth scrolling
2. Opening external links in a new tab
3. Checking mobile menu functionality

## Adding Privacy and Terms Pages

### Footer Modification
Add privacy and terms links to the footer:
```html
<div class="border-t border-gray-800 mt-12 pt-8 text-center">
    <p>&copy; 2024 Nachtbril. All rights reserved.</p>
    <!-- Add these lines -->
    <div class="mt-4 space-x-4">
        <a href="/privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a>
        <a href="/terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a>
    </div>
</div>
```

### Creating Policy Pages
1. Create new files:
   - `privacy.html`
   - `terms.html`

2. Use consistent styling:
```html
<!-- privacy.html/terms.html template -->
<!DOCTYPE html>
<html lang="nl" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Privacy Policy - Nachtbril</title>
    <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
</head>
<body class="font-sans antialiased">
    <!-- Copy header from index.html -->
    
    <main class="container mx-auto px-4 py-16">
        <h1 class="text-3xl font-bold mb-8">Privacy Policy</h1>
        <!-- Add policy content here -->
    </main>

    <!-- Copy footer from index.html -->
</body>
</html>
```

## Troubleshooting

### Common Issues

1. Broken Responsive Design
   - Check for missing `md:` or `lg:` prefixes
   - Verify container classes are present
   ```html
   <div class="container mx-auto px-4">
   ```

2. Misaligned Elements
   - Ensure proper flex classes:
   ```html
   <div class="flex items-center justify-between">
   ```

3. Missing Styles
   - Confirm Tailwind CSS link is present:
   ```html
   <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
   ```

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Verify HTML structure matches the original
- Test on multiple devices and browsers

Remember to always make a backup before making significant changes to the code.