# AV Accounting Landing Page - Maintenance Guide

This guide will help you maintain and customize the AV Accounting landing page. Follow these detailed instructions to make common updates while preserving the page's responsive design and functionality.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company logo and navigation menu. To modify:

1. **Company Logo**
```html
<div class="text-2xl font-bold text-blue-600">AV Accounting</div>
```
- Replace "AV Accounting" with your company name
- Adjust size using `text-2xl` (options: text-xl, text-3xl, text-4xl)
- Change color using `text-blue-600` (options: text-[color]-[shade])

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-6">
    Ascot Vale accounting services
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">
    Accounting excellence with a personal touch
</p>
```
To modify:
1. Replace heading and subheading text
2. Maintain responsive classes (`md:text-5xl lg:text-6xl`)
3. Adjust spacing using `mb-` classes (margin-bottom)

### Features Section
Each feature card follows this structure:
```html
<div class="bg-white rounded-xl p-8 shadow-lg hover:shadow-xl transition-shadow duration-300">
    <div class="text-blue-600 mb-4">
        <i class='bx bx-line-chart text-4xl'></i>
    </div>
    <h3 class="text-xl font-bold mb-4">Retirement Planning</h3>
    <p class="text-gray-600">Secure your future with our expert retirement planning services...</p>
</div>
```
To modify:
1. Change icon: Replace `bx-line-chart` with any [Boxicons](https://boxicons.com) class
2. Update heading and description text
3. Maintain padding (`p-8`) and margin (`mb-4`) classes for consistent spacing

## Managing Links

### Navigation Menu Links
Current navigation structure:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Services</a>
    <a href="#benefits" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">FAQ</a>
    <a href="#contact" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Contact</a>
</div>
```
To update links:
1. Internal links (same page):
   - Use `#section-id` format
   - Ensure section IDs match exactly
2. External links:
   - Replace `#` with full URL
   - Add `target="_blank"` for new tab opening

### Call-to-Action Buttons
Current CTA links:
```html
<a href="https://theaccountants.com" class="inline-block bg-blue-600 text-white px-8 py-4 rounded-lg">
    Get Started Today
</a>
```
To update:
1. Replace `https://theaccountants.com` with your booking or contact page URL
2. Maintain all styling classes to preserve button appearance

## Adding Privacy and Terms Pages

### Footer Link Updates
Locate the Legal section in the footer:
```html
<div>
    <h4 class="text-lg font-semibold text-white mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add privacy and terms pages:
1. Create new files:
   ```
   privacy.html
   terms.html
   ```

2. Update footer links:
   ```html
   <li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
   <li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
   ```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Check that section IDs match navigation href attributes exactly
   - Example: `href="#features"` must match `id="features"`

2. **Responsive Design Issues**
   - Maintain responsive classes (md:, lg:)
   - Don't remove `container` or `mx-auto` classes
   - Keep the viewport meta tag in header

3. **Icon Not Showing**
   - Verify Boxicons CSS is loaded
   - Check icon class names on [Boxicons](https://boxicons.com)
   - Ensure `bx` prefix is included

### Style Consistency
When adding new elements:
1. Copy existing element structure
2. Maintain Tailwind class patterns
3. Use the same color scheme:
   - Primary: `blue-600`
   - Text: `gray-600`, `gray-900`
   - Background: `white`, `gray-50`

Need more help? Contact your web development team or refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs).