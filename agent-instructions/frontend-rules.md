# Frontend Rules

Apply these rules when editing frontend code.

## Components

- Keep components focused.
- Avoid large components with many responsibilities.
- Extract reusable logic only when reuse is real.
- Do not over-abstract.
- Keep UI state close to where it is used.
- Avoid duplicating server state in local state.

## Data fetching

- Centralize API calls where practical.
- Handle loading, empty, success, and error states.
- Avoid request waterfalls.
- Avoid refetch loops.
- Handle authentication expiration.
- Validate assumptions about API response shape.

## Forms

- Validate on the client for usability.
- Validate on the server for security.
- Show useful error messages.
- Preserve user input after validation errors.
- Disable duplicate submissions where appropriate.
- Handle pending states.

## Accessibility

Ensure:

- Buttons are buttons.
- Links are links.
- Inputs have labels.
- Errors are associated with fields.
- Interactive elements are keyboard accessible.
- Focus states are visible.
- Dialogs manage focus.
- Images have appropriate alt text.
- Icons have accessible names when needed.
- Color is not the only signal.

## Security

- Avoid unsafe HTML rendering.
- Sanitize rich text.
- Validate external URLs.
- Do not expose secrets in frontend code.
- Do not rely on frontend-only authorization.
- Avoid leaking sensitive data into analytics or logs.

## Performance

- Paginate or virtualize large lists.
- Avoid unnecessary re-renders.
- Memoize expensive calculations when needed.
- Optimize images.
- Watch bundle size.
- Avoid importing large libraries for small tasks.

## Testing

Test:

- User-visible behavior
- Form validation
- Error states
- Auth states
- Accessibility-critical interactions
- Regression cases
