# Design Guidelines: "Starry Night" Portfolio for Heet Shripal Kankariya

## Design Approach
**Reference-Based Approach**: Inspired by Vincent van Gogh's "Starry Night" - swirling motion, luminous celestial colors, painterly textures, and flowing animation. This is an artistic portfolio that prioritizes visual impact and emotional engagement while maintaining usability.

## Core Design Principles
- **Artistic Expression**: Painterly, dreamlike quality with swirling animations
- **Celestial Motion**: Continuous flowing animation that never stops
- **Luminous Aesthetics**: Glowing elements and soft transitions
- **Responsive Elegance**: Fully responsive across all devices

## Color Palette
- **Deep Blue**: `#0B3D91` - Primary background color
- **Star Gold**: `#FFD700` - Accent color for interactive elements and stars
- **Midnight Blue**: `#1C1C3C` - Secondary backgrounds and cards
- **Cream**: `#F5DEB3` - Text and subtle highlights

## Typography
- **Headings**: Playfair Display (serif) - Artistic, elegant feel
- **Body Text**: Inter (sans-serif) - Clean, modern readability
- **Hierarchy**: 
  - Hero Name: text-6xl to text-8xl (responsive)
  - Section Headings: text-4xl to text-5xl
  - Subheadings: text-2xl to text-3xl
  - Body: text-base to text-lg
  - Small text: text-sm

## Layout System
**Spacing Units**: Use Tailwind spacing of 4, 8, 12, 16, 20, 24 (e.g., p-4, m-8, gap-12, py-16, px-20, mb-24)

**Container Strategy**:
- Full-width animated background layer (fixed position)
- Content container: max-w-7xl mx-auto px-8
- Section padding: py-20 (desktop), py-12 (mobile)

## Animated Background
**Critical Feature**: Full-viewport swirling "Starry Night" backdrop
- **Implementation**: tsparticles or Three.js for particle system
- **Animation Style**: Continuous swirling motion mimicking Van Gogh's brushstrokes
- **Particles**: Golden stars (#FFD700) with varying sizes and opacity
- **Movement**: Organic, flowing paths with parallax depth
- **Layer**: Fixed background layer (z-index: -1) spanning entire viewport
- **Performance**: Smooth 60fps animation with optimized particle count

## Component Library

### Navigation
- Fixed/sticky top navigation with glass-morphism effect
- Backdrop blur with semi-transparent midnight blue background
- Golden hover states for nav links
- Smooth scroll behavior to sections

### Hero Section
- Full viewport height (100vh)
- Layered on top of animated starry background
- Centered content with name, tagline, profile image
- Glowing "View My Work" CTA button with golden accent
- Profile image with soft glow effect and fade-in animation

### About Section
- Two-column layout (desktop): Profile image left, bio text right
- Single column (mobile): Image top, text below
- Gentle fade-in animations on scroll
- Profile image with artistic border treatment

### Projects Section
- Grid layout: grid-cols-1 md:grid-cols-2 lg:grid-cols-3
- Project cards with:
  - Midnight blue (#1C1C3C) background
  - Project image at top
  - Title, description, links below
  - Hover effect: lift (transform translateY) and golden glow
  - GitHub and Live Demo buttons with icon + text

### Contact Section
- Centered form with max-w-2xl
- Form fields with midnight blue backgrounds and golden focus states
- Validated inputs (name, email, message)
- Submit button with glowing hover effect
- Success/error message states

### Footer
- Midnight blue background
- Social links with golden hover states
- "Inspired by Van Gogh's Starry Night" credit text
- Cream text color

## Animations
**Full Animation Intensity** - Rich, artistic motion throughout:
- **Page Load**: Fade-in cascade effect for all sections
- **Scroll Animations**: Parallax effects, fade-in on reveal
- **Hover States**: Gentle lift (4px), golden glow, scale transitions
- **Background**: Continuous swirling particle animation
- **Transitions**: Smooth 300-500ms easing for all interactions
- **Button Interactions**: Glow expansion on hover, subtle scale

## Theme Toggle
- Dark mode default (matches Starry Night aesthetic)
- Light mode available via toggle button
- Smooth transition between themes (duration-300)
- Toggle positioned in navigation bar

## Images
- **Hero Profile Image**: https://ibb.co/27nzj8Mz - Centered with circular crop, glowing border
- **Project Images**: https://ibb.co/27nzj8Mz (placeholder for all three projects) - Aspect ratio 16:9, rounded corners
- **Image Treatment**: Soft shadows, subtle hover zoom effects

## Accessibility
- Semantic HTML5 elements throughout
- ARIA labels for interactive elements
- Focus outlines with golden accent color
- Alt text for all images
- Keyboard navigation support
- Sufficient color contrast for cream text on dark backgrounds

## Responsive Breakpoints
- Mobile: < 768px (single column layouts)
- Tablet: 768px - 1024px (2-column grids)
- Desktop: > 1024px (3-column grids, full layouts)

## Special Effects
- **Glass-morphism**: Navigation bar with backdrop-blur-md
- **Glowing Effects**: text-shadow and box-shadow with golden color
- **Particle System**: Starry background with swirling motion paths
- **Parallax**: Multiple depth layers in background animation
- **Soft Transitions**: All state changes animated smoothly