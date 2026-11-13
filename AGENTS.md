# AdminKit

Free Bootstrap 5 admin template, published to npm as `@adminkit/core`.

## Commands

- `npm run dev`: dev server on http://localhost:8080
- `npm run build`: build into `dist/`; `npm run preview` serves it
- `npm run lint`: ESLint, Prettier, the icon check and the stats check; must pass
- `npm run format`: Prettier write
- `npm run stats`: regenerate `src/data/stats.json` and the README counts
- `npm run stats:sync -- --pro ../adminkit-pro`: refresh PRO's counts; run it before every release

## Layout

- `src/pages/*.html` are Handlebars pages with YAML frontmatter; `src/layouts` and `src/partials` are partials, `src/helpers` helpers, `src/data` global data.
- `src/js` and `src/scss` build to `js/app.js` and `css/app.css`. Keep the output names: the pages and the npm package use them. `js/app.js` stays one self-contained file (no dynamic imports, no chunks); `src/types/app.d.ts` types its globals.
- `src/js/head.js` is a blocking script in `<head>`: it sets the color mode before the first paint and must not import anything.

## Rules
