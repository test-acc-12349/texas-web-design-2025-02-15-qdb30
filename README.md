# Texas Web Design Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Texas Web Design landing page. Whether you're new to web development or need a quick reference, you'll find step-by-step guidance for common maintenance tasks.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company logo and navigation menu. To update:

1. **Company Logo Text**
```html
<!-- Find this line in the header section -->
<a href="/" class="text-2xl font-bold text-gray-800">TWD</a>
```
Simply replace "TWD" with your desired text.

2. **Navigation Menu Items**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```
Replace the text between the `<a>` tags to change menu items.

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-6xl font-bold text-gray-900 mb-6">Texas Web Design</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">Best Websites In Texas</p>
```
- Update the heading by changing "Texas Web Design"
- Modify the subheading by changing "Best Websites In Texas"

### Tailwind CSS Tips
- Font sizes use classes like `text-4xl` (larger) or `text-xl` (smaller)
- Colors use formats like `text-gray-900` (dark) or `text-gray-600` (lighter)
- Spacing uses `mb-6` (margin bottom) or `py-24` (padding top/bottom)
- Responsive design uses `md:` prefix for medium screens and larger

## Managing Links

### External Links
1. **Get Started Button**
```html
<a href="https://twd.com" class="hidden md:inline-block px-6 py-2 bg-blue-600">Get Started</a>
```
Replace `https://twd.com` with your actual website URL.

2. **Contact Email**
```html
<a href="mailto:admin@twd.com">admin@twd.com</a>
```
Update both the `href` and display text with your email address.

### Internal Links
Navigation menu links use hashtags to scroll to sections:
```html
<a href="#features">Features</a>
```
Ensure the `href` matches the `id` of the target section:
```html
<section id="features" class="py-24 bg-white">
```

### Social Media Links
Located in the footer:
```html
<div class="flex space-x-4">
    <a href="#" class="hover:text-white"><i class="fab fa-twitter"></i></a>
    <a href="#" class="hover:text-white"><i class="fab fa-facebook"></i></a>
    <a href="#" class="hover:text-white"><i class="fab fa-linkedin"></i></a>
</div>
```
Replace the `#` with your social media profile URLs.

## Adding Privacy and Terms Pages

### 1. Create New Pages
Create two new files in your website directory:
- `privacy.html`
- `terms.html`

### 2. Update Footer Links
Find these lines in the footer:
```html
<ul class="space-y-2">
    <li><a href="#" class="hover:text-white">Privacy Policy</a></li>
    <li><a href="#" class="hover:text-white">Terms of Service</a></li>
</ul>
```

Replace with:
```html
<ul class="space-y-2">
    <li><a href="privacy.html" class="hover:text-white">Privacy Policy</a></li>
    <li><a href="terms.html" class="hover:text-white">Terms of Service</a></li>
</ul>
```

### 3. Maintain Consistent Styling
When creating privacy.html and terms.html:
- Copy the header and footer from index.html
- Use the same Tailwind CSS classes for consistent styling
- Include the same CSS and Font Awesome links in the `<head>`

## Troubleshooting

### Common Issues

1. **Broken Links**
- Check that all `href` attributes point to valid URLs
- Verify that section IDs match their corresponding links
- Test all links after updating

2. **Styling Problems**
- Ensure Tailwind CSS CDN is properly loaded
- Check for typos in class names
- Verify responsive design classes (md:, lg:) are correct

3. **Missing Icons**
- Confirm Font Awesome CSS is properly linked
- Verify icon class names (e.g., `fa-twitter`)
- Check for updated Font Awesome class naming conventions

### Need Help?
If you encounter issues:
1. Check the browser's developer tools (F12) for errors
2. Verify all CDN links are accessible
3. Test the page across different devices and browsers
4. Ensure all files are in the correct directory structure

Remember to always backup your files before making changes, and test thoroughly after updates.