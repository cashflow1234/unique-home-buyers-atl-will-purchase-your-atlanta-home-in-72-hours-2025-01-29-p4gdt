# Landing Page Maintenance Guide
## For Unique Home Buyers ATL Website

This guide provides detailed instructions for maintaining and customizing the Unique Home Buyers ATL landing page.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
```html
<div class="text-2xl font-bold text-blue-600">Unique Home Buyers ATL</div>
```
To update the company name:
1. Locate this div in the header section
2. Replace "Unique Home Buyers ATL" with your desired text
3. Adjust text size using these classes:
   - `text-xl` (smaller)
   - `text-2xl` (current size)
   - `text-3xl` (larger)

### Hero Section
The main headline is located here:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8 bg-gradient-to-r from-blue-600 to-purple-600 bg-clip-text text-transparent">
    Unique Home Buyers ATL Will Purchase Your Atlanta Home in 72 Hours
</h1>
```
To modify:
1. Change the text between the `<h1>` tags
2. Adjust responsive text sizes:
   - `text-4xl`: mobile devices
   - `md:text-5xl`: medium screens
   - `lg:text-6xl`: large screens

### Feature Cards
Each feature card follows this structure:
```html
<div class="bg-white rounded-xl shadow-lg p-8 hover:transform hover:scale-105 transition-all duration-300">
    <h3 class="text-xl font-semibold mb-4">All Cash Purchase</h3>
    <p class="text-gray-600">No waiting on lender approvals...</p>
</div>
```
To update:
1. Find the feature card section
2. Modify the `<h3>` text for the title
3. Update the `<p>` text for the description
4. Keep the existing classes for consistent styling

## Fixing Broken Links

### Navigation Menu Links
Current navigation structure:
```html
<div class="hidden lg:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">FAQ</a>
    <a href="#contact" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Contact</a>
</div>
```
To update links:
1. Locate the `href` attribute in each `<a>` tag
2. For internal links (same page sections):
   - Use `#section-id` format
   - Ensure section IDs match exactly
3. For external links:
   - Replace with full URL (e.g., `https://example.com`)

### Call-to-Action Links
Current form link:
```html
<a href="https://form.jotform.com/250276622130043" class="inline-block bg-blue-600 text-white...">
```
To update:
1. Replace the JotForm URL with your new form link
2. Test the link thoroughly before deploying

## Linking Privacy and Terms Pages

### Adding Footer Links
Add these links to the Quick Links section:
```html
<div>
    <h3 class="text-xl font-bold mb-4">Quick Links</h3>
    <ul class="space-y-2">
        <!-- Existing links -->
        <li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Verify that section IDs match href attributes exactly
   - Section IDs are case-sensitive
   ```html
   <!-- Example fix -->
   <a href="#features">Features</a>
   <section id="features">...</section>
   ```

2. **Responsive Design Issues**
   - Check responsive classes are properly ordered:
   ```html
   <!-- Correct order -->
   class="text-base md:text-lg lg:text-xl"
   ```

3. **Style Inconsistencies**
   - Copy existing classes for new elements
   - Maintain color scheme using these classes:
     - Primary blue: `text-blue-600`
     - Gray text: `text-gray-600`
     - White backgrounds: `bg-white`

### Need Help?
- Check the Tailwind CSS documentation for class references
- Verify all links using browser developer tools
- Test responsive design using browser device emulation

Remember to always backup your files before making changes, and test thoroughly in multiple browsers before deploying updates.