# whack-a-mole

A historical vanilla JavaScript learning exercise adapted from
[kubowania/whack-a-mole](https://github.com/kubowania/whack-a-mole). Preserve that
tutorial attribution; this repository is not presented as an original game engine.

## Preview and play

With Python 3, run from the repository root:

```sh
python -m http.server 8000 --bind 127.0.0.1
```

Open `http://127.0.0.1:8000` and stop with Ctrl+C. The game begins on page load:
click the moving mole in the nine-square grid during the 60-second countdown.
Refresh to restart. No dependency installation, build or environment variables
are needed.

[`index.html`](index.html) defines the grid, [`style.css`](style.css) its appearance,
and [`app.js`](app.js) the random movement, mouse scoring and countdown.

## Known limitations

The current countdown stops its own interval at zero but leaves the mole's
movement interval and mouse handlers active. Keyboard gameplay and a restart
control are not implemented. No automated suite or CI workflow is committed;
this documentation review did not run browser gameplay. Changes should verify
scoring, duplicate clicks, countdown completion and restart behavior while
preserving the [MIT license](LICENSE) and tutorial provenance.
