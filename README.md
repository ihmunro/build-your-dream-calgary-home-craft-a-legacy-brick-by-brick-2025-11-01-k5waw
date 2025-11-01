# Calgary Dream Homes Landing Page - Maintenance & Customization Guide

Welcome! This comprehensive guide will help you maintain and customize the Calgary Dream Homes landing page. Whether you're updating text, fixing links, or adding new pages, you'll find step-by-step instructions designed for beginners.

---

## Table of Contents

1. [Getting Started](#getting-started)
2. [Understanding the Page Structure](#understanding-the-page-structure)
3. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
4. [Fixing Broken Links](#fixing-broken-links)
5. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
6. [Troubleshooting](#troubleshooting)
7. [Best Practices](#best-practices)

---

## Getting Started

### What You'll Need

- A text editor (we recommend [Visual Studio Code](https://code.visualstudio.com/), [Sublime Text](https://www.sublimetext.com/), or even Notepad)
- The `index.html` file
- Basic familiarity with opening and saving files
- A web browser to preview changes

### How to Open and Edit the File

1. **Right-click** on your `index.html` file
2. Select **"Open with"** and choose your text editor
3. The file will open in the editor, showing all the code
4. Make your changes (we'll guide you through this)
5. **Save** the file using `Ctrl+S` (Windows) or `Cmd+S` (Mac)
6. **Refresh** your web browser to see the changes

> **Pro Tip:** After making changes, always save the file and refresh your browser to see the updates immediately.

---

## Understanding the Page Structure

Before making edits, let's understand how the page is organized. The landing page has several main sections:

### Page Sections Overview

```
├── Header Navigation (sticky at top)
├── Hero Section (large banner with main message)
├── Features Section (6 service cards)
├── Benefits Section (6 benefit items)
├── Testimonials Section (4 customer reviews)
├── About Us Section (company information)
├── Trust & Credibility Section (certifications)
├── Call-to-Action Section (final push to convert)
└── Footer (contact info and links)
```

Each section has:
- **An ID** (like `id="features"`) - used for navigation links
- **Heading text** - the main title
- **Body text** - descriptive content
- **Links** - buttons and navigation elements
- **Tailwind CSS classes** - styling instructions

### Key Concept: Tailwind CSS Classes

This page uses **Tailwind CSS**, a system of pre-made styling classes. Instead of writing custom CSS, we use class names like:

- `text-4xl` = large text (4xl size)
- `font-bold` = bold text
- `text-white` = white text color
- `bg-purple-600` = purple background
- `px-8` = horizontal padding (left and right)
- `py-4` = vertical padding (top and bottom)
- `rounded-lg` = slightly rounded corners
- `hover:text-purple-600` = turns purple when you hover over it

**Don't worry if this seems complex!** We'll show you exactly what to change for each task.

---

## Updating Text and Tailwind CSS Classes

### Section 1: Header Navigation

The header appears at the very top of the page and stays visible as you scroll.

#### Location in Code
Find this section near the top of your file (around line 36):

```html
<header class="sticky top-0 z-50 bg-white shadow-md">
    <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex items-center justify-between">
        <div class="flex items-center space-x-2">
            <div class="w-10 h-10 hero-gradient rounded-lg flex items-center justify-center">
                <i class="fas fa-home text-white text-lg"></i>
            </div>
            <span class="text-xl font-bold text-gray-900">Calgary Dream Homes</span>
        </div>
```

#### How to Update the Company Name

1. Find the text `Calgary Dream Homes` in the header
2. **Replace it** with your company name
3. Keep the surrounding code exactly the same
4. Save and refresh your browser

**Example:**
```html
<!-- BEFORE -->
<span class="text-xl font-bold text-gray-900">Calgary Dream Homes</span>

<!-- AFTER (if your company is "Dream Builder Inc.") -->
<span class="text-xl font-bold text-gray-900">Dream Builder Inc.</span>
```

#### How to Update Navigation Menu Items

The navigation menu has 4 links. Find them around line 50-54:

```html
<a href="#features" class="text-gray-700 hover:text-purple-600 font-medium transition-colors duration-300">Features</a>
<a href="#benefits" class="text-gray-700 hover:text-purple-600 font-medium transition-colors duration-300">Benefits</a>
<a href="#testimonials" class="text-gray-700 hover:text-purple-600 font-medium transition-colors duration-300">Testimonials</a>
<a href="#about" class="text-gray-700 hover:text-purple-600 font-medium transition-colors duration-300">About</a>
```

**To change a menu label:**

1. Find the text between `>` and `</a>` (this is the visible text)
2. Replace it with your new text
3. **Keep the `href="#..."` part unchanged** (this tells the link where to go)

**Example:**
```html
<!-- BEFORE -->
<a href="#features" class="text-gray-700 hover:text-purple-600 font-medium transition-colors duration-300">Features</a>

<!-- AFTER (if you want to call it "Our Services") -->
<a href="#features" class="text-gray-700 hover:text-purple-600 font-medium transition-colors duration-300">Our Services</a>
```

> **Important:** The `#features` part must match the `id="features"` in the Features Section below. We'll show you how to verify this later.

---

### Section 2: Hero Section (Main Banner)

The hero section is the large colorful banner with the main headline. Find it around line 70.

#### Current Hero Text

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight tracking-tight mb-6">
    Build Your Dream Calgary Home
</h1>
<h2 class="text-xl md:text-2xl font-light leading-relaxed mb-8 text-purple-100">
    Craft a Legacy, Brick by Brick
</h2>
<p class="text-lg md:text-xl leading-relaxed mb-12 text-purple-50 max-w-3xl mx-auto">
    Imagine waking up in a home perfectly tailored to your life. We transform your vision into a stunning reality, exceeding expectations from concept to completion.
</p>
```

#### How to Update Hero Headline

1. Find the text `Build Your Dream Calgary Home`
2. Replace it with your company's main message
3. Save and refresh

**Example:**
```html
<!-- BEFORE -->
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight tracking-tight mb-6">
    Build Your Dream Calgary Home
</h1>

<!-- AFTER -->
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight tracking-tight mb-6">
    Premium Custom Homes Built for You
</h1>
```

#### How to Update Hero Subheading

Find `Craft a Legacy, Brick by Brick` and replace it similarly.

#### How to Update Hero Description

Replace the paragraph text while keeping all the class names intact.

#### Understanding Responsive Text Sizes

Notice these classes in the hero section: `text-4xl md:text-5xl lg:text-6xl`

This means:
- **Mobile phones:** `text-4xl` (medium size)
- **Tablets (md):** `text-5xl` (larger)
- **Desktop (lg):** `text-6xl` (largest)

**Don't change these classes** unless you want different sizes on different devices. Just update the text content.

---

### Section 3: Features Section (6 Service Cards)

The Features section starts around line 100. It contains 6 cards describing your services.

#### Location of Features Section Header

```html
<section id="features" class="py-24 bg-gray-50">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center mb-16">
            <h2 class="text-4xl md:text-5xl font-bold text-gray-900 mb-4">
                Our Premium Services
            </h2>
            <p class="text-xl text-gray-600 max-w-2xl mx-auto">
                Discover what sets us apart in the custom home building industry
            </p>
        </div>
```

#### How to Update Section Title and Description

1. Find `Our Premium Services` and replace with your title
2. Find the description text below it and update as needed
3. Keep all the class names the same

**Example:**
```html
<!-- BEFORE -->
<h2 class="text-4xl md:text-5xl font-bold text-gray-900 mb-4">
    Our Premium Services
</h2>
<p class="text-xl text-gray-600 max-w-2xl mx-auto">
    Discover what sets us apart in the custom home building industry
</p>

<!-- AFTER -->
<h2 class="text-4xl md:text-5xl font-bold text-gray-900 mb-4">
    What We Offer
</h2>
<p class="text-xl text-gray-600 max-w-2xl mx-auto">
    Industry-leading services tailored to your needs
</p>
```

#### How to Update Individual Feature Cards

Each feature card looks like this (around line 115):

```html
<div class="feature-card bg-white p-8 rounded-xl shadow-md hover:shadow-xl transition-all duration-300">
    <div class="w-16 h-16 hero-gradient rounded-lg flex items-center justify-center mb-6">
        <i class="fas fa-pencil-ruler text-white text-2xl"></i>
    </div>
    <h3 class="text-2xl font-bold text-gray-900 mb-4">Design-Driven Approach</h3>
    <p class="text-gray-600 leading-relaxed mb-4">
        Collaborate with our award-winning architects...
    </p>
    <ul class="space-y-2 text-gray-600">
        <li class="flex items-start"><i class="fas fa-check text-purple-600 mr-3 mt-1"></i><span>Custom architectural designs</span></li>
        <li class="flex items-start"><i class="fas fa-check text-purple-600 mr-3 mt-1"></i><span>Award-winning design team</span></li>
        <li class="flex items-start"><i class="fas fa-check text-purple-600 mr-3 mt-1"></i><span>Personalized consultation process</span></li>
    </ul>
</div>
```

**To update a feature card:**

1. **Update the title:** Find `Design-Driven Approach` and replace it
2. **Update the description:** Replace the paragraph text
3. **Update the bullet points:** Replace each item in the `<li>` tags

**Example:**
```html
<!-- BEFORE -->
<h3 class="text-2xl font-bold text-gray-900 mb-4">Design-Driven Approach</h3>
<p class="text-gray-600 leading-relaxed mb-4">
    Collaborate with our award-winning architects...
</p>

<!-- AFTER -->
<h3 class="text-2xl font-bold text-gray-900 mb-4">Expert Design Team</h3>
<p class="text-gray-600 leading-relaxed mb-4">
    Work with our talented designers to create your perfect space...
</p>
```

#### How to Change Feature Card Icons

Each card has an icon. For example: `<i class="fas fa-pencil-ruler text-white text-2xl"></i>`

This uses Font Awesome icons. To change the icon:

1. Visit [Font Awesome Free Icons](https://fontawesome.com/icons)
2. Search for an icon you like
3. Copy the icon name (e.g., `fa-pencil-ruler`)
4. Replace the icon name in your code

**Example:**
```html
<!-- BEFORE (pencil/ruler icon) -->
<i class="fas fa-pencil-ruler text-white text-2xl"></i>

<!-- AFTER (lightbulb icon) -->
<i class="fas fa-lightbulb text-white text-2xl"></i>

<!-- AFTER (star icon) -->
<i class="fas fa-star text-white text-2xl"></i>
```

> **Note:** The classes `text-white text-2xl` make the icon white and size 2xl. Don't change these unless you want different styling.

---

### Section 4: Benefits Section

The Benefits section starts around line 200 and shows 6 benefits with icons.

#### How to Update Benefits Section

The structure is similar to features:

```html
<section id="benefits" class="py-24 bg-white">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="text-center mb-16">
            <h2 class="text-4xl md:text-5xl font-bold text-gray-900 mb-4">
                Why Choose Calgary Dream Homes?
            </h2>
            <p class="text-xl text-gray-600 max-w-2xl mx-auto">
                Experience transformative benefits that go beyond just building a house
            </p>
        </div>
```

**Update the title and description** just like you did for the Features section.

#### Updating Individual Benefit Items

Each benefit looks like this (around line 220):

```html
<div class="flex gap-6">
    <div class="flex-shrink-0">
        <div class="flex items-center justify-center h-14 w-14 rounded-lg hero-gradient">
            <i class="fas fa-chart-line text-white text-2xl"></i>
        </div>
    </div>
    <div>
        <h3 class="text-2xl font-bold text-gray-900 mb-3">Enjoy Lasting Value</h3>
        <p class="text-gray-600 leading-relaxed mb-4">
            Increase your property value significantly...
        </p>
        <ul class="space-y-2 text-gray-600 text-sm">
            <li><i class="fas fa-check text-purple-600 mr-2"></i>Higher property valuations</li>
            <li><i class="fas fa-check text-purple-600 mr-2"></i>Investment-grade construction</li>
            <li><i class="fas fa-check text-purple-600 mr-2"></i>Strong resale potential</li>
        </ul>
    </div>
</div>
```

**To update a benefit:**

1. Change the icon (same process as features)
2. Replace the title text
3. Replace the description paragraph
4. Update the bullet points in the `<li>` tags

---

### Section 5: Testimonials Section

The Testimonials section starts around line 310 and shows 4 customer reviews.

#### How to Update Testimonials

Each testimonial card looks like this:

```html
<div class="testimonial-card bg-white p-8 rounded-xl shadow-md">
    <div class="flex items-center gap-1 mb-4">
        <i class="fas fa-star text-yellow-400"></i>
        <i class="fas fa-star text-yellow-400"></i>
        <i class="fas fa-star text-yellow-400"></i>
        <i class="fas fa-star text-yellow-400"></i>
        <i class="fas fa-star text-yellow-400"></i>
    </div>
    <p class="text-gray-700 leading-relaxed mb-6">
        "The attention to detail was impeccable..."
    </p>
    <div class="border-t pt-4">
        <p class="font-bold text-gray-900">Sarah Miller</p>
        <p class="text-gray-600 text-sm">Marketing Director, Tech Solutions Inc.</p>
    </div>
</div>
```

**To update a testimonial:**

1. **Replace the quote text** (the text in quotation marks)
2. **Replace the customer name** (e.g., "Sarah Miller")
3. **Replace the job title/company** (e.g., "Marketing Director, Tech Solutions Inc.")

**Example:**
```html
<!-- BEFORE -->
<p class="text-gray-700 leading-relaxed mb-6">
    "The attention to detail was impeccable. They truly listened to our vision..."
</p>
<div class="border-t pt-4">
    <p class="font-bold text-gray-900">Sarah Miller</p>
    <p class="text-gray-600 text-sm">Marketing Director, Tech Solutions Inc.</p>
</div>

<!-- AFTER -->
<p class="text-gray-700 leading-relaxed mb-6">
    "Outstanding work! This team exceeded all our expectations and delivered on time."
</p>
<div class="border-t pt-4">
    <p class="font-bold text-gray-900">John Anderson</p>
    <p class="text-gray-600 text-sm">Real Estate Agent, Premier Properties</p>
</div>
```

#### How to Change Star Ratings

To change from 5 stars to 4 stars, simply remove one star line:

```html
<!-- BEFORE (5 stars) -->
<div class="flex items-center gap-1 mb-4">
    <i class="fas fa-star text-yellow-400"></i>
    <i class="fas fa-star text-yellow-400"></i>
    <i class="fas fa-star text-yellow-400"></i>
    <i class="fas fa-star text-yellow-400"></i>
    <i class="fas fa-star text-yellow-400"></i>
</div>

<!-- AFTER (4 stars - remove one line) -->
<div class="flex items-center gap-1 mb-4">
    <i class="fas fa-star text-yellow-400"></i>
    <i class="fas fa-star text-yellow-400"></i>
    <i class="fas fa-star text-yellow-400"></i>
    <i class="fas fa-star text-yellow-400"></i>
</div>
```

---

### Section 6: About Us Section

The About Us section starts around line 390.

#### How to Update About Us Content

```html
<section id="about" class="py-24 bg-white">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
            <div>
                <h2 class="text-4xl md:text-5xl font-bold text-gray-900 mb-8">
                    About Calgary Dream Homes
                </h2>
                <p class="text-lg text-gray-600 leading-relaxed mb-6">
                    Founded in 2008, Calgary Dream Homes emerged from a simple yet powerful vision...
                </p>
                <p class="text-lg text-gray-600 leading-relaxed">
                    Our core mission is to build homes that inspire...
                </p>
            </div>
```

**To update About Us:**

1. Replace the section title
2. Replace the paragraph text (keep the `<p>` tags)
3. Add more paragraphs if needed by copying a `<p>` tag and updating the text

**Example:**
```html
<!-- BEFORE -->
<h2 class="text-4xl md:text-5xl font-bold text-gray-900 mb-8">
    About Calgary Dream Homes
</h2>

<!-- AFTER -->
<h2 class="text-4xl md:text-5xl font-bold text-gray-900 mb-8">
    Our Story
</h2>
```

---

### Section 7: Trust & Credibility Section

This section (around line 430) shows your certifications and partnerships.

#### How to Update Certifications

```html
<div class="bg-white p-8 rounded-lg shadow-md text-center">
    <div class="w-16 h-16 hero-gradient rounded-full flex items-center justify-center mx-auto mb-4">
        <i class="fas fa-certificate text-white text-2xl"></i>
    </div>
    <h3 class="text-xl font-bold text-gray-900 mb-2">Calgary Home Builders' Association</h3>
    <p class="text-gray-600">Member in Good Standing with full compliance to industry standards and ethics</p>
</div>
```

**To update a certification:**

1. Change the icon if desired
2. Replace the certification name
3. Replace the description text

---

### Section 8: Call-to-Action Section

The CTA section (around line 470) is the final push before the footer.

#### How to Update CTA Section

```html
<h2 class="text-4xl md:text-5xl font-bold text-white mb-6">
    Ready to Build Your Dream Home?
</h2>
<p class="text-xl text-purple-100 mb-8 max-w-2xl mx-auto">
    Let's start a conversation about your vision...
</p>
```

Simply replace the text while keeping the class names intact.

---

### Section 9: Footer

The footer (around line 500) contains company info, links, and contact details.

#### How to Update Footer Company Name

```html
<div class="flex items-center space-x-2 mb-6">
    <div class="w-10 h-10 hero-gradient rounded-lg flex items-center justify-center">
        <i class="fas fa-home text-white text-lg"></i>
    </div>
    <span class="text-xl font-bold text-white">Calgary Dream Homes</span>
</div>
```

Replace `Calgary Dream Homes` with your company name.

#### How to Update Footer Description

```html
<p class="text-gray-400 leading-relaxed">
    Building premium custom homes in Calgary with excellence, sustainability, and innovation.
</p>
```

Replace this text with your company description.

#### How to Update Contact Information

```html
<p class="flex items-start gap-3">
    <i class="fas fa-envelope text-purple-500 mt-1"></i>
    <a href="mailto:test@test.com" class="text-gray-400 hover:text-white transition-colors duration-300">test@test.com</a>
</p>
<p class="flex items-start gap-3">
    <i class="fas fa-map-marker-alt text-purple-500 mt-1"></i>
    <span class="text-gray-400">Calgary, Alberta, Canada</span>
</p>
```

**To update email:**
- Replace `test@test.com` in both places (the `href` and the visible text)

**To update address:**
- Replace `Calgary, Alberta, Canada` with your address

---

## Fixing Broken Links

A "broken link" is a link that doesn't go anywhere or goes to the wrong place. Let's identify and fix all the links on this page.

### Understanding Links

A link in HTML looks like this:

```html
<a href="https://example.com" class="...">Click Here</a>
```

- **`<a>`** = starts a link
- **`href="..."`** = where the link goes
- **`</a>`** = ends the link
- **Text between `<a>` and `</a>`** = what you see on the page

### Types of Links on This Page

1. **Internal links** - go to sections on the same page (start with `#`)
2. **External links** - go to other websites (start with `https://` or `http://`)
3. **Email links** - send an email (start with `mailto:`)

---

### Navigation Menu Links (Header)

Located around line 50-54 in the header:

```html
<a href="#features" class="text-gray-700 hover:text-purple-600 font-medium transition-colors duration-300">Features</a>
<a href="#benefits" class="text-gray-700 hover:text-purple-600 font-medium transition-colors duration-300">Benefits</a>
<a href="#testimonials" class="text-gray-700 hover:text-purple-600 font-medium transition-colors duration-300">Testimonials</a>
<a href="#about" class="text-gray-700 hover:text-purple-600 font-medium transition-colors duration-300">About</a>
```

#### Verify Navigation Links Are Working

These links should go to sections with matching IDs. Let's verify:

1. **Features link** (`#features`) should match `<section id="features">` ✓ (Found at line 100)
2. **Benefits link** (`#benefits`) should match `<section id="benefits">` ✓ (Found at line 200)
3. **Testimonials link** (`#testimonials`) should match `<section id="testimonials">` ✓ (Found at line 310)
4. **About link** (`#about`) should match `<section id="about">` ✓ (Found at line 390)

All navigation links are correct! They should work fine.

#### If Navigation Links Don't Work

If clicking a navigation link doesn't scroll to the section, check:

1. **Verify the section ID exists:**
   - Search for `<section id="features">` (for example)
   - If you don't find it, the link is broken

2. **Fix by adding the ID if missing:**
   ```html
   <!-- BROKEN (no id) -->
   <section class="py-24 bg-gray-50">

   <!-- FIXED (add id) -->
   <section id="features" class="py-24 bg-gray-50">
   ```

3. **Make sure the ID matches the link:**
   ```html
   <!-- These must match -->
   <a href="#features">Features</a>  <!-- link -->
   <section id="features">           <!-- section -->
   ```

---

### Call-to-Action Buttons

The page has several "Get Started" or "Start Your Journey" buttons. These are currently placeholder links.

#### Locations of CTA Buttons

**Button 1 - Header (around line 56):**
```html
<a href="https://example.com" class="bg-gradient-to-r from-purple-600 to-purple-800 text-white px-6 py-2 rounded-lg hover:shadow-lg cta-button">Get Started</a>
```

**Button 2 - Hero Section (around line 85):**
```html
<a href="https://example.com" class="bg-white text-purple-700 px-8 py-4 rounded-lg font-bold text-lg hover:shadow-xl cta-button inline-block transition-all duration-300">
    Start Your Journey
</a>
```

**Button 3 - CTA Section (around line 480):**
```html
<a href="https://example.com" class="bg-white text-purple-700 px-8 py-4 rounded-lg font-bold text-lg hover:shadow-xl cta-button inline-block transition-all duration-300">
    Schedule Consultation
</a>
```

#### How to Fix CTA Button Links

1. **Find all instances of `href="https://example.com"`** in your file
2. **Replace `https://example.com`** with your actual URL

**Example:**
```html
<!-- BEFORE (placeholder) -->
<a href="https://example.com" class="...">Get Started</a>

<!-- AFTER (real link to contact form) -->
<a href="https://yourwebsite.com/contact" class="...">Get Started</a>

<!-- OR link to an external booking site -->
<a href="https://calendly.com/yourname" class="...">Get Started</a>
```

#### Quick Reference: Where to Put Your Link

- **Your website's contact form:** `https://yourwebsite.com/contact`
- **Calendly booking:** `https://calendly.com/yourname`
- **Booking service:** `https://www.acuityscheduling.com/yourname`
- **Your email:** `mailto:your@email.com`

---

### Mobile Menu Links

The mobile menu (around line 61-70) has the same navigation links. They should already be correct if you verified the desktop menu.

```html
<a href="#features" class="text-gray-700 hover:text-purple-600 font-medium transition-colors duration-300">Features</a>
<a href="#benefits" class="text-gray-700 hover:text-purple-600 font-medium transition-colors duration-300">Benefits</a>
<a href="#testimonials" class="text-gray-700 hover:text-purple-600 font-medium transition-colors duration-300">Testimonials</a>
<a href="#about" class="text-gray-700 hover:text-purple-600 font-medium transition-colors duration-300">About</a>
```

---

### Footer Links

#### Quick Links Section (around line 525)

```html
<li><a href="#features" class="text-gray-400 hover:text-white transition-colors duration-300">Our Services</a></li>
<li><a href="#benefits" class="text-gray-400 hover:text-white transition-colors duration-300">Benefits</a></li>
<li><a href="#testimonials" class="text-gray-400 hover:text-white transition-colors duration-300">Testimonials</a></li>
<li><a href="#about" class="text-gray-400 hover:text-white transition-colors duration-300">About Us</a></li>
```

These are all correct (same as navigation menu).

#### Resources Section (around line 535)

```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
<li><a href="blog.html" class="text-gray-400 hover:text-white transition-colors duration-300">Blog</a></li>
<li><a href="https://example.com" class="text-gray-400 hover:text-white transition-colors duration-300">Portfolio</a></li>
```

**These links are placeholders and need to be fixed:**

1. **`privacy.html`** - This file should exist in the same folder as `index.html`
2. **`terms.html`** - This file should exist in the same folder as `index.html`
3. **`blog.html`** - This file should exist in the same folder as `index.html`
4. **`https://example.com`** - Replace with your actual portfolio URL

We'll show you how to create these files in the next section.

#### Contact Information (around line 545)

```html
<a href="mailto:test@test.com" class="text-gray-400 hover:text-white transition-colors duration-300">test@test.com</a>
```

**Change `test@test.com` to your actual email address.**

#### Social Media Links (around line 551)

```html
<a href="#" class="w-10 h-10 rounded-full bg-gray-800 flex items-center justify-center text-gray-400 hover:bg-purple-600 hover:text-white transition-all duration-300">
    <i class="fab fa-facebook-f"></i>
</a>
```

These currently have `href="#"` which does nothing. Replace with actual social media URLs:

**Example:**
```html
<!-- BEFORE -->
<a href="#" class="...">
    <i class="fab fa-facebook-f"></i>
</a>

<!-- AFTER -->
<a href="https://facebook.com/yourpage" class="...">
    <i class="fab fa-facebook-f"></i>
</a>
```

**Common social media URLs:**
- Facebook: `https://facebook.com/yourpage`
- Instagram: `https://instagram.com/yourprofile`
- LinkedIn: `https://linkedin.com/company/yourcompany`
- Twitter: `https://twitter.com/yourhandle`

---

### Complete Link Checklist

Here's a checklist of all links that need updating:

| Link | Current | Status | Action Needed |
|------|---------|--------|---------------|
| Get Started (Header) | `https://example.com` | ❌ Broken | Replace with your URL |
| Start Your Journey (Hero) | `https://example.com` | ❌ Broken | Replace with your URL |
| Schedule Consultation (CTA) | `https://example.com` | ❌ Broken | Replace with your URL |
| Privacy Policy (Footer) | `privacy.html` | ⚠️ Needs file | Create or link correctly |
| Terms of Service (Footer) | `terms.html` | ⚠️ Needs file | Create or link correctly |
| Blog (Footer) | `blog.html` | ⚠️ Needs file | Create or link correctly |
| Portfolio (Footer) | `https://example.com` | ❌ Broken | Replace with your URL |
| Contact Email (Footer) | `test@test.com` | ⚠️ Placeholder | Replace with your email |
| Facebook (Footer) | `#` | ❌ Broken | Add your Facebook URL |
| Instagram (Footer) | `#` | ❌ Broken | Add your Instagram URL |
| LinkedIn (Footer) | `#` | ❌ Broken | Add your LinkedIn URL |
| Twitter (Footer) | `#` | ❌ Broken | Add your Twitter URL |

---

## Linking Privacy and Terms Pages

Many websites are required to have Privacy Policy and Terms of Service pages. This section shows you how to link them properly.

### Step 1: Understand What You're Creating

You need to create two new HTML files:
- `privacy.html` - Your privacy policy page
- `terms.html` - Your terms of service page

These files should be in the **same folder** as your `index.html`.

### Step 2: Create the Privacy Policy Page

#### Creating the File

1. **Open your text editor** (same one you use for index.html)
2. **Create a new file** (File → New)
3. **Copy this template:**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Privacy Policy - Calgary Dream Homes">
    <title>Privacy Policy | Calgary Dream Homes</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        html {
            scroll-behavior: smooth;
        }
    </style>
</head>
<body class="bg-white text-gray-900 font-sans">
    <!-- Header Navigation (same as index.html) -->
    <header class="sticky top-0 z-50 bg-white shadow-md">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex items-center justify-between">
            <div class="flex items-center space-x-2">
                <div class="w-10 h-10 bg-gradient-to-r from-purple-600 to-purple-800 rounded-lg flex items-center justify-center">
                    <i class="fas fa-home text-white text-lg"></i>
                </div>
                <a href="index.html" class="text-xl font-bold text-gray-900">Calgary Dream Homes</a>
            </div>
            <div class="hidden md:flex items-center space-x-8">
                <a href="index.html#features" class="text-gray-700 hover:text-purple-600 font-medium">Features</a>
                <a href="index.html#benefits" class="text-gray-700 hover:text-purple-600 font-medium">Benefits</a>
                <a href="index.html#testimonials" class="text-gray-700 hover:text-purple-600 font-medium">Testimonials</a>
                <a href="index.html#about" class="text-gray-700 hover:text-purple-600 font-medium">About</a>
                <a href="https://example.com" class="bg-gradient-to-r from-purple-600 to-purple-800 text-white px-6 py-2 rounded-lg">Get Started</a>
            </div>
        </nav>
    </header>

    <!-- Privacy Policy Content -->
    <section class="py-16 bg-gray-50">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <h1 class="text-4xl font-bold text-gray-900 mb-8">Privacy Policy</h1>
            
            <div class="prose prose-lg max-w-none text-gray-700 space-y-6">
                <h2 class="text-2xl font-bold text-gray-900 mt-8">1. Introduction</h2>
                <p>
                    Calgary Dream Homes ("we," "us," "our," or "Company") is committed to protecting your privacy. 
                    This Privacy Policy explains how we collect, use, disclose, and safeguard your information when you 
                    visit our website.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">2. Information We Collect</h2>
                <p>
                    We may collect information about you in a variety of ways. The information we may collect on the Site includes:
                </p>
                <ul class="list-disc pl-6 space-y-2">
                    <li>Personal Data: Personally identifiable information, such as your name, shipping address, email address, and telephone number, that you voluntarily give to us when you register with the Site or when you choose to participate in various activities related to the Site.</li>
                    <li>Financial Data: Financial information, such as data related to your payment method (e.g., valid credit card number, card brand, expiration date) that we may collect when you purchase, order, return, exchange, or request information about our services from the Site.</li>
                    <li>Data From Social Networks: User information from social networks, including your name, your social network username, location, gender, birth date, email address, profile picture, and public data for contacts, if you connect your account to such social networks.</li>
                </ul>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">3. Use of Your Information</h2>
                <p>
                    Having accurate information about you permits us to provide you with a smooth, efficient, and customized experience. 
                    Specifically, we may use information collected about you via the Site to:
                </p>
                <ul class="list-disc pl-6 space-y-2">
                    <li>Email you regarding your account or order</li>
                    <li>Fulfill and manage purchases, orders, payments, and other transactions related to the Site</li>
                    <li>Generate a personal profile about you so that future visits to the Site will be personalized</li>
                    <li>Increase the efficiency and operation of the Site</li>
                    <li>Monitor and analyze usage and trends to improve your experience with the Site</li>
                </ul>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">4. Disclosure of Your Information</h2>
                <p>
                    We may share information we have collected about you in certain situations:
                </p>
                <ul class="list-disc pl-6 space-y-2">
                    <li><strong>By Law or to Protect Rights:</strong> If we believe the release of information is necessary to comply with the law.</li>
                    <li><strong>Third-Party Service Providers:</strong> We may share your information with third parties that perform services for us or on our behalf.</li>
                    <li><strong>Business Transfers:</strong> We may share or transfer your information in connection with a merger, sale, or acquisition of all or a portion of our business.</li>
                </ul>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">5. Security of Your Information</h2>
                <p>
                    We use administrative, technical, and physical security measures to help protect your personal information. 
                    While we have taken reasonable steps to secure the personal information you provide to us, please be aware that 
                    despite our efforts, no security measures are perfect or impenetrable.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">6. Contact Us</h2>
                <p>
                    If you have questions or comments about this Privacy Policy, please contact us at:
                </p>
                <p>
                    Calgary Dream Homes<br>
                    Email: test@test.com<br>
                    Calgary, Alberta, Canada
                </p>
            </div>
        </div>
    </section>

    <!-- Footer (same as index.html) -->
    <footer class="bg-gray-900 text-gray-300 py-16">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center border-t border-gray-800 pt-8">
                <p class="text-gray-400 text-sm">
                    &copy; 2025 Calgary Dream Homes. All rights reserved.
                </p>
            </div>
        </div>
    </footer>
</body>
</html>
```

4. **Save the file** as `privacy.html` in the same folder as `index.html`
5. **Replace placeholder text** with your actual privacy policy

### Step 3: Create the Terms of Service Page

#### Creating the File

1. **Create a new file** (File → New)
2. **Copy this template:**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Terms of Service - Calgary Dream Homes">
    <title>Terms of Service | Calgary Dream Homes</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        html {
            scroll-behavior: smooth;
        }
    </style>
</head>
<body class="bg-white text-gray-900 font-sans">
    <!-- Header Navigation (same as index.html) -->
    <header class="sticky top-0 z-50 bg-white shadow-md">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex items-center justify-between">
            <div class="flex items-center space-x-2">
                <div class="w-10 h-10 bg-gradient-to-r from-purple-600 to-purple-800 rounded-lg flex items-center justify-center">
                    <i class="fas fa-home text-white text-lg"></i>
                </div>
                <a href="index.html" class="text-xl font-bold text-gray-900">Calgary Dream Homes</a>
            </div>
            <div class="hidden md:flex items-center space-x-8">
                <a href="index.html#features" class="text-gray-700 hover:text-purple-600 font-medium">Features</a>
                <a href="index.html#benefits" class="text-gray-700 hover:text-purple-600 font-medium">Benefits</a>
                <a href="index.html#testimonials" class="text-gray-700 hover:text-purple-600 font-medium">Testimonials</a>
                <a href="index.html#about" class="text-gray-700 hover:text-purple-600 font-medium">About</a>
                <a href="https://example.com" class="bg-gradient-to-r from-purple-600 to-purple-800 text-white px-6 py-2 rounded-lg">Get Started</a>
            </div>
        </nav>
    </header>

    <!-- Terms of Service Content -->
    <section class="py-16 bg-gray-50">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <h1 class="text-4xl font-bold text-gray-900 mb-8">Terms of Service</h1>
            
            <div class="prose prose-lg max-w-none text-gray-700 space-y-6">
                <h2 class="text-2xl font-bold text-gray-900 mt-8">1. Agreement to Terms</h2>
                <p>
                    These Terms of Service constitute a legally binding agreement made between you, whether personally or on behalf 
                    of an entity ("you") and Calgary Dream Homes ("we," "us," "our," or "Company"), concerning your access to and use 
                    of the website as well as any other media form, media channel, mobile website or mobile application related or 
                    connected thereto (collectively, the "Site").
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">2. Intellectual Property Rights</h2>
                <p>
                    Unless otherwise indicated, the Site is our proprietary property and all source code, databases, functionality, 
                    software, website designs, audio, video, text, photographs, and graphics on the Site (collectively, the "Content") 
                    and the trademarks, service marks, and logos contained therein (the "Marks") are owned or controlled by us or 
                    licensed to us, and are protected by copyright and trademark laws.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">3. User Representations</h2>
                <p>
                    By using the Site, you represent and warrant that:
                </p>
                <ul class="list-disc pl-6 space-y-2">
                    <li>All registration information you submit is true, accurate, current, and complete</li>
                    <li>You will maintain the accuracy of such information and promptly update such registration information as necessary</li>
                    <li>You have the legal capacity and you agree to comply with these Terms of Service</li>
                    <li>You are not under the age of 18</li>
                    <li>You will not access the Site through automated or non-human means, whether through a bot, script or otherwise</li>
                </ul>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">4. User Restrictions</h2>
                <p>
                    You may not access or use the Site for any purpose other than that for which we make the Site available. 
                    The Site may not be used in connection with any commercial endeavors except those specifically endorsed or approved by us.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">5. Disclaimer of Warranties</h2>
                <p>
                    The Site is provided on an "AS-IS" and "AS AVAILABLE" basis. You agree that your use of the Site and our services 
                    will be at your sole risk. To the fullest extent permitted by law, we disclaim all warranties, express or implied, 
                    in connection with the Site and your use thereof.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">6. Limitation of Liability</h2>
                <p>
                    In no event shall Calgary Dream Homes or its suppliers be liable for any damages (including, without limitation, 
                    damages for loss of data or profit, or due to business interruption) arising out of or in connection with the use 
                    or inability to use the materials on the Site.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">7. Indemnification</h2>
                <p>
                    You agree to defend, indemnify, and hold harmless our company and its officers, directors, employees, and agents 
                    from and against any and all claims, damages, obligations, losses, liabilities, costs or debt, and expenses arising 
                    from your use and access of the Site.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">8. Governing Law</h2>
                <p>
                    These terms and conditions are governed by and construed in accordance with the laws of the Province of Alberta, 
                    Canada, and you irrevocably submit to the exclusive jurisdiction of the courts in that location.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8">9. Contact Us</h2>
                <p>
                    If you have any questions about these Terms of Service, please contact us at:
                </p>
                <p>
                    Calgary Dream Homes<br>
                    Email: test@test.com<br>
                    Calgary, Alberta, Canada
                </p>
            </div>
        </div>
    </section>

    <!-- Footer (same as index.html) -->
    <footer class="bg-gray-900 text-gray-300 py-16">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center border-t border-gray-800 pt-8">
                <p class="text-gray-400 text-sm">
                    &copy; 2025 Calgary Dream Homes. All rights reserved.
                </p>
            </div>
        </div>
    </footer>
</body>
</html>
```

3. **Save the file** as `terms.html` in the same folder as `index.html`
4. **Replace placeholder text** with your actual terms of service

### Step 4: Verify Links Work

Now let's make sure the links in your `index.html` footer work correctly.

#### Check Footer Links

In your `index.html`, find the Resources section in the footer (around line 535):

```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
<li><a href="blog.html" class="text-gray-400 hover:text-white transition-colors duration-300">Blog</a></li>
```

**These links should now work if:**
1. ✓ `privacy.html` exists in the same folder as `index.html`
2. ✓ `terms.html` exists in the same folder as `index.html`
3. ✓ The filenames match exactly (case-sensitive on some servers)

#### Test the Links

1. **Open `index.html` in your browser**
2. **Scroll to the footer**
3. **Click on "Privacy Policy"** - should open `privacy.html`
4. **Click on "Terms of Service"** - should open `terms.html`

If the links don't work, see the Troubleshooting section below.

### Step 5: Update Policy Content

The templates above are generic. You should customize them with your actual policies:

**For Privacy Policy, update:**
- Your company name and contact information
- Specific data collection practices
- How you use customer data
- Third-party services you use
- Your data retention policies

**For Terms of Service, update:**
- Your company name and contact information
- Specific terms for your services
- Liability limitations
- Governing law (if different from Alberta)
- Your specific policies

---

## Troubleshooting

### Common Issues and Solutions

#### Problem: Navigation links don't scroll to sections

**Symptoms:**
- Clicking a navigation menu item doesn't scroll to the section
- Page stays in the same place

**Solutions:**

1. **Check that section IDs exist:**
   - Search for `<section id="features">` (for example)
   - If not found, add it: `<section id="features" class="...">`

2. **Verify link matches ID:**
   ```html
   <!-- Link -->
   <a href="#features">Features</a>
   
   <!-- Must have matching ID -->
   <section id="features">
   ```

3. **Check for typos:**
   - `#featuress` (with extra 's') won't match `id="features"`
   - Must match exactly

---

#### Problem: Links open 404 error (page not found)

**Symptoms:**
- Clicking a link shows "404 Not Found" error
- Browser shows error message

**Solutions:**

1. **For internal links (privacy.html, terms.html):**
   - Verify files exist in same folder as index.html
   - Check filename spelling matches exactly
   - On Linux/Mac servers, filenames are case-sensitive
   - `privacy.html` ≠ `Privacy.html`

2. **For external links:**
   - Verify URL is complete: `https://example.com/page`
   - Not just: `example.com/page`
   - Check for typos in URL

3. **File structure should look like:**
   ```
   your-website-folder/
   ├── index.html
   ├── privacy.html
   ├── terms.html
   └── blog.html (if you create it)
   ```

---

#### Problem: CTA buttons don't work

**Symptoms:**
- Clicking "Get Started" button does nothing
- Button appears to be broken

**Solutions:**

1. **Check the href value:**
   ```html
   <!-- BROKEN (placeholder) -->
   <a href="https://example.com">Get Started</a>
   
   <!-- FIXED (real URL) -->
   <a href="https://yourwebsite.com/contact">Get Started</a>
   ```

2. **Verify URL format:**
   - Must start with `https://` or `http://`
   - Not just: `yourwebsite.com`
   - Correct: `https://yourwebsite.com`

3. **Test the URL:**
   - Copy the URL from the code
   - Paste it directly in browser address bar
   - If it doesn't work there, fix it in the code

---

#### Problem: Email link doesn't work

**Symptoms:**
- Clicking email link doesn't open email client
- Or opens wrong email address

**Solutions:**

1. **Check email format:**
   ```html
   <!-- CORRECT -->
   <a href="mailto:your@email.com">Contact Us</a>
   
   <!-- WRONG (missing mailto:) -->
   <a href="your@email.com">Contact Us</a>
   ```

2. **Verify email address:**
   - Replace `test@test.com` with your real email
   - Check for typos
   - Example: `info@calgarydreamhomes.com`

---

#### Problem: Social media links don't work

**Symptoms:**
- Clicking Facebook/Instagram/etc. doesn't go anywhere
- Shows `#` in URL

**Solutions:**

1. **Replace placeholder links:**
   ```html
   <!-- BEFORE (broken) -->
   <a href="#">
       <i class="fab fa-facebook-f"></i>
   </a>
   
   <!-- AFTER (fixed) -->
   <a href="https://facebook.com/yourpage">
       <i class="fab fa-facebook-f"></i>
   </a>
   ```

2. **Get your social media URLs:**
   - Go to your Facebook page
   - Copy the URL from the address bar
   - Paste it in the code

---

#### Problem: Text changes don't appear

**Symptoms:**
- Updated text in the code but browser still shows old text

**Solutions:**

1. **Save the file:**
   - Use `Ctrl+S` (Windows) or `Cmd+S` (Mac)
   - Look for a dot or indicator showing unsaved changes

2. **Refresh browser:**
   - Press `F5` or `Ctrl+R` (Windows)
   - Press `Cmd+R` (Mac)
   - Or click refresh button in browser

3. **Clear browser cache:**
   - Press `Ctrl+Shift+Delete` (Windows)
   - Press `Cmd+Shift+Delete` (Mac)
   - Select "Cached images and files"
   - Click "Clear"

4. **Try different browser:**
   - Sometimes browser caches aggressively
   - Try Chrome, Firefox, Safari, or Edge

---

#### Problem: Page looks broken or misaligned

**Symptoms:**
- Text overlaps, buttons look wrong
- Layout is messed up
- Colors are wrong

**Solutions:**

1. **Check for missing closing tags:**
   - Every `<div>` needs a `</div>`
   - Every `<a>` needs a `</a>`
   - Missing closing tags break the layout

2. **Verify Tailwind classes are intact:**
   - Don't modify class names accidentally
   - `text-4xl` not `text-4x1` (that's an 'L' not a '1')
   - `bg-purple-600` not `bg-purple600` (need the hyphen)

3. **Check for deleted code:**
   - If you deleted a section, make sure you didn't accidentally delete a closing tag
   - Use `Ctrl+Z` to undo recent changes

4. **Validate HTML:**
   - Visit [HTML Validator](https://validator.w3.org/)
   - Upload or paste your code
   - Look for errors

---

#### Problem: Mobile menu doesn't work

**Symptoms:**
- Menu button doesn't open on mobile
- Menu doesn't close

**Solutions:**

1. **Check JavaScript is intact:**
   - Scroll to the bottom of your `index.html`
   - Find the `<script>` section
   - Make sure it's not deleted or broken

2. **Verify mobile menu HTML exists:**
   - Search for `class="mobile-menu"`
   - Should exist in the header
   - If missing, you may have accidentally deleted it

3. **Test on actual mobile:**
   - Resize browser window to mobile size
   - Or use phone to test
   - Desktop resizing sometimes behaves differently

---

### When to Get Help

If you've tried the solutions above and still have problems:

1. **Check the console for errors:**
   - Press `F12` in your browser
   - Click "Console" tab
   - Look for red error messages
   - Screenshot the errors for support

2. **Validate your code:**
   - Use [HTML Validator](https://validator.w3.org/)
   - Use [CSS Validator](https://jigsaw.w3.org/css-validator/)
   - Fix any errors reported

3. **Compare with original:**
   - If you have a backup of the original file
   - Compare your version with original
   - See what changed

---

## Best Practices

### General Guidelines

#### 1. Always Backup Before Major Changes

```
Before editing:
1. Copy index.html to index-backup.html
2. Make your changes to index.html
3. If something breaks, you can restore from backup
```

#### 2. Make One Change at a Time

- Change one thing
- Save and test
- Then change something else
- This makes it easier to find problems

#### 3. Use Comments to Mark Your Changes

```html
<!-- CUSTOMIZED: Changed company name -->
<span class="text-xl font-bold text-gray-900">Your Company Name</span>

<!-- CUSTOMIZED: Updated contact email -->
<a href="mailto:your@email.com">your@email.com</a>
```

#### 4. Keep File Names Consistent

- Use lowercase: `privacy.html` not `Privacy.html`
- Use hyphens: `about-us.html` not `about_us.html`
- No spaces: `contact-form.html` not `contact form.html`

#### 5. Test All Links Regularly

- Click every link on the page
- Verify they go to the right place
- Test on mobile and desktop
- Test in different browsers

---

### Customization Checklist

Before launching your site, verify:

- [ ] Company name updated everywhere (header, footer, about section)
- [ ] All CTA buttons link to correct URLs
- [ ] Email address updated (footer, email links)
- [ ] Contact information is current (address, phone if applicable)
- [ ] Social media links added
- [ ] Privacy Policy page created and linked
- [ ] Terms of Service page created and linked
- [ ] All navigation links work
- [ ] Mobile menu works on phone
- [ ] Page looks good on desktop and mobile
- [ ] No broken images or icons
- [ ] All text is spell-checked

---

### Performance Tips

#### 1. Image Optimization

If you add images, compress them:
- Use [TinyPNG](https://tinypng.com/) or [ImageOptim](https://imageoptim.com/)
- Reduces file size and load time

#### 2. Link Structure

- Use relative links for internal pages: `privacy.html`
- Use full URLs for external links: `https://example.com`
- Test all links work correctly

#### 3. Mobile Testing

- Test on actual phones
- Not just browser window resizing
- Check touch buttons are big enough to tap

---

### Maintenance Schedule

#### Weekly
- Check all links work
- Verify forms are receiving submissions
- Monitor for errors in browser console

#### Monthly
- Update testimonials if you have new ones
- Review and update any outdated information
- Check for broken external links

#### Quarterly
- Update portfolio/projects section
- Review and refresh content
- Check site performance

---

### Version Control

Consider keeping track of versions:

```
Files to keep:
- index.html (current version)
- index-backup-v1.html (previous version)
- index-backup-v2.html (even older version)
- privacy.html
- terms.html
```

This way, if you need to revert to an older version, you have it.

---

## Quick Reference: Common Changes

### Change Company Name
Find and replace `Calgary Dream Homes` with your company name in:
- Header (line ~45)
- Footer (line ~510)
- About section (line ~395)

### Change Contact Email
Find and replace `test@test.com` with your email in:
- Footer contact section (line ~545)
- Email link (line ~547)
- Privacy policy (if you created it)
- Terms of service (if you created it)

### Change CTA Links
Find and replace `https://example.com` with your URL in:
- Header button (line ~56)
- Hero section button (line ~85)
- CTA section button (line ~480)
- Footer resources (line ~540)

### Add Social Media
Replace `href="#"` with actual URLs in footer (line ~551-567):
- Facebook: `https://facebook.com/yourpage`
- Instagram: `https://instagram.com/yourprofile`
- LinkedIn: `https://linkedin.com/company/yourcompany`
- Twitter: `https://twitter.com/yourhandle`

---

## Final Checklist

Before considering your site complete:

✓ **Content Updated**
- [ ] Company name updated
- [ ] All text customized
- [ ] Contact information correct
- [ ] Testimonials updated (optional)

✓ **Links Fixed**
- [ ] All navigation links work
- [ ] CTA buttons link correctly
- [ ] Email links work
- [ ] Social media links added
- [ ] Privacy/Terms links work

✓ **Pages Created**
- [ ] privacy.html created
- [ ] terms.html created
- [ ] Both pages linked in footer
- [ ] Both pages have correct content

✓ **Testing Done**
- [ ] All links tested
- [ ] Mobile menu tested
- [ ] Page looks good on mobile
- [ ] Page looks good on desktop
- [ ] All buttons clickable

✓ **Optimized**
- [ ] No broken links
- [ ] No placeholder text remaining
- [ ] No "example.com" URLs
- [ ] No "test@test.com" emails

---

## Support Resources

### Helpful Tools

- **HTML Validator:** https://validator.w3.org/
- **CSS Validator:** https://jigsaw.w3.org/css-validator/
- **Font Awesome Icons:** https://fontawesome.com/icons
- **Tailwind CSS Docs:** https://tailwindcss.com/docs
- **Color Picker:** https://htmlcolorcodes.com/

### Learning Resources

- **HTML Basics:** https://www.w3schools.com/html/
- **CSS Basics:** https://www.w3schools.com/css/
- **Tailwind CSS:** https://tailwindcss.com/docs/installation
- **Font Awesome:** https://fontawesome.com/docs

### Where to Get Help

- **Stack Overflow:** https://stackoverflow.com/ (ask coding questions)
- **Web Development Forums:** Various communities for web developers
- **Your Web Host Support:** If hosted on a server, contact their support team
- **Freelance Developers:** If you need professional help

---

## Conclusion

You now have all the tools and knowledge to maintain and customize the Calgary Dream Homes landing page. Remember:

1. **Take your time** - There's no rush
2. **Make backups** - Always save a copy before major changes
3. **Test everything** - Click all links and test on mobile
4. **Keep it simple** - Don't change more than needed
5. **Ask for help** - There's no shame in getting professional assistance

Good luck with your website! If you have questions, refer back to this guide or seek help from the resources listed above.

---

**Document Version:** 1.0  
**Last Updated:** 2025  
**For:** Calgary Dream Homes Landing Page  
**Framework:** Tailwind CSS + Font Awesome Icons