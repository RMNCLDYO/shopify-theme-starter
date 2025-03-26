# Shopify Theme Starter

![Shopify Partner](https://img.shields.io/badge/Shopify-Partner-green)
![License](https://img.shields.io/badge/License-MIT-blue.svg)
![HTML](https://img.shields.io/badge/HTML-5-blue.svg)
![CSS](https://img.shields.io/badge/CSS-3-blue.svg)
![JavaScript](https://img.shields.io/badge/JavaScript-ES6-blue.svg)
![Liquid](https://img.shields.io/badge/Liquid-Latest-blue.svg)

A modern, production-ready starter theme for building custom Shopify storefronts. This theme was bootstrapped using the Shopify CLI and the `shopify theme init` command, providing a solid foundation for creating custom Shopify themes.

## Table of Contents

- [Features](#features)
- [Prerequisites](#prerequisites)
- [Quick Start](#quick-start)
- [Getting Started](#getting-started)
- [Project Structure](#project-structure)
- [Theme Development](#theme-development)
- [Deployment](#deployment)
- [Customization](#customization)
- [Performance Considerations](#performance-considerations)
- [Resources](#resources)
- [License](#license)

## Features

- 📱 **Responsive Design** - Works on all devices and screen sizes
- 🚀 **Performance Optimized** - Fast loading times and smooth interactions
- 🔍 **SEO Friendly** - Structured data and optimized markup
- 🌐 **Internationalization Ready** - Support for multiple languages
- 🎨 **Customizable Sections** - Flexible layout options for merchants
- 🛒 **Optimized Checkout** - Streamlined shopping experience
- 📦 **Modern Asset Handling** - Efficient loading of stylesheets and scripts
- 🧩 **Modular Architecture** - Clean, maintainable code structure

## Prerequisites

Before you begin, make sure you have:

- **Node.js** - Version ^16.0.0 or higher ([Download](https://nodejs.org/en/download/))
- **Shopify CLI** - For theme development and store integration
- **Shopify Partner Account** - [Create one](https://partners.shopify.com/signup) if you don't have it
- **Shopify Development Store** - For testing ([Create a development store](https://help.shopify.com/en/partners/dashboard/development-stores#create-a-development-store))
- **Git** - For version control and deployment

## Quick Start

There are two ways to get started with this theme:

### Option 1: Use the Shopify CLI (Recommended)

The official way to create a Shopify theme is using the Shopify CLI:

```bash
# Install the Shopify CLI
npm install -g @shopify/cli @shopify/theme

# Create a new theme based on Dawn (Shopify's reference theme)
shopify theme init

# Choose Dawn when prompted for a theme
```

### Option 2: Use this Starter Theme

If you prefer to use this starter theme directly:

```bash
# Clone the repository
git clone https://github.com/rmncldyo/shopify-theme-starter.git your-theme-name

# Navigate to the project directory
cd your-theme-name

# Start the development server
shopify theme dev
```

## Getting Started

### Local Development

Start your development server to preview the theme in your browser:

```bash
# Using the Shopify CLI
shopify theme dev
```

This will:
1. Connect to your Shopify store
2. Set up a local development server
3. Watch for changes to your theme files
4. Provide a URL to preview your theme

### Theme Editor

You can also use the Shopify Theme Editor to make changes directly in the Shopify admin:

1. Go to your Shopify admin
2. Navigate to Online Store > Themes
3. Click on "Customize" on your theme
4. Use the visual editor to make changes

## Project Structure

```
├── assets/            # Theme assets (JS, CSS, images, fonts)
├── config/            # Theme settings
├── layout/            # Theme layout templates
├── locales/           # Translation files
├── sections/          # Theme sections
├── snippets/          # Reusable liquid snippets
├── templates/         # Page templates
│   └── customers/     # Customer account templates
├── .shopify/          # Shopify CLI configuration 
├── .theme-check.yml   # Theme Check configuration
```

## Theme Development

### Working with Liquid

Shopify themes use Liquid, a template language created by Shopify. Here's a simple example of Liquid syntax:

```liquid
{% if product.available %}
  <p>{{ product.price | money }}</p>
{% else %}
  <p>Sold out</p>
{% endif %}
```

### Theme Settings

Theme settings are defined in `config/settings_schema.json` and allow merchants to customize the theme without editing code.

### Sections

Sections are modular, customizable components that merchants can add, remove, and rearrange on their store.

### Blocks

Blocks are subsections that can be added to sections, providing even more customization options.

## Deployment

### Publishing Your Theme

To publish your theme to your Shopify store:

```bash
# Package and upload your theme
shopify theme push
```

### Creating a Release

To create a new version of your theme:

```bash
# Package your theme for the Theme Store
shopify theme package
```

## Customization

### Styling with CSS

The theme uses modern CSS features. Main stylesheets are located in the `assets` directory.

### JavaScript Enhancements

Add JavaScript functionality in the `assets` directory. The theme uses vanilla JavaScript for optimal performance.

### Custom Sections and Blocks

Create custom sections by adding new files to the `sections` directory:

```liquid
{% schema %}
{
  "name": "Custom Section",
  "settings": [
    {
      "type": "text",
      "id": "title",
      "label": "Heading",
      "default": "Hello world"
    }
  ],
  "presets": [
    {
      "name": "Custom Section",
      "category": "Custom"
    }
  ]
}
{% endschema %}

<div class="custom-section">
  <h2>{{ section.settings.title }}</h2>
</div>
```

## Performance Considerations

- Optimize images using formats like WebP
- Minimize JavaScript usage
- Use lazy loading for images and content
- Leverage browser caching
- Implement responsive image techniques

## Resources

- [Shopify Theme Development](https://shopify.dev/docs/themes)
- [Liquid Documentation](https://shopify.dev/docs/api/liquid)
- [Shopify CLI Documentation](https://shopify.dev/docs/apps/tools/cli)
- [Dawn Theme Documentation](https://shopify.dev/themes/tools/dawn)
- [Shopify Partners Program](https://www.shopify.com/partners)
- [Theme Store Requirements](https://shopify.dev/themes/store/requirements)

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.
