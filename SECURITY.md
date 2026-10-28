# Security Policy

## Supported Versions

Memox is a continuously deployed web app. Only the latest version on the `main` branch is supported with security fixes.

| Version | Supported |
| ------- | --------- |
| Latest (`main`) | ✅ |
| Older commits | ❌ |

## Reporting a Vulnerability

Please **do not** open a public issue for security problems.

Report privately using GitHub's built-in tool:

1. Go to the **Security** tab of this repository.
2. Click **Report a vulnerability**.
3. Describe the issue and submit.

Please include:

- A clear description of the problem and its impact
- Steps to reproduce (URL, browser, account type if relevant)
- A proof of concept or screenshots, if you have them
- Any suggested fix

This project is maintained by one person, so responses are best effort. You can expect an acknowledgement within a few days, and I will keep you updated until the issue is fixed. Once it is resolved, you are welcome to be credited if you wish.

## Scope

In scope:

- Authentication and account handling
- Reading or modifying another user's portfolio data
- Cross-site scripting (XSS) or injection in the app
- Problems with the Firestore security rules
- Service worker or manifest issues that expose user data

Out of scope:

- The Firebase web config in `index.html` (`apiKey`, `projectId`, and so on). These values are public by design for Firebase web apps. Access is controlled by Firebase Authentication and Firestore security rules, not by hiding them.
- Vulnerabilities in third-party services (Firebase, Binance, CoinGecko, TradingView). Please report those to the respective vendors.
- Social engineering, spam, or denial-of-service testing
- Issues that require a compromised device or browser

## Safe Harbor

If you act in good faith, avoid accessing other users' data beyond what is needed to demonstrate the issue, and report it privately, I will not pursue action against you.

## Notes for Users

- Memox is a portfolio tracker only. It never asks for exchange API keys, private keys, or seed phrases. **Never enter those anywhere in the app.**
- Use a unique password for your account. Passwords cannot be recovered by the developer.
- Prices shown are indicative and are not financial advice.
