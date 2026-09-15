# DISTORTER — project page

The page the paper cites: <https://qjawls12.github.io/DISTORTER/>

## Publishing it

1. Create a **public** repository named `DISTORTER` under the `qjawls12` account.
2. Push the contents of this directory to `main`.
3. Settings → Pages → Source: **Deploy from a branch** → `main` → `/ (root)`.
4. The address above is live a minute or two later.

The repository name decides the path and is case-sensitive, so `DISTORTER` gives
`/DISTORTER/`, not `/distorter/`.

## Adding the audio examples

Drop the files into `audio/` under the names `index.html` already references:

| Slot | Files |
|---|---|
| One input, three modes | `example1_input.wav`, `example1_scream.wav`, `example1_growl.wav`, `example1_shriek.wav`, and the same with `example2_` |
| Intensity sweep | `sweep_m3.wav`, `sweep_m1.wav`, `sweep_0.wav`, `sweep_p075.wav`, `sweep_p15.wav` |

Only publish material you are free to redistribute. EMO, EMVD, VCTK and VocalSet
are all CC BY 4.0, so conversions of those inputs can go up with credit.
**GTSinger is CC BY-NC-SA 4.0**: keep it off this site, since the page and the
paper are both CC BY 4.0 and cannot carry a NonCommercial-ShareAlike derivative.

Keep each clip short. GitHub recommends staying under 1 GB per repository and
refuses single files over 100 MB.

## Keeping the live-demo link current

The research demo runs behind a Cloudflare quick tunnel, whose hostname changes
every time it restarts, and it is invitation-only: the bare origin answers 404
without the invite cookie. So the paper cites **this page**, never the tunnel.

When the tunnel is restarted, edit the one line in `index.html` marked

```html
<!-- LIVE DEMO LINK -- edit this one line whenever the tunnel is restarted. -->
```

and push. The address in the paper never changes.

If a stable endpoint is wanted later, an ngrok free static domain gives a
permanent `*.ngrok.app` hostname without buying a domain, within its free
allowance of 20k requests and 1 GB per month. A Cloudflare *named* tunnel is the
other option, but it needs a domain you own.

## Files

```
index.html     project page: summary, figure, audio slots, live-demo link
credits.html   dataset and component attribution, linked from every footer
style.css      one stylesheet, light and dark
figures/       inference panel and demo screenshot, copied from the paper
audio/         empty; see above
```
