# lastfm_artist_discovery

Personal copy for the Last.fm user `bonelifer`.

A GitHub Pages site that tracks artists discovered via Last.fm scrobbles. Updated nightly by GitHub Actions.

## Pages

**Discoveries** (`index.html`) — Artists heard in the last 7 days that are not in the all-time top 500. Stays in the catalog until they graduate into the top 500.

**Classical Spotter** (`classical.html`) — Filters the discovery catalog for tracks or albums where a classical composer's name appears, performed by someone else.

**Old Favorites** (`familiar.html`) — All non-graduated discovery artists, enriched with each artist's personal top 3 all-time tracks.

## Stack

- Python + `pylast` for data collection (`scripts/update_catalog.py`, `scripts/update_familiar.py`)
- Static JSON files in `data/` as the data layer
- Vanilla JS frontend; no build step
- GitHub Actions for nightly runs and automatic Pages deployment

## Setup

Add `LASTFM_API_KEY` and `LASTFM_API_SECRET` in the repository's Actions secrets before running **Update Artist Catalog**. The workflow uses `bonelifer` for both catalogs. The checked-in catalogs initially contain upstream data until a successful update replaces or updates them.

To publish the static site, configure GitHub Pages to deploy from the default branch root.

## Contributing

Contributions are welcome!

- **Bug reports**: [Open an issue](https://github.com/bonelifer/lastfm_artist_discovery/issues).
- **Everything else** (questions, feature requests, ideas, general discussion): [Use Discussions](https://github.com/bonelifer/lastfm_artist_discovery/discussions).
- Pull requests are welcome for bug fixes or discussed features.

## Acknowledgments

- Based on [sugarsmax/lastfm_artist_discovery](https://github.com/sugarsmax/lastfm_artist_discovery), with its Git history preserved.
- Repository setup and workflow configuration assisted by [Codex](https://openai.com/codex/).

## License

The upstream repository did not include a license file when this copy was created. No new license is assigned to the upstream code here.
