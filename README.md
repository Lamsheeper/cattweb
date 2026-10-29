# cattweb

Website for https://catt.baulab.info/, the project page for
"Elucidating the Design Space of LM Data Attribution".

Edit the page in `src/`, run `make` to copy it into `public/`, and push:
the baulab.info webhook serves `public/`. To preview locally, serve `public/`
over HTTP (the page fetches `data/*.json`), e.g.
`python -m http.server -d public 8000`.

The server sends no cache headers, so browsers may keep an old `style.css`:
when you change it, bump the `?v=` on its `<link>` in `index.html`.

`src/data/*.json` and `src/media/teaser.gif` are written by
`filter/project_page/build.py` in the main
[influence-benchmarking-hops](https://github.com/Lamsheeper/influence-benchmarking-hops)
repository.
