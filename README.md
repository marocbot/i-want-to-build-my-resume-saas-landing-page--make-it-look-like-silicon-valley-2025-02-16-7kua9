# Landing Page Maintenance Guide

This guide will help you maintain and customize the ResumePro landing page. It's written for beginners with no prior coding experience.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the logo and navigation menu. To modify:

1. **Logo Text**: Find this line and replace "ResumePro":
```html
<span class="text-2xl font-bold text-indigo-600">ResumePro</span>
```

2. **Navigation Menu Items**: Locate the navigation section:
```html
<div class="hidden md:flex items-center space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
</div>
```
To change menu items, modify the text between `<a>` tags.

### Hero Section
To update the main headline:
```html
<h1 class="text-4xl tracking-tight font-extrabold text-gray-900 sm:text-5xl md:text-6xl">
    <span class="block">Build your Resume</span>
    <span class="block text-indigo-600">Silicon Valley Style</span>
</h1>
```

### Tailwind CSS Tips
- Font sizes use classes like `text-sm`, `text-base`, `text-lg`, `text-xl`
- Colors use format `text-{color}-{shade}` (e.g., `text-indigo-600`)
- Spacing uses format `p-{number}` for padding, `m-{number}` for margin
- Responsive classes start with screen sizes: `sm:`, `md:`, `lg:`, `xl:`

## Managing Links

### Current Link Locations

1. **Navigation Menu Links**:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="https://buy.stripe.com/6oE17Y2hFard6Pu5kk">Get Started</a>
```

2. **Call-to-Action Links**:
```html
<a href="https://buy.stripe.com/6oE17Y2hFard6Pu5kk" class="w-full flex items-center...">
    Get Started
</a>
```

### Updating Links
1. Internal links (starting with #) point to section IDs
2. External links need full URLs
3. To update the Stripe payment link:
   - Find all instances of `https://buy.stripe.com/6oE17Y2hFard6Pu5kk`
   - Replace with your new payment link
   - Use search (Ctrl+F/Cmd+F) to find all instances

## Adding Privacy and Terms Pages

### Footer Modification
Add privacy and terms links in the footer support section:

```html
<div class="md:grid md:grid-cols-2 md:gap-8">
    <div>
        <h3 class="text-sm font-semibold text-gray-400 tracking-wider uppercase">
            Support
        </h3>
        <ul class="mt-4 space-y-4">
            <li>
                <a href="mailto:technik.adisam@gmail.com" class="text-base text-gray-300 hover:text-white">
                    Contact Us
                </a>
            </li>
            <!-- Add these new links -->
            <li>
                <a href="privacy.html" class="text-base text-gray-300 hover:text-white">
                    Privacy Policy
                </a>
            </li>
            <li>
                <a href="terms.html" class="text-base text-gray-300 hover:text-white">
                    Terms of Service
                </a>
            </li>
        </ul>
    </div>
</div>
```

## Troubleshooting

### Common Issues

1. **Broken Layout**
   - Check for missing closing tags
   - Verify Tailwind CSS classes are spelled correctly
   - Ensure responsive classes (sm:, md:, lg:) are in correct order

2. **Links Not Working**
   - Verify file names match exactly (case-sensitive)
   - Check that files are in the correct directory
   - Ensure internal links (#) match section IDs

3. **Images Not Displaying**
   - Verify image URLs are correct
   - Check image paths if hosted locally
   - Ensure images are uploaded to the correct location

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Validate HTML at [W3C Validator](https://validator.w3.org/)
- Contact support at the email provided in the footer

Remember to always test changes across different screen sizes using your browser's developer tools (F12).