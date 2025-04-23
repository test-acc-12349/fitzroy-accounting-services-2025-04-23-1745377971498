# Fitzroy Landing Page Maintenance Guide

This guide will help you maintain and customize the Fitzroy Accounting Services landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common updates.

## 1. Updating Text and Tailwind CSS Classes

### Text Content Updates

#### Hero Section
```html
<!-- Located in the main hero section -->
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold">
    Fitzroy accounting services  <!-- Edit this text -->
</h1>
<p class="text-xl md:text-2xl text-gray-400">
    Proactive accounting for forward-thinking businesses  <!-- Edit this text -->
</p>
```

#### Services Section
```html
<!-- Located in the services grid -->
<div class="bg-gray-800 rounded-2xl p-8">
    <h3 class="text-xl font-semibold mb-4">
        Business Valuation  <!-- Edit service title -->
    </h3>
    <p class="text-gray-400">
        Expert analysis and valuation...  <!-- Edit service description -->
    </p>
</div>
```

### Understanding Tailwind Classes

Key classes explained:
- `container mx-auto`: Centers content with automatic margins
- `px-6`: Adds horizontal padding (left and right)
- `py-4`: Adds vertical padding (top and bottom)
- `text-4xl`: Sets large text size (increases with md: and lg: prefixes)
- `bg-gray-800`: Sets background color
- `hover:bg-gray-750`: Changes background color on hover

To modify responsive design:
```html
<!-- Example of responsive classes -->
<div class="text-base md:text-lg lg:text-xl">
    <!-- text-base: Default size -->
    <!-- md:text-lg: Medium screens -->
    <!-- lg:text-xl: Large screens -->
</div>
```

## 2. Fixing Broken Links

### Navigation Menu Links
Current navigation links:
```html
<nav class="container mx-auto px-6 py-4">
    <a href="#services">Services</a>
    <a href="#benefits">Benefits</a>
    <a href="#contact">Contact</a>
    <a href="https://theaccountants.com">Get Started</a>  <!-- Update this URL -->
</nav>
```

To update external links:
1. Locate the `href` attribute
2. Replace `https://theaccountants.com` with your desired URL
3. Ensure URLs include `https://` for external links

### Footer Links
```html
<footer class="bg-gray-800 py-16">
    <ul class="space-y-2 text-gray-400">
        <li><a href="#">About Us</a></li>  <!-- Add proper URLs -->
        <li><a href="#">Careers</a></li>
        <li><a href="#">Contact</a></li>
    </ul>
</footer>
```

To fix footer links:
1. Replace `#` with proper URLs
2. For internal pages: `href="about.html"`
3. For external links: `href="https://example.com"`

## 3. Linking Privacy and Terms Pages

### Adding Privacy Policy Link
```html
<!-- Locate this section in the footer -->
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2 text-gray-400">
        <li>
            <a href="privacy.html" class="hover:text-white transition-colors duration-300">
                Privacy Policy
            </a>
        </li>
    </ul>
</div>
```

### Adding Terms of Service Link
```html
<li>
    <a href="terms.html" class="hover:text-white transition-colors duration-300">
        Terms of Service
    </a>
</li>
```

### Implementation Steps
1. Create `privacy.html` and `terms.html` in your root directory
2. Update the href attributes in the footer
3. Maintain consistent styling by copying these classes:
   - `hover:text-white`
   - `transition-colors`
   - `duration-300`

## Troubleshooting Tips

### Common Issues and Solutions

1. Broken Internal Links
```html
<!-- Wrong -->
<a href="privacy">Privacy Policy</a>

<!-- Correct -->
<a href="privacy.html">Privacy Policy</a>
```

2. Missing Responsive Classes
```html
<!-- Wrong -->
<div class="text-xl">Content</div>

<!-- Correct -->
<div class="text-base md:text-lg lg:text-xl">Content</div>
```

3. Incorrect External Links
```html
<!-- Wrong -->
<a href="www.example.com">Link</a>

<!-- Correct -->
<a href="https://www.example.com">Link</a>
```

### Style Consistency
- Always maintain the dark theme colors (bg-gray-800, bg-gray-900)
- Keep hover effects consistent (hover:text-white, hover:bg-blue-700)
- Preserve responsive design patterns (using md: and lg: prefixes)

## Best Practices
- Test all links after updating
- Maintain consistent spacing using Tailwind's padding/margin classes
- Keep the responsive design intact when modifying classes
- Back up the file before making significant changes
- Validate external URLs before linking
- Keep brand colors consistent throughout the page

Remember to test your changes across different screen sizes to ensure the responsive design remains functional.