Stephanie Zhang studio site
===========================

A static site: index.html, images/, video/, audio/, fonts/. No build step.

Publish
  Drag this whole folder onto Netlify Drop (app.netlify.com/drop), or push it to
  GitHub Pages, Vercel or Cloudflare Pages, and point your domain at it.
  The largest file is video/bv-gameplay.mp4 (about 37 MB), within every host's limits.

Pages
  Every page is a <section>/<article> in index.html with an id starting "v-"
  (v-home, v-emergent-vessels, v-synthetic-cesia, v-bestiary-of-vanishings,
  v-info, v-exhibitions, v-curatorial, v-research, v-notebook).

The landing
  One work at a time, crossfading every eight seconds; hovering a work in the
  sidebar shows it. Each is a <figure class="slide"> in v-home. To change a slide,
  swap its image and caption.

Work pages
  Each work page has a hero (<div class="hero">), the wall label and statement
  (<div class="info">), then a gallery of rows (<div class="row">). Every item in a
  row has style="--ar:W/H;--nw:Wpx": --ar is its aspect ratio, which makes all items
  in a row share one height, and --nw is its native width, which it is never shown
  beyond. When you add an image, set both from its pixel size.

Videos and sound
  Videos are in video/ as MP4 (H.264, listed first) with a WebM fallback and a
  -poster.jpg, at their native resolution. They play muted and looped while on
  screen, pause when scrolled away or on changing page, and have a Pause/Play button;
  they never autoplay for visitors who prefer reduced motion. To add one, copy any
  <figure class="plate plate--video"> block and point it at your files.

  Four videos still come from Google Drive (data-drive="FILE_ID" on their <figure>):
  "Play video" first tries Drive's direct file link, then falls back to Drive's
  player. Those files must be shared as "Anyone with the link can view".

  The kk.Shucko track is audio/foyer-kkshucko.mp3, on the Synthetic Cesia page.

Curatorial
  The curatorial page holds One Molecule Said Yes to Another (And Life Was Born);
  its photographs are images/omsy-01.jpg to omsy-17.jpg.

Previewing locally
  Run "python3 -m http.server" inside this folder and open http://localhost:8000.
