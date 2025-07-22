# Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Cycle Count Management landing page. Follow these steps to make common updates while preserving the page's design and functionality.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the logo and navigation menu. To update:

1. **Logo Text:**
```html
<a href="/" class="text-2xl font-bold bg-gradient-to-r from-blue-600 to-purple-600 bg-clip-text text-transparent">CCM</a>
```
- Replace "CCM" with your desired logo text
- Keep the classes to maintain the gradient effect

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">FAQ</a>
</div>
```
- Update text between `<a>` tags
- Maintain the `hover:text-gray-900` class for consistent hover effects

### Hero Section
Located at the top of the page:
```html
<h1 class="text-5xl md:text-6xl lg:text-7xl font-bold mb-8 bg-gradient-to-r from-blue-600 to-purple-600 bg-clip-text text-transparent">Cycle Count Management</h1>
<p class="text-2xl md:text-3xl text-gray-600 mb-12">Best of Your Process</p>
```
- Update heading and subheading text
- Keep responsive text classes (`text-5xl md:text-6xl lg:text-7xl`)
- Maintain gradient effect classes

### Features Section
Each feature card follows this structure:
```html
<div class="group p-8 rounded-2xl bg-white border border-gray-100 hover:shadow-xl transition-all duration-300">
    <div class="w-16 h-16 bg-blue-100 rounded-full flex items-center justify-center mb-6">
        <!-- Icon SVG here -->
    </div>
    <h3 class="text-xl font-semibold mb-4">Faster</h3>
    <p class="text-gray-600">Streamline your cycle count process...</p>
</div>
```
To modify:
1. Update the title in the `<h3>` tag
2. Change description text in the `<p>` tag
3. Keep all classes for consistent styling

## Managing Links

### Internal Navigation Links
Current internal links use section IDs:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
```
To update:
1. Locate the section you want to link to
2. Add an `id` attribute to that section
3. Update the `href` to match the new ID
4. Example: `<section id="new-section">` → `<a href="#new-section">`

### External Links
The main call-to-action links point to:
```html
<a href="https://contagemciclica.com.br" class="inline-block px-8 py-4 bg-gradient-to-r from-blue-600 to-purple-600 text-white rounded-full">
```
To update:
1. Replace the URL in `href`
2. Test the new link
3. Maintain all styling classes

## Adding Privacy and Terms Pages

### Footer Link Setup
Current placeholder links in footer:
```html
<ul class="space-y-4">
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>
```

To add proper links:
1. Create new files:
   ```
   privacy.html
   terms.html
   ```

2. Update href attributes:
   ```html
   <a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a>
   <a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a>
   ```

3. Ensure consistent styling by copying these classes to new pages:
   ```html
   class="text-gray-400 hover:text-white transition-colors duration-300"
   ```

## Troubleshooting

### Common Issues

1. **Broken Gradients**
   - Ensure all gradient classes remain intact:
   - `bg-gradient-to-r from-blue-600 to-purple-600`
   - `bg-clip-text text-transparent` (for text gradients)

2. **Responsive Issues**
   - Check media query classes (md:, lg:)
   - Example: `text-5xl md:text-6xl lg:text-7xl`
   - Don't remove responsive classes when updating content

3. **Missing Hover Effects**
   - Verify transition classes are present:
   - `transition-colors duration-300`
   - `hover:text-gray-900`

### Getting Help
- Refer to [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Check class naming conventions
- Test responsiveness using browser dev tools
- Validate HTML at [W3C Validator](https://validator.w3.org/)

Remember to:
- Back up files before making changes
- Test all links after updates
- Check mobile responsiveness
- Maintain consistent styling across pages