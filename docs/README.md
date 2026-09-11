# Fertility Transition Index

A catalogue of the literature on fertility decline and the demographic transition:
bibliographic records with a key-argument summary for each work, cross-indexed by
school of thought, author, region, publication decade, and the period each work covers.

The site is a single static page. Open `index.html` through GitHub Pages (or any
web server) rather than as a local file, since it loads its data over HTTP.

## Files

| File | What it is |
| --- | --- |
| `index.html` | The whole application: search, faceted browsing, entry records, and the time plane |
| `data.json` | The corpus. One object per work in `entries`. Edit this to change the index |

## Editing

Two ways, and they meet in the same place.

Edit `data.json` directly in GitHub and commit. The site picks up the change on the
next load.

Or use the page: **+ Add entry** and **Edit entry** save into your browser's local
storage, so they survive a reload but live only in that browser. When you are happy
with them, press **Download data.json** and commit the downloaded file over the one
in this repository. The button shows a count of edits not yet written back.

## Entry fields

`title`, `authors` (array), `year`, `kind`, `venue`, `volume`, `issue`, `pages`,
`publisher`, `doi`, `url`, `citeKey`, `language`, `sourceFile`.

`camps` (array) is the school of thought, `regions` (array) the geography covered,
and `periodFrom` / `periodTo` the span of time the work studies. Set `periodDeep`
to `true` for a work that reaches back before 1780, which draws an open left edge
on the time plane.

`keyArgument` holds the summary. Blank lines separate paragraphs.

Set `citationVerified` to `false` when a citation needs checking, and put the reason
in `citationNote`; the record then shows that note in the margin.

## The time plane

Each work is drawn as a bar spanning the period it studies, positioned vertically by
publication year, against the dashed publication diagonal. The distance between a bar
and the diagonal is how far back that author was looking.

## Export

**Export BibTeX** writes the whole corpus as a `.bib` file, with each key argument
carried in the `annote` field.
