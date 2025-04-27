# Takoma Park Shower Glass Company - Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Takoma Park Shower Glass Company landing page. Whether you're new to web development or need a quick reference, follow these step-by-step instructions.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Company Name and Logo
```html
<!-- Located in the header -->
<a href="/" class="text-2xl font-bold text-gray-900">Takoma Glass</a>
```
To update:
1. Replace "Takoma Glass" with your company name
2. Adjust text size using Tailwind classes:
   - `text-xl` (smaller)
   - `text-2xl` (current)
   - `text-3xl` (larger)

### Hero Section
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 tracking-tight mb-6">
    Takoma Park Shower Glass Company
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">
    Shower door replacement - fast service
</p>
```
To modify:
1. Update heading and subheading text
2. Responsive text sizes are controlled by:
   - `text-4xl` (mobile)
   - `md:text-5xl` (tablet)
   - `lg:text-6xl` (desktop)

### Feature Cards
```html
<div class="bg-white p-8 rounded-xl shadow-lg hover:shadow-xl transition duration-300">
    <div class="text-blue-600 mb-4">
        <!-- Icon SVG here -->
    </div>
    <h3 class="text-xl font-semibold mb-4">Frosted Glass Options</h3>
    <p class="text-gray-600">Enhanced privacy solutions...</p>
</div>
```
To customize:
1. Duplicate this div for additional features
2. Update heading and description text
3. Key styling classes:
   - `shadow-lg`: Box shadow
   - `hover:shadow-xl`: Hover effect
   - `p-8`: Padding
   - `rounded-xl`: Border radius

## Fixing Broken Links

### Navigation Menu Links
Current navigation structure:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">FAQ</a>
    <a href="#contact" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Contact</a>
</div>
```

To update internal links:
1. Ensure section IDs match href attributes
2. Example: `href="#features"` links to `<section id="features">`
3. For external links, replace # with full URL:
   ```html
   <a href="https://yourwebsite.com/page" class="text-gray-600 hover:text-gray-900">
   ```

### Call-to-Action Links
Current CTA button:
```html
<a href="http://www.customeuroglass.com" class="inline-flex items-center px-8 py-4 bg-blue-600 text-white">
    Get Started
</a>
```
To update:
1. Replace URL with your website or contact page
2. Verify the link works before deploying
3. Maintain the existing classes for consistent styling

## Adding Privacy and Terms Pages

### Footer Modification
Add privacy and terms links to the footer:
```html
<div class="grid grid-cols-1 md:grid-cols-3 gap-8">
    <!-- Existing footer content -->
    <div>
        <h3 class="text-lg font-semibold mb-4">Legal</h3>
        <ul class="space-y-2">
            <li><a href="/privacy.html" class="text-gray-400 hover:text-white transition duration-300">Privacy Policy</a></li>
            <li><a href="/terms.html" class="text-gray-400 hover:text-white transition duration-300">Terms of Service</a></li>
        </ul>
    </div>
</div>
```

### Creating Policy Pages
1. Create new files:
   - `privacy.html`
   - `terms.html`
2. Use consistent styling:
   ```html
   <!DOCTYPE html>
   <html lang="en">
   <head>
       <meta charset="UTF-8">
       <meta name="viewport" content="width=device-width, initial-scale=1.0">
       <title>Privacy Policy - Takoma Glass</title>
       <script src="https://cdn.tailwindcss.com"></script>
   </head>
   <body class="font-sans antialiased text-gray-900 bg-white">
       <!-- Copy header from index.html -->
       <main class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-24">
           <h1 class="text-3xl font-bold mb-8">Privacy Policy</h1>
           <!-- Add policy content here -->
       </main>
       <!-- Copy footer from index.html -->
   </body>
   </html>
   ```

## Troubleshooting

Common Issues:
1. **Broken Internal Links**
   - Verify section IDs match href attributes
   - Check for typos in IDs and hrefs
   - Ensure no duplicate IDs exist

2. **Responsive Design Issues**
   - Check mobile view using browser dev tools
   - Verify Tailwind responsive classes:
     - `md:` (768px and up)
     - `lg:` (1024px and up)

3. **Missing Styles**
   - Confirm Tailwind CDN is loading
   - Check for typos in class names
   - Verify class combinations are valid

For additional help:
- Consult [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Use browser developer tools to inspect elements
- Test all links before deploying changes

Remember to:
- Back up files before making changes
- Test on multiple devices and browsers
- Maintain consistent styling throughout
- Update copyright year in footer annually