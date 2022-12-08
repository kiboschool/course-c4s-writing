# Communicating for Success

- See course info: https://degree-planner.programming.africa/?f=HSS120
- See info about Kibo's BSc. Computer Science: https://kibo.school/degree/

## What's here?

```
$ tree .
.
├── README.md
├── output
├── book.toml
└── src
    ├── SUMMARY.md
    └── chapter_1.md
```

### README.md

This file.

### output

To generate the static site, run:

```
mdbook build
```

Output lives in `output`. It's git-ignored.

You can usually ignore the files in `output`.

### book.toml

Config file for the course. Authors, title, other mdbook settings.

https://rust-lang.github.io/mdBook/format/configuration/index.html

### src/SUMMARY.md

This gets turned into the sidebar on the site. 

It's the text that should show, plus links to other md files in `src/`.

https://rust-lang.github.io/mdBook/format/summary.html

### src/*

These are the pages that actually make up the course. It's nice to put
things in folders to organize the different pages, so that's what the convert
script does by default.

## Getting Started

Install mdbook: https://rust-lang.github.io/mdBook/guide/installation.html

if you use rust:

```
cargo install mdbook
```

Or use your package manager: `brew install mdbook`, or download a release from
Github.

## Run the book locally

```
mdbook serve
```

## Deployment

We use `vercel` to handle deploys. It takes some setup to connect a repo to
vercel, assign a production domain, and set up auto-deploys.

If all that's been done...

* Pushes to the `main` branch will automatically deploy to vercel. 

### Manual deployment

You'll need vercel permissions.

Create a preview deploy:

```
vercel
```

Deploy to production:

```
vercel --prod
```
