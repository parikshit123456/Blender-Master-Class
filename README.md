# Blender Masterclass – Freelance Edition | Landing Page

A modern, dark-themed, single-page landing page built with plain HTML, CSS,
and JavaScript — no frameworks, no build step, no backend.

## Folder Structure

```
Course-Landing-Page/
│
├── index.html
├── style.css
├── script.js
│
├── images/
│   └── course-thumbnail.jpg   (placeholder — replace with your real thumbnail)
│
└── README.md
```

## How to Run

Just open `index.html` in any browser. No build tools, no server, no
dependencies to install.

For local development with live reload, you can optionally use any static
server, e.g.:

```bash
npx serve .
```

## Before You Publish — Things to Replace

Search the code for `REPLACE HERE` comments — every spot you need to edit is
marked. Here's the full list:

| What | Where | How |
|---|---|---|
| **Razorpay payment link** | `index.html` — `#navBuyBtn`, `#heroBuyBtn`, `#featuresBuyBtn`, `#floatingBuyBtn` | Change the `href="#"` to your Razorpay payment link. |
| **WhatsApp link** | `index.html` — `#heroWhatsappBtn`, the "Message on WhatsApp" button, `#floatingWhatsapp` | Change `href="#"` to `https://wa.me/916297179352` (or your number, no spaces/symbols). |
| **Contact form's WhatsApp number** | `script.js` — `OWNER_WHATSAPP_NUMBER` constant at the top of the file | Set it to your number in `<countrycode><number>` format, digits only (e.g. `'916297179352'`). This is where the contact form sends its generated message. |
| **YouTube preview video** | `index.html` — inside `<section id="preview">`, the `<iframe src="...">` | Replace with `https://www.youtube.com/embed/YOUR_VIDEO_ID`. |
| **Course thumbnail image** | `images/course-thumbnail.jpg` | Replace the file with your real thumbnail (keep the same filename, or update the `src` in `index.html`). |
| **Email address** | `index.html` — contact section, `mailto:` link | Update if your email ever changes. |
| **Phone number** | `index.html` — contact section text | Update the displayed number to match your WhatsApp link. |

## Contact Form → WhatsApp

The contact section now has a form asking for **Name, State, Email, Phone
Number, and Blender Experience** (Just Started / Intermediate / Pro). On
submit, `script.js`:

1. Validates every field (required, valid email format, valid 10-digit
   Indian mobile number).
2. Builds a plain-text message from the values.
3. Opens `https://wa.me/OWNER_WHATSAPP_NUMBER?text=...` in a new tab with
   that message pre-filled — the visitor just taps send from WhatsApp.

There's no backend or database involved — the browser does all of this
client-side. Set `OWNER_WHATSAPP_NUMBER` in `script.js` to your own number
before publishing.

## Notes

- All animations (fade-in on scroll, floating thumbnail, hover states, mobile
  menu) are handled with pure CSS + vanilla JS — no libraries.
- The design respects `prefers-reduced-motion` for accessibility.
- Fully responsive: mobile, tablet, laptop, desktop — tested with Flexbox and
  CSS Grid, no horizontal scroll at any width.
- Font used: [Poppins](https://fonts.google.com/specimen/Poppins) via Google
  Fonts CDN.
