# Kosha — Privacy Policy

**Effective date:** 9 May 2026
**Last updated:** 9 May 2026

Kosha is a personal library cataloguing app for books and board games. This page describes what data the app collects, why, and how it's handled. It's written to be understandable rather than to impress lawyers — if anything is unclear, email **garveeta09@gmail.com** and we'll explain.

This policy applies to the Kosha mobile app distributed via TestFlight (and, in future, the Apple App Store and Google Play Store).

## What Kosha is, in one paragraph

Kosha lets you photograph books you own, get them automatically identified, organise them by location (e.g. "My house", "Parents' house"), and — in future versions — share your library with a small circle of friends. The current version (v1) is solo-only: there is no sharing between users yet. Friends features will arrive in a later release with their own opt-in choices.

## What information Kosha collects

When you sign up and use the app, Kosha collects:

- **Account information.** Your email address (always) and your name (from your Google account if you sign in with Google, or entered manually otherwise). Authentication is handled by Firebase Authentication; Kosha never sees your Google password.
- **Your library.** The books and other items you add — titles, authors, covers, genres, your reading status, your ratings, notes, your reading start/finish dates, the location label you assigned, and any tags or metadata you supply.
- **Photos you take or pick.** When you scan a book cover, the photo is sent to the book identification service (see "Service providers" below) and, where useful, the resulting cover image URL is stored alongside the item. Photos that aren't successfully identified are not uploaded to long-term storage; they're processed in transit.
- **App preferences.** Locally on your device, Kosha remembers small UI preferences such as your selected view mode (shelf / grid / list) and sort order. These never leave your device.

Kosha does **not** collect:

- Advertising or marketing identifiers.
- Your contacts, location, or device identifiers.
- Crash analytics or behavioural analytics in the current version. (A future version may add crash reporting; if so, this policy will be updated and you'll be notified.)
- Payment information of any kind.

## How Kosha uses your information

Your data is used solely to provide the app's functionality:

- Authenticating you when you sign in.
- Storing your library so it's there when you reopen the app or sign in on another device.
- Identifying books from photos you scan.
- Enriching item details (genre, publisher, year, page count) from public book databases.

Kosha does not use your data for advertising, profiling, or any commercial purpose beyond running the app for you.

## Service providers (subprocessors)

To operate, Kosha uses a small number of third-party services. Each receives only the data needed for its specific job:

| Service | Run by | What it does | What it sees |
|---|---|---|---|
| Firebase Authentication | Google LLC | Sign-in, password reset, session management | Your email, name, and authentication tokens |
| Cloud Firestore | Google LLC | Stores your library and account data | All library data you save in the app |
| Firebase Storage | Google LLC | Stores cover photos that aren't sourced from public databases | Cover images you upload |
| Claude API (Vision) | Anthropic, PBC | Identifies book titles and authors from photos you scan | The photos you submit for identification (not stored beyond the API call) |
| Google Books API | Google LLC | Looks up book metadata (cover, ISBN, year, etc.) | Search queries (typically a title + author or ISBN) |

These services are bound by their own privacy and data-processing terms. Their data is not used by Kosha for any purpose other than what's described above.

Note: data processed by these services is hosted on infrastructure operated primarily in the United States. By using Kosha, you understand that your data may be transferred outside your country of residence.

## Sharing

Kosha does not sell, rent, or share your personal data with anyone outside the service providers listed above. There is no advertising network, no analytics broker, and no third-party SDK collecting data behind the scenes.

In future versions of Kosha, you'll be able to opt in to sharing your library with a circle of friends you invite. That feature is not present in v1; when it arrives, this policy will be updated to describe exactly what's shared and with whom, and the choice will be yours to make per-account.

## Your choices and permissions

Kosha asks for two device permissions, each only when you use the corresponding feature:

- **Camera** — to take a photo of a book cover or shelf for identification.
- **Photo library** — to pick an existing photo for identification.

You can revoke either permission at any time from your device's Settings → Kosha. The corresponding features will stop working until you grant access again; nothing else changes.

## Data retention and deletion

Your library and account data are retained for as long as your account exists.

In v1, account deletion is a manual process: email **garveeta09@gmail.com** with the email address tied to your Kosha account and we'll delete your account and all associated data within 14 days. A future version will add self-serve account deletion in the app's Settings.

You can delete individual books, locations, or other items at any time from within the app; those deletions take effect immediately.

## Children

Kosha is not directed at children under 13 (or the equivalent minimum age in your jurisdiction). We do not knowingly collect data from children. If you believe a child has provided personal information to Kosha, please contact us and we will delete it promptly.

## Security

Authentication and storage are handled by Firebase services, which encrypt data in transit and at rest. No system is perfectly secure, but Kosha takes reasonable steps to protect your information and limits internal access to what's necessary to operate the service.

## Changes to this policy

If this policy changes in a way that affects how your data is handled, the "Last updated" date at the top will change and — for material changes — you'll be notified within the app or by email before the change takes effect.

## Contact

Questions, deletion requests, or anything else: **garveeta09@gmail.com**.
