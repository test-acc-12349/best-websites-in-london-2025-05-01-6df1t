# WebLondon Landing Page - Maintenance Guide

This guide will help you maintain and customize the WebLondon landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your logo and navigation menu. To update:

1. **Logo Text**: Find this line and change "WebLondon" to your brand name:
```html
<a href="/" class="text-2xl font-bold text-gray-900">WebLondon</a>
```

2. **Navigation Menu Items**: Located in the header `<nav>` element:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

### Hero Section
Update the main headline and subheading:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-6">Best Websites In London</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">Custom Websites For Your Business</p>
```

### Tailwind CSS Class Guide
Common classes used throughout:
- Text sizes: `text-xl`, `text-2xl`, `text-3xl`, etc.
- Colors: `text-gray-900`, `bg-blue-600`, `text-white`
- Spacing: `px-6`, `py-4`, `mb-12`, `mt-8`
- Responsive design: `md:text-5xl`, `lg:text-6xl`

To modify a style:
1. Find the element you want to change
2. Locate its class attribute
3. Add or modify Tailwind classes as needed

Example - changing text color:
```html
<!-- Original -->
<p class="text-gray-600">Your text here</p>

<!-- Modified to blue -->
<p class="text-blue-600">Your text here</p>
```

## Managing Links

### Current Link Inventory
1. Navigation Menu Links:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

2. Call-to-Action Links:
```html
<a href="https://sigmaseo.io" class="inline-block px-8 py-4 bg-blue-600">Start Your Project</a>
```

### Updating Links
To update any link:
1. Locate the `<a>` tag
2. Modify the `href` attribute
3. Update the link text between the tags

Example:
```html
<!-- Original -->
<a href="https://sigmaseo.io">Start Your Project</a>

<!-- Updated -->
<a href="https://yournewdomain.com">Request a Quote</a>
```

### Footer Links
Update company information and links in the footer:
```html
<div>
    <h4 class="text-white text-lg font-semibold mb-4">Services</h4>
    <ul class="space-y-2">
        <li><a href="#">Web Design</a></li>
        <!-- Add your service page URLs -->
    </ul>
</div>
```

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
Create two new files in your project:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
Locate this section in the footer:
```html
<div>
    <h4 class="text-white text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

Update the links:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Links**
   - Check that all `href` attributes point to valid URLs
   - Ensure internal links (starting with #) match section IDs
   - Test all links after updating

2. **Responsive Design Issues**
   - Keep the `md:` and `lg:` prefixed classes when modifying styles
   - Test on different screen sizes after making changes
   - Don't remove the `container` class from main section wrappers

3. **Style Changes Not Working**
   - Verify Tailwind CDN link is present in the `<head>`
   - Check for typos in class names
   - Ensure classes are space-separated

### Need Help?
- Review the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Test all changes in multiple browsers
- Keep a backup of the original file before making changes

Remember to always test your changes thoroughly before pushing to production. If you're unsure about any modifications, make a backup copy of the file first.