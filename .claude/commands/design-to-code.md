# Design to Code - Transform Mockups into Production Components

Convert design mockups, screenshots, or Figma exports into production-ready code with extracted design systems.

## Usage

```bash
design-to-code @screenshot.png              # Single mockup
design-to-code @designs/                    # Multiple designs
design-to-code @mockup.png --framework react  # Specific framework
```

## Workflow

This command orchestrates a complete design implementation pipeline:

1. **visual-design-extractor** - Analyzes mockup and extracts complete design system
2. **typescript-expert** or **python-expert** - Creates type-safe components
3. **test-generator** - Generates visual regression and component tests
4. **documentation-writer** - Documents component API and usage
5. **code-reviewer** - Ensures accessibility and best practices

## What Gets Generated

### Design System
```css
/* design-tokens.css */
:root {
  --color-primary-500: #3B82F6;
  --spacing-unit: 8px;
  --font-family-sans: 'Inter', sans-serif;
  /* ... complete design system ... */
}
```

### Components
```tsx
// Button.tsx - Pixel-perfect implementation
export const Button: React.FC<ButtonProps> = ({ 
  variant = 'primary',
  size = 'md',
  children,
  ...props 
}) => {
  // Implementation matching design exactly
}
```

### Configuration
```js
// tailwind.config.js - Generated from design
module.exports = {
  theme: {
    extend: {
      colors: { /* extracted palette */ },
      spacing: { /* extracted spacing */ }
    }
  }
}
```

## Options

- `--framework [react|vue|angular|native]` - Target framework
- `--style [tailwind|css|scss|styled]` - Styling approach
- `--a11y` - Enhanced accessibility features
- `--animations` - Include micro-animations
- `--responsive` - Generate responsive variants
- `--dark-mode` - Include dark mode variants

## Example Output

```
🎨 Design Analysis Starting...

📐 Design System Extracted:
- Primary Color: #3B82F6 (Blue)
- Typography: Inter (14px, 16px, 20px, 32px)
- Spacing: 8px grid system
- Components: 12 unique patterns identified

🏗️ Generating Components:
✅ Button (3 variants, 3 sizes)
✅ Card (standard, featured)
✅ Input (text, search, password)
✅ Navigation (header, mobile)

🧪 Creating Tests:
✅ Visual regression tests
✅ Component unit tests
✅ Accessibility tests

📚 Documentation:
✅ Component storybook
✅ Usage examples
✅ Design tokens reference

✨ Design Implementation Complete!
- 12 components generated
- 100% design fidelity
- WCAG AA compliant
```

## Advanced Features

### Consistency Checking
```
design-to-code @new-screen.png --check @existing-design-system.json
```
Validates new designs against existing design system

### Batch Processing
```
design-to-code @designs/*.png --output ./src/components
```
Process multiple designs maintaining consistency

### Design Updates
```
design-to-code @updated-mockup.png --update
```
Updates existing components to match new designs

## When to Use

- Starting new projects from designs
- Implementing designer mockups
- Creating design systems
- Ensuring design consistency
- Rapid prototyping from mockups