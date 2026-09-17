# Physical Visualizer — Notes

## Navigation
- Added a "🏠 Home" link at the top of the transport chrome, linking to `/` so users can
  return to the site's main index page from within the visualizer.
- Implemented as a plain anchor (`<a id="btn-home" href="/">`) rather than a `<button>` so
  that it behaves as a standard, accessible link (middle-click/new-tab support, proper
  status bar preview, no JS handler required).
- Styled in `css/chrome.css` to visually match the existing transport buttons (same
  border, background, and active state) while using the anchor-appropriate `#9cf` link
  color already used elsewhere in the chrome (see `.preset-name`).

## Status
- This is a DOM-based placeholder chrome per the existing comment in `index.html`
  ("temporary DOM transport; replaced by skinned windows in Phase 5"). The home link
  should be preserved/re-implemented when the skinned window chrome lands in Phase 5.

## Follow-ups
- When Phase 5 skinned chrome replaces this DOM transport, ensure the home navigation
  affordance is carried over (e.g., as a skin sprite/button bound to `location.href = '/'`
  or an equivalent anchor element).
- Consider whether the home link should warn users if audio/visualization state would be
  lost (currently no confirmation is shown; navigation is immediate).