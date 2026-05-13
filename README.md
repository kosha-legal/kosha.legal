# Kosha — Privacy Policy

**Effective date:** 9 May 2026
**Last updated:** 13 May 2026

Kosha is a personal library cataloguing app for books and board games. This page describes what data the app collects, why, and how it's handled. It's written to be understandable rather than to impress lawyers — if anything is unclear, email **garveeta09@gmail.com** and we'll explain.

This policy applies to the Kosha mobile app distributed via TestFlight (and, in future, the Apple App Store and Google Play Store).

## What Kosha is, in one paragraph

Kosha lets you photograph books you own, get them automatically identified, organise them by location (e.g. "My house", "Parents' house"), and optionally share your library with a small circle of friends you connect with on Kosha. Friend connections and library sharing are opt-in: you decide whether your library is private or visible to friends, and you decide whether to send or accept any individual friend request.

## What information Kosha collects

When you sign up and use the app, Kosha collects:

- **Account information.** Depending on how you sign in: your email address (when you sign in with Email or Google) or your phone number (when you sign in with Phone). Your name comes from your Google account if you sign in with Google, or is entered manually otherwise. If you sign in with Email or Google, you can also optionally add your phone number so friends can find you on Kosha through their contacts; this is never required. Authentication, including SMS one-time-passcode delivery for phone sign-in, is handled by Firebase Authentication; Kosha never sees your Google password or your verification codes.
- **Your library.** The books and other items you add — titles, authors, covers, genres, your reading status, your ratings, notes, your reading start/finish dates, the location label you assigned, and any tags or metadata you supply.
- **Photos you take or pick.** When you scan a book cover, the photo is sent to the book identification service (see "Service providers" below) and, where useful, the resulting cover image URL is stored alongside the item. Photos that aren't successfully identified are not uploaded to long-term storage; they're processed in transit.
- **Friend connections.** If you accept or send a friend request, Kosha stores a small record linking the two accounts (who is connected to whom, and who initiated the connection). This is what lets the app show you your friends' libraries on the "Circle" tab. You can decline incoming requests; declined connections are not surfaced to either party as friendships.
- **Contacts you check against Kosha (in transit only).** If you choose to find friends from your address book, Kosha asks your operating system for permission to read your contacts. The email addresses and phone numbers from your contacts are sent to a Kosha server function which checks them against the list of registered Kosha accounts and returns only the matches. **Your contacts are not stored on Kosha's servers** — they're used once to compute the match and then discarded. The full address-book content never persists outside your device.
- **App preferences.** Locally on your device, Kosha remembers small UI preferences such as your selected view mode (shelf / grid / list) and sort order. These never leave your device.
- **Crash reports.** When the app crashes or hits an unexpected error, a stack trace and basic device context (operating system version, app version, device model) are sent to our crash-reporting service so we can fix the bug. These reports do not include the contents of your library, the photos you've taken, or anything you've typed. See the Sentry row of the Service Providers table below.

Kosha does **not** collect:

- Advertising or marketing identifiers.
- Your location or device identifiers.
- Behavioural analytics — we do not track which screens you visit, which features you use, or how long you spend in the app.
- Payment information of any kind.

## How Kosha uses your information

Your data is used solely to provide the app's functionality:

- Authenticating you when you sign in.
- Storing your library so it's there when you reopen the app or sign in on another device.
- Identifying books from photos you scan.
- Enriching item details (genre, publisher, year, page count) from public book databases.
- Finding which of your contacts are already on Kosha (only when you actively use the contacts-picker feature), and letting you send and accept friend requests.
- Showing your library to friends you've connected with, if and only if you've set your library visibility to "Share with friends" (the alternative, "Track privately", keeps your library hidden even from people you're connected to).

Kosha does not use your data for advertising, profiling, or any commercial purpose beyond running the app for you.

## Service providers (subprocessors)

To operate, Kosha uses a small number of third-party services. Each receives only the data needed for its specific job:

| Service | Run by | What it does | What it sees |
|---|---|---|---|
| Firebase Authentication | Google LLC | Sign-in, password reset, session management, and SMS one-time-passcode delivery for phone sign-in | Your email, name, phone number (if you use Phone sign-in or add it to your profile), and authentication tokens |
| Cloud Firestore | Google LLC | Stores your library, account data, and friend connections | All library data you save in the app, plus friendship records |
| Firebase Storage | Google LLC | Stores cover photos that aren't sourced from public databases | Cover images you upload |
| Cloud Functions for Firebase | Google LLC | Runs Kosha's server-side contacts-matching logic (looking up which contacts are on Kosha) | Lowercased emails and phone numbers from your address book, only during the matching call; not stored after the call returns |
| Claude API (Vision) | Anthropic, PBC | Identifies book titles and authors from photos you scan | The photos you submit for identification (not stored beyond the API call) |
| Google Books API | Google LLC | Looks up book metadata (cover, ISBN, year, etc.) | Search queries (typically a title + author or ISBN) |
| Sentry | Functional Software, Inc. (Sentry) | Crash and error reporting so we can fix bugs | Stack traces of crashes, app version, OS version, device model. No library contents, no photos, no typed text. |

These services are bound by their own privacy and data-processing terms. Their data is not used by Kosha for any purpose other than what's described above.

Note: data processed by these services is hosted on infrastructure operated primarily in the United States. By using Kosha, you understand that your data may be transferred outside your country of residence.

## Sharing

Kosha does not sell, rent, or share your personal data with anyone outside the service providers listed above. There is no advertising network, no analytics broker, and no third-party SDK collecting data behind the scenes.

**Sharing with friends on Kosha.** If you set your library visibility to "Share with friends" and you've accepted a friend request from another Kosha user, the following becomes visible to that friend: your name, the titles, authors, covers, and reading status of books in your library, and (in future versions) your ratings and reading dates. Your private notes, your home and parents'-house location labels, and any items you've explicitly marked as private remain hidden. You can switch your library visibility back to "Track privately" at any time in Settings, which immediately hides your library from anyone you're connected to. You can also decline incoming friend requests; the other party is not notified that you declined.

## Your choices and permissions

Kosha asks for three device permissions, each only when you use the corresponding feature:

- **Camera** — to take a photo of a book cover or shelf for identification.
- **Photo library** — to pick an existing photo for identification.
- **Contacts** — to find which of your contacts are already on Kosha when you choose to invite friends. As explained in "What information Kosha collects" above, your address book is not stored on Kosha's servers; matching happens once per check and the contact data is discarded.

You can revoke any permission at any time from your device's Settings → Kosha. The corresponding features will stop working until you grant access again; nothing else changes.

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
