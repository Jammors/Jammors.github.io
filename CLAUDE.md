# jammor.com

A personal Jekyll blog, hosted on GitHub Pages (repo Jammors/Jammors.github.io, custom domain in `CNAME`).

## Layout
- `_posts/`: posts named `YYYY-MM-DD-slug.md`
- `assets/<post-slug>/`: images and videos for each post (for example `assets/bevy-periscope/`)
- `_includes/`: template overrides (the Google Analytics tag is set via `google_analytics` in `_config.yml`)
- `_site/` and `.jekyll-cache/` are build output. Never edit or commit them.

## Commands
- `bundle install`, then `bundle exec jekyll serve` for a local preview at http://localhost:4000. Restart it after editing `_config.yml`.

## Git
- Push straight to `main`. There are no PRs, and GitHub Pages deploys on push.
- Commit messages use conventional commits with a `blog` scope, for example `feat(blog): add GA4 google analytics` or `chore(blog): new bevy periscope demo video`.

## Writing
- Posts are in the author's own voice: informal but informative. Don't make them sound like marketing or AI-generated text.
- The GA measurement ID is public by design, so committing it is fine.
