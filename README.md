# Wedding Invitation Demo

Ek upgraded digital wedding invitation ki demo static site — sales hub, personalized invitation aur host ke liye RSVP dashboard, teeno ek hi jagah.

## Pages

| Page | Kaam |
|---|---|
| `index.html` | **Sales hub** — packages/pricing, demo links aur WhatsApp enquiry. Yahi se shuru karo. |
| `invite.html` | **Invitation demo** — Sumit & Nidhi ki shaadi ka invitation: events, venue, photo carousel (assets/photo-1.jpg … photo-5.jpg) aur RSVP form. |
| `dashboard.html` | **Host dashboard** — saare RSVP ek jagah: guest list, attending counts, event-wise aur food-wise summary, CSV export. |

## Demo links kaise kholein

Locally (folder ke andar se):

```bash
python3 -m http.server 8000
```

Phir browser mein:

- Sales hub: http://localhost:8000/index.html
- Invitation (aam): http://localhost:8000/invite.html
- Invitation (personalized): http://localhost:8000/invite.html?g=Sharma+Parivar
- Dashboard: http://localhost:8000/dashboard.html

GitHub Pages par host hone ke baad yahi links `https://<owner>.github.io/wedding-invitation-demo/` se khulenge (jaise `.../invite.html?g=Sharma+Parivar`).

### Personalization (`?g=`)

`invite.html?g=Sharma+Parivar` kholne par:

- Greeting "Namaste, Sharma Parivar" ho jati hai.
- RSVP form mein naam pehle se bhara (prefill) aata hai.
- Har guest ke liye apna link banaya ja sakta hai — bas `?g=` ke baad unka naam/parivar likh do (space ki jagah `+`).

## localStorage demo note

Ye ek **static demo** hai — koi backend/server database nahi hai.

- `invite.html` ka RSVP form jawab ko **usi browser ke** localStorage mein key `sn_rsvps_v1` ke under save karta hai (fields: `name`, `attending`, `count`, `events`, `food`, `note`, `ts`, `guest`).
- `dashboard.html` wahi key (`sn_rsvps_v1`) padhkar live RSVP dikhata hai; iske alawa dashboard mein kuch sample data bhi dikhta hai taaki khaali na lage.
- Isiliye RSVP aur dashboard **ek hi browser/device** par test karne hain — dusre phone ke RSVP is dashboard mein nahi dikhenge. Asli client version mein ye data server par jayega.

## Files

```
index.html        sales hub
invite.html       personalized invitation + RSVP form
dashboard.html    host RSVP dashboard
assets/           photo-1.jpg … photo-5.jpg
```
