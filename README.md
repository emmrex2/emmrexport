# EMMREX — cinematic portfolio

Static site, no build step. Deploy as-is on Vercel.

## Deploy
- **Fastest:** vercel.com/new → drag this whole folder in → Deploy.
- **CLI:** `npm i -g vercel`, then inside this folder run `vercel --prod`.
- **GitHub:** push this folder to a repo, import it in Vercel, Framework = "Other", no build command, output directory = `.`

## Edit
Everything lives in `index.html`. Search for these near the top of the `<script>`:
- `CONFIG` — email, WhatsApp number, 
- `PROJECTS` — the 6 rooms. Replace title, description, tech, result, liveUrl, and set `sample:false`.
- `IMGS` — points to files in `assets/projects/`. Overwrite them with your real screenshots
  (same file names; 16:9 landscape ~1280x720; `frame0-2` are 9:16 portrait) or change the paths.
- `SERVICES` — the 10 services shown in the lobby.

## Contact form
It opens the visitor's email app pre-filled and offers WhatsApp. To receive submissions directly,
add a Vercel serverless function or a form service (Formspree, Resend) and post the form to it.

## Notes
- `vendor/three.min.js` is Three.js r128, bundled so no CDN is needed for 3D.
- The 6 project screenshots are fictional samples. Replace them before presenting as real client work.
