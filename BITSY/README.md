# BITSY — Financial Literacy Simulator

A browser-based MVP for an adaptive financial-literacy and virtual stock-market learning platform.

## Run it
1. Extract the ZIP.
2. Open the `BITSY` folder.
3. Double-click `index.html` in a recent version of Chrome or Edge.

No server or Google account is required.

## New: local learner accounts and BITSY levels
- Create an account with name, email and password, or log in with an existing local account.
- After first login, users can take a 6-question baseline assessment or skip it.
- The score assigns one of three companion levels:
  - **BITSY Novice (0–2 correct):** pacifier-wearing beginner companion.
  - **BITSY Intermediate (3–4 correct):** glasses-wearing, bookish companion.
  - **BITSY Supra (5–6 correct):** neon cyber companion for more advanced learning.
- The assigned character appears in the learner profile and dashboard.
- Each account has its own saved simulator, lesson and activity data in that browser.
- The three avatars are used in the Learn area: the level determines the teaching depth, examples and knowledge-check questions. Novice uses plain-language foundations, Intermediate uses applied scenarios, and Supra uses advanced analytical material. The avatar is not a trading recommendation or risk rating.

## Existing features
- Learner dashboard and ₹1,00,000 virtual balance
- Six financial-literacy lessons with knowledge checks
- Illustrative stock market simulator and virtual buy/sell transactions
- Portfolio holdings, allocation and profit/loss calculations
- BITSY educational assistant with rule-based responses
- Pre-trade BITSY decision review before every virtual buy or sell, including potential advantages, disadvantages, concentration and cash impact
- Post-trade logging and monitoring of held stocks after each simulated market update
- Transaction and learning activity history
- Browser localStorage persistence
- Responsive desktop and mobile layout

## Important prototype limitations
- **Authentication is local-demo authentication only.** Accounts and password hashes are stored in the current browser's localStorage; there is no server, database, password recovery, email verification or cross-device sign-in. Do not use a real or reused password. This must be replaced with secure backend authentication before public deployment.
- Passwords are salted and hashed with PBKDF2 (Web Crypto, 120,000 iterations), but this client-only approach is not a substitute for production password hashing and server-side authentication.
- All market data and prices are illustrative, not live NSE/BSE data.
- No real money or real trading is involved.
- BITSY is a rule-based educational demo, not a connected LLM or financial adviser.
- Clearing browser storage removes local accounts and learner data.

## Suggested presentation flow
1. Create a learner account and log in.
2. Take the 6-question level check and show the assigned BITSY avatar.
3. Complete a financial-literacy lesson and its knowledge check.
4. Open Market Simulator and buy a small quantity of a virtual stock.
5. Open My Portfolio to show holdings and allocation.
6. Select a stock and review BITSY’s advantages, disadvantages and portfolio-impact warning before confirming or cancelling the virtual trade.
7. Ask BITSY: “How risky is my portfolio?”
7. Trigger “Simulate market move” and show how portfolio values update.
8. Open Activity to show recorded learning and trading history.

## Reset demo data
Open browser developer tools → Console and run:
`localStorage.clear(); location.reload();`

## Project structure
- `index.html` — complete app (HTML, CSS and JavaScript)
- `bitsy-mascot.png` — original main BITSY character artwork
- `bitsy-novice.png` — Novice avatar
- `bitsy-intermediate.png` — Beginner avatar
- `bitsy-supra.png` — Supra avatar
- `README.md` — setup, features, limitations and demo guide

## Profile menu and mascot branding
- The sidebar brand mark uses the BITSY mascot artwork.
- The top-right profile button opens a learner summary with name, account email, simulated holdings, remaining virtual cash, invested value, total portfolio value, simulated P/L and BITSY learning level.
- The menu closes when the user clicks outside it. Log out is available inside the profile menu.

## Retake assessments and previous results
- The 6-question level assessment is always available from the Learn page using **Retake assessment**.
- Each completed attempt is saved separately to that learner's local browser profile.
- The Learn page displays previous attempts, date/time, score and assigned BITSY level.
- The latest attempt is compared with the previous attempt by score and level, showing score improvement or change.
- Skipping the initial assessment does not create a test result; the learner can take it later.
- BITSY artwork is embedded into the HTML as data images, so it can render even if the PNG files are moved. The PNG files remain included in the project folder as well.
