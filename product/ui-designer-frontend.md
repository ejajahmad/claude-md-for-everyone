# CLAUDE.md: Design-Minded Frontend Developer

<!-- For: designers who code and frontend devs who care about pixel-level polish and UX. -->

## About me
I care how things look and feel. Interfaces should be polished, consistent, accessible, and delightful, not "functional but ugly".

## Visual design
- Use the existing design system (tokens, components, spacing scale) when the project has one. Never hardcode a color or size that already has a token.
- Without a system, use a consistent spacing scale (4/8px), a limited type scale, and a restrained palette.
- Create visual hierarchy through size, weight, and spacing before color.
- Align to a grid. Keep spacing consistent between related and unrelated elements.

## States (every interactive element)
Default, hover, focus-visible, active, disabled, loading, empty, error, and success. Don't ship a component without its empty and error states.

## Responsiveness
- Mobile-first. Test at 360px, 768px, and 1280px or wider. No horizontal scroll at any width.
- Touch targets of at least 44×44px on mobile.

## Accessibility (non-negotiable)
- Semantic HTML first. Use ARIA only when there's no native element.
- Make everything keyboard-operable, with a visible focus ring and a logical tab order.
- Text contrast of at least 4.5:1. Never use color alone to convey meaning.
- Labels on all inputs, and alt text that describes purpose.
- Respect `prefers-reduced-motion` and `prefers-color-scheme`.

## Motion
- Keep transitions subtle and quick (150–250ms) with ease-out. Use motion to explain changes, not to decorate.

## Copy
- Use clear, human microcopy. Buttons say what they do ("Save changes", not "Submit"). Error messages say how to fix the problem.

## Project specifics
<!-- Framework, CSS approach (Tailwind, CSS modules…), design system/Figma link, brand colors. -->
