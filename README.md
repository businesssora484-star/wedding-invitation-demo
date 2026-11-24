# Wedding Invitation Demo

Ek upgraded digital wedding invitation ki demo static site — sales hub aur personalized invitation, dono ek hi jagah.

## Pages

| Page | Kaam |
|---|---|
| `index.html` | **Sales hub** — packages/pricing, demo links aur WhatsApp enquiry. Yahi se shuru karo. |
| `invite.html` | **Invitation demo** — Sumit & Nidhi ki shaadi ka invitation: "Shubh Vivaah" book opening, tassel pull-reveal date, swipe function cards (Haldi, Mehendi, Sangeet, Baraat & Pheras), photo gallery (assets/photo-1.jpg … photo-5.jpg), Grand Reception, venue map, countdown aur background music. |

## Demo links kaise kholein

Locally (folder ke andar se):

```bash
python3 -m http.server 8000
```

Phir browser mein:

- Sales hub: http://localhost:8000/index.html
- Invitation (aam): http://localhost:8000/invite.html
- Invitation (personalized): http://localhost:8000/invite.html?g=Sharma+Parivar

GitHub Pages par live: https://businesssora484-star.github.io/wedding-invitation-demo/

### Personalization (`?g=`)

`invite.html?g=Sharma+Parivar` kholne par:

- Invitation mein greeting "Namaste, Sharma Parivar" dikhti hai.
- Har guest ke liye apna link banaya ja sakta hai — bas `?g=` ke baad unka naam/parivar likh do (space ki jagah `+`).

## Files

```
index.html        sales hub
invite.html       personalized invitation (original light festive theme)
assets/           photo-1.jpg … photo-5.jpg
```
