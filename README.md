# KeywordPro Landing Page - Maintenance Guide

This guide will help you maintain and customize the KeywordPro landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions to make updates safely and effectively.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To update:

1. **Company Name:**
```html
<a href="/" class="text-xl font-bold tracking-tight">KeywordPro</a>
```
- Replace "KeywordPro" with your desired company name
- Keep the classes unchanged to maintain styling

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">FAQ</a>
</div>
```
- Update text between `<a>` tags
- Keep the `href` attributes matching your section IDs
- Maintain the Tailwind classes for consistent styling

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold tracking-tight mb-6">
    Unlock Top Keywords: Your Go-To Search Tool
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-10">
    Uncover the Keywords That Drive Growth
</p>
```
- Update heading and subheading text as needed
- The `text-4xl md:text-5xl lg:text-6xl` classes control text size across different screen sizes
- Don't remove responsive classes (those starting with `md:` or `lg:`)

### Features and Benefits Sections
Each feature/benefit card follows this structure:
```html
<div class="p-8 rounded-2xl bg-gray-50 hover:bg-gray-100 transition-all duration-300">
    <i class='bx bx-analyse text-4xl text-gray-900 mb-4'></i>
    <h3 class="text-xl font-semibold mb-4">In-depth Analysis</h3>
    <p class="text-gray-600">Comprehensive keyword analysis with detailed metrics and insights.</p>
</div>
```
To modify:
1. Change the icon by updating the `bx-analyse` class to another [Boxicons](https://boxicons.com/) name
2. Update the heading text within `<h3>` tags
3. Modify the description within `<p>` tags
4. Keep all Tailwind classes intact for consistent styling

## Managing Links

### Navigation Links
Current navigation links are:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
```
To update:
1. Ensure the `href` matches the `id` of the target section
2. For external links, use complete URLs: `href="https://example.com"`
3. For internal pages, use relative paths: `href="/about.html"`

### Call-to-Action (CTA) Links
Currently pointing to:
```html
<a href="https://wisdom31.com/" class="inline-flex items-center px-8 py-3 bg-gray-900 text-white">
```
To update:
1. Replace `https://wisdom31.com/` with your desired URL
2. Test the link before deploying
3. Maintain all classes to preserve button styling

### Social Media Links
Located in the footer:
```html
<div class="flex space-x-4">
    <a href="#" class="text-gray-600 hover:text-gray-900"><i class='bx bxl-twitter text-xl'></i></a>
    <a href="#" class="text-gray-600 hover:text-gray-900"><i class='bx bxl-linkedin text-xl'></i></a>
    <a href="#" class="text-gray-600 hover:text-gray-900"><i class='bx bxl-facebook text-xl'></i></a>
</div>
```
Replace the `#` with your social media profile URLs.

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
1. Create two new files in your project directory:
   - `privacy.html`
   - `terms.html`

### Step 2: Update Footer Links
Replace the placeholder links with:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2 text-gray-600">
        <li><a href="/privacy.html" class="hover:text-gray-900">Privacy Policy</a></li>
        <li><a href="/terms.html" class="hover:text-gray-900">Terms of Service</a></li>
    </ul>
</div>
```

### Step 3: Style Consistency
Ensure your new pages maintain consistent styling by:
1. Copying the header and footer from `index.html`
2. Using the same Tailwind CSS classes for text and spacing
3. Following the same responsive design patterns

## Troubleshooting

### Common Issues:

1. **Broken Layout:**
   - Check that all Tailwind classes remain intact
   - Verify that `<div>` tags are properly closed
   - Ensure the TailwindCSS CDN link is working:
   ```html
   <script src="https://cdn.tailwindcss.com"></script>
   ```

2. **Icons Not Showing:**
   - Verify the Boxicons CDN link:
   ```html
   <link href="https://unpkg.com/boxicons@2.1.4/css/boxicons.min.css" rel="stylesheet">
   ```
   - Check icon class names against [Boxicons documentation](https://boxicons.com/)

3. **Links Not Working:**
   - Verify that section IDs match their corresponding href attributes
   - Check for typos in URLs
   - Ensure relative paths start with `/` for root-relative links

Remember to test all changes in multiple browsers and screen sizes before deploying to production.