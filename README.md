# The 9x Academic

Minimal Jekyll landing page for the9x.ac - AI tools for academics.

## Setup

1. Install dependencies: `bundle install`
2. Run locally: `bundle exec jekyll serve`
3. Deploy to GitHub Pages via GitHub Actions

## Configuration

All site settings are centralized in `_data/settings.yml`. This file controls:

### Kit.com Integration
Configure your Kit (formerly ConvertKit) integration:
```yaml
kit:
  form_id: "YOUR_FORM_ID"
  public_api_key: "YOUR_PUBLIC_KEY_HERE"
```
- Get your form ID from Kit.com dashboard
- Use only the public API key (never expose secret key in frontend)
- Form supports both JavaScript API submission and standard POST fallback

### Customization Options

#### Colors
Edit the `colors` section to change the color scheme:
- `background`: Main background color
- `accent`: Call-to-action button color
- `primary_text`, `secondary_text`: Text hierarchy

#### Typography
Modify fonts and weights in `typography`:
- Currently uses Inter font from Google Fonts
- Three weight variants: regular (400), medium (600), bold (700)

#### Content
Update meta descriptions, titles, and form labels:
- `meta`: SEO and social sharing information
- `form.fields`: Customize form field labels and placeholders
- `form`: Success/error messages and button text

#### Responsive Design
Adjust scaling values for different screen sizes:
- Logo and tagline scale independently but proportionally
- Breakpoints: mobile (480px), tablet (768px), desktop (1024px+)

### Features

- **Progressive Enhancement**: Form works with or without JavaScript
- **Spam Prevention**: Honeypot field to catch bots
- **Responsive SVGs**: Logo and tagline scale proportionally
- **Dark Mode**: Native dark theme design
- **Accessibility**: Proper contrast ratios and touch targets

## Domain

Configure custom domain `the9x.ac` in GitHub Pages settings with CNAME file.

## Deployment

The site automatically deploys to GitHub Pages when changes are pushed to the main branch via GitHub Actions workflow.