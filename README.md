# Sydney Website Design - Landing Page Maintenance Guide

This guide will help you maintain and customize the Sydney Website Design landing page. Whether you're new to web development or need a quick reference, follow these instructions to make updates safely and effectively.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains your logo and navigation menu. To update:

1. **Logo Text**
```html
<!-- Find this line in the header -->
<a href="/" class="text-2xl font-bold text-blue-600">SWD</a>
```
- Replace "SWD" with your desired logo text
- Adjust size using `text-2xl` (options: text-sm, text-lg, text-3xl, etc.)

2. **Navigation Menu Items**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="hover:text-blue-600 transition-colors duration-300">Features</a>
    <!-- Additional menu items -->
</div>
```
- Update text between `>` and `</a>` tags
- Keep the `hover:text-blue-600` class for consistent hover effects

### Hero Section
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-6 text-gray-900">Sydney Website Design</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-10">Best Websites On The East Coast</p>
```
- Update heading text between `<h1>` tags
- Modify subheading text between `<p>` tags
- Classes explained:
  - `text-4xl`: Base text size
  - `md:text-5xl`: Tablet size
  - `lg:text-6xl`: Desktop size

### Features Section
To update feature cards:
```html
<div class="p-8 rounded-2xl bg-white shadow-lg hover:shadow-xl transition-shadow duration-300">
    <div class="w-16 h-16 bg-blue-100 rounded-full flex items-center justify-center mb-6">
        <i class="fas fa-paint-brush text-2xl text-blue-600"></i>
    </div>
    <h3 class="text-xl font-bold mb-4">Custom Design</h3>
    <p class="text-gray-600">Unique, tailored designs...</p>
</div>
```
- Change icons by updating `fa-paint-brush` to other [Font Awesome](https://fontawesome.com/icons) classes
- Modify headings in `<h3>` tags
- Update descriptions in `<p>` tags

## Fixing Broken Links

### Navigation Menu Links
Current links in the navigation:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```
To update:
1. Replace `#features` with your new section ID or URL
2. Ensure section IDs match exactly (case-sensitive)
3. For external links, use complete URLs: `https://example.com`

### Call-to-Action Buttons
```html
<a href="https://swd.com" class="inline-block px-8 py-4 bg-blue-600">Start Your Project</a>
```
Replace `https://swd.com` with your actual website URL or contact form link

### Footer Links
```html
<ul class="space-y-2 text-gray-400">
    <li><a href="#" class="hover:text-white transition-colors duration-300">About Us</a></li>
    <li><a href="#" class="hover:text-white transition-colors duration-300">Services</a></li>
    <li><a href="#" class="hover:text-white transition-colors duration-300">Portfolio</a></li>
</ul>
```
Replace `#` with actual page URLs:
- Internal pages: `/about.html`
- External links: `https://example.com/page`

## Linking Privacy and Terms Pages

### Adding Privacy Policy Link
1. Locate the footer's legal section:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2 text-gray-400">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
```
2. Update the href attribute:
```html
<li><a href="/privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
```

### Adding Terms of Service Link
```html
<li><a href="/terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
- Ensure file names match exactly
- Check that files are in the correct directory
- Verify that IDs match section IDs (e.g., `#features` matches `id="features"`)

2. **Responsive Design Issues**
- Don't remove `md:` or `lg:` prefixes from classes
- Keep the `container` class on parent elements
- Maintain the responsive grid classes (`grid-cols-1 md:grid-cols-3`)

3. **Icon Problems**
- Verify Font Awesome is properly loaded
- Check icon class names on [Font Awesome's website](https://fontawesome.com)
- Ensure the correct icon style prefix is used (fas, far, fab)

### Need Help?
If you encounter issues:
1. Check the browser's developer tools (F12) for errors
2. Verify all files are in the correct location
3. Ensure all HTML tags are properly closed
4. Maintain the existing class structure when making changes

Remember to always test your changes across different device sizes using browser developer tools.