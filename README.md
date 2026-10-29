# Hibar III — Modern Landing Page

A fast, accessible, single-file portfolio landing page built with vanilla HTML, CSS and JavaScript.

## Live site

https://tekashihibarii.github.io/hibar-landing-page/

## Features

- Responsive layout with mobile navigation
- Light / dark theme with saved preference
- Scroll progress indicator, reveal animations and animated statistics
- Project filtering, testimonial carousel with pause control and FAQ accordion
- Client-side contact form validation with accessible error states
- No frameworks, no runtime dependencies, zero external requests

## Performance and accessibility

- One HTML request; CSS and JavaScript are inlined and minified
- System font stack, CSS-only visuals and a data-URI favicon
- Lighthouse mobile: 100 Performance / 100 Accessibility / 100 Best Practices / 100 SEO
- WCAG 2.2 AA checks with axe-core: zero violations across light, dark, form-error and mobile-menu states

## Security

- Hash-based Content-Security-Policy delivered with a `<meta http-equiv>` element
- `strict-origin-when-cross-origin` referrer policy
- `/.well-known/security.txt` vulnerability contact
- HTTPS enforced by GitHub Pages, with HSTS supplied by the host

GitHub Pages does not allow custom HTTP response headers, so `Content-Security-Policy`,
`X-Content-Type-Options`, `X-Frame-Options`, `Referrer-Policy` and `Permissions-Policy`
cannot be set at the server level. The meta CSP and referrer policy mitigate what the
platform allows; the remaining gaps are host-controlled and documented in the audit report.

## Known limitations

- The contact form is a front-end validation demo. It has no backend and does not send email;
  the success message directs visitors to the published email address.
- `hello@example.com` is placeholder contact content and should be replaced before production use.

## Local preview

```bash
npx serve .
```

## Deployment

Hosted on GitHub Pages from the `main` branch. Every push to `main` is published automatically.
