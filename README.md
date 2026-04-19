# Safaricom SMS Bundle Simulator

An interactive browser-based simulator that replicates the Safaricom `*188#` SMS bundle experience. The application runs entirely in a single HTML file with no dependencies or build tools required.

It offers two modes of interaction: a modern web catalog for browsing and purchasing bundles, and a USSD dialog simulator that mirrors the real numeric menu flow you see when dialing `*188#` on a Safaricom line.

---

## Modes

### Web Mode

A structured bundle catalog displaying all available SMS bundles organised by type: Daily, Weekly, and Monthly. Each bundle card shows the SMS count, price, validity period, and a Fair Usage Policy notice for unlimited bundles.

Selecting a bundle opens a confirmation modal where you choose your payment method (Airtime or M-PESA) before the purchase processes. A simulated spinning indicator appears during the 2-second processing delay, after which the balance is deducted and a confirmation toast is shown.

Additional web mode features:

- **Top-up control** in the account strip — enter any amount between Ksh 5 and Ksh 9,999 to add simulated airtime
- **Purchase history panel** below the catalog — every purchase is logged with its bundle type, time, payment method, and price
- **Balance flash** — the top-bar balance chip turns green briefly whenever a balance change occurs
- **Ripple animation** on the Buy Now button

### USSD Mode

A pixel-faithful replica of the real Safaricom USSD dialog. Press "Dial *188#" to open a session on the simulated phone screen. Navigate using numeric replies, exactly as you would on a real handset.

USSD mode features:

- Simulated phone frame with status bar showing live clock, animated signal bars, network label, and battery indicator
- 20-second session countdown timer with a visible progress bar that pulses red in the final 5 seconds
- Screen transition animations between each USSD screen
- Input field shake animation on invalid entry
- Animated processing screen with bouncing dots
- SMS notification banner that slides down over the phone screen after a successful purchase, replicating a real Safaricom confirmation SMS
- Slow network toggle — switches processing delay between 1.8 seconds (fast) and 3.5 seconds (slow) for demonstrating the processing state
- `aria-live` region on the USSD content area so screen readers announce screen changes

---

## Bundle Catalogue

All bundle data is sourced from the official Safaricom SMS Bundles Terms and Conditions, Section 2 (last updated August 2023).

### Daily SMS Bundles — valid 24 hours

| SMS | Price (Ksh) |
|-----|-------------|
| 20  | 5           |
| 200 | 10          |
| Unlimited | 20  |

### Weekly SMS Bundles — valid 7 days, On-Net and Off-Net

| SMS | Price (Ksh) |
|-----|-------------|
| 100  | 20         |
| 1000 | 30         |
| Unlimited | 50 |

### Monthly SMS Bundles — valid 30 days, On-Net and Off-Net

| SMS  | Price (Ksh) |
|------|-------------|
| 1500 | 100         |
| 3500 | 200         |

Unlimited bundles are subject to a Fair Usage Policy of 1,000 SMS per day and 7,000 SMS per week.

---

## USSD Flow

The complete flow available in USSD mode:

```
Dial *188#
  1. Buy SMS Bundles
       1. Daily SMS   → select bundle → confirm → payment → processing → success
       2. Weekly SMS  → select bundle → confirm → payment → processing → success
       3. Monthly SMS → select bundle → confirm → payment → processing → success
  2. Check Balance    → shows airtime balance and active bundles (terminal)
  3. Buy for Another Number → enter recipient number → category → bundle → confirm → payment → success
  4. Unsubscribe      → confirm → processing → success
```

Payment method is selected on a dedicated screen (Airtime or M-PESA) before processing begins. If the balance is insufficient, a clear error message is shown without deducting anything.

---

## Simulated Account

The application maintains a simulated account state for the duration of the browser session:

- Starting airtime balance: Ksh 150.00
- Balance decreases by the bundle price on each successful purchase
- Balance increases using the top-up control in the account strip
- Active bundles are displayed in the account strip and in the USSD balance check screen
- All purchases are logged in the purchase history panel (web mode)

---

## Keyboard Support

| Key | Action |
|-----|--------|
| Enter | Submit USSD reply |
| Escape | Close web confirm modal or end USSD session |
| Tab / Shift+Tab | Cycle through focusable elements; trapped inside the modal while it is open |

All interactive elements have visible focus rings when navigated by keyboard. Animations are disabled automatically when the operating system has `prefers-reduced-motion` enabled.

---

## Installation

```bash
git clone https://github.com/Martin888Maina/JS-Safaricom-SMS-Bundle-Program.git
cd JS-Safaricom-SMS-Bundle-Program
```

Open `index.html` in any modern web browser. No server, build tools, or internet connection required (fonts load from Google Fonts if available).

---

## Usage

**Web Mode:**
1. Open `index.html` in a browser
2. Use the top-up field in the account strip to adjust your simulated balance if needed
3. Select a bundle tab: Daily, Weekly, or Monthly
4. Click "Buy Now" on the desired bundle
5. Choose payment method in the confirmation modal
6. Click Confirm — the purchase processes and your balance updates

**USSD Mode:**
1. Switch to "USSD Mode" using the toggle in the top bar
2. Optionally enable "Simulate slow network" to extend the processing delay
3. Click "Dial *188#" to open a session
4. Read the menu and type a number to navigate
5. Press Enter or tap "Send" to submit each reply
6. Follow the flow through bundle selection, confirmation, and payment
7. Press Escape at any time to end the session

---

## Technology Stack

- HTML5, CSS3, JavaScript ES6+ — no frameworks or build tools
- Google Fonts: Inter and Poppins
- Single file: `index.html`

---

## Project Structure

```
JS-Safaricom-SMS-Bundle-Program/
├── index.html                  Main application file
├── favicon.png                 Project favicon
├── README.md                   Project documentation
├── LICENSE                     MIT License
├── .gitignore                  Excludes local implementation guides
```

---

## Browser Compatibility

- Google Chrome 90 and above
- Mozilla Firefox 88 and above
- Microsoft Edge 90 and above
- Safari 14 and above

---

## Disclaimer

This is a simulator built for educational and portfolio purposes. It does not connect to Safaricom's network and does not perform real transactions. Bundle data is based on publicly available Safaricom Terms and Conditions. For actual bundle purchases, dial `*188#` on a Safaricom line or visit the official Safaricom website at www.safaricom.co.ke.

---

## License

MIT License. See the [LICENSE](LICENSE) file for details.

---

## Author

Martin Maina — [github.com/Martin888Maina](https://github.com/Martin888Maina)
