# personaltaste
Community art review platform — an endless draggable grid of real museum artwork, taste-tagging, and a public review leaderboard.

# Vantage

A community art review platform. Browse an endless, draggable grid of real artwork, tag pieces with your own taste vocabulary, and post reviews that count toward a public leaderboard.

## Features

- **Infinite grid** of real artwork — click and drag to pan through both a design grid and a separate keyword field
- **Live artwork** pulled from the Met Museum's Open Access API — real public-domain pieces, not placeholders
- **1,250+ keyword taxonomy** across movements, aesthetics, mediums, techniques, cultural contexts, and more — explore, tag your own, or use them to filter the grid
- **Community reviews** — post a take on any piece, react to others' reviews ("resonates"), and see reviewer profiles
- **Rank & leaderboard** — your review count is your rank, filterable by category, backed by a real public database
- **Research tools** — style/technique reference notes, an "applications" folder view, and a quiz mode
- **Your Library** — saved pieces, collections, and your own image uploads for private review

## Tech stack

- Single-file HTML/CSS/JS, no build step, no framework
- [Supabase](https://supabase.com) (Postgres + realtime) for reviews, reactions, and the leaderboard — see `supabase-schema.sql`
- [Met Museum Open Access API](https://metmuseum.github.io/) for live artwork

## Setup

1. Create a free [Supabase](https://supabase.com) project.
2. Run `supabase-schema.sql` in the Supabase SQL Editor to create the `reviews` and `reactions` tables.
3. Drop your project's URL and publishable key into the `SUPABASE_URL` / `SUPABASE_KEY` constants near the top of `index.html`'s script.
4. Open `index.html` in a browser, or host it anywhere static (GitHub Pages, Netlify, etc.).

No login required to browse or leave a display name once you review — accounts are honor-system by design.
