# Privacy Policy

This Privacy Policy describes how **Zvycha** (“we”, “us”, or “our”) collects, uses, stores, and discloses information from users (“Users”) of:

- The **Zvycha habit tracker application** (Flutter app and **BackEnd_Tracker** API), and
- The **Zvycha marketing / landing website**, including the beta email signup.

This policy applies to those products and related services we offer under the Zvycha name.

## Content Overview

- [What data we collect](#what-data-we-collect)
- [How we use your data](#how-we-use-your-data)
- [Sharing your data](#sharing-your-data)
- [Retention](#retention)
- [Security](#security)
- [Your rights](#your-rights)
- [Changes to this policy](#changes-to-this-policy)
- [Contact](#contact)

## What data we collect

**Account (tracker):** email, username, password (stored on the server only as a **bcrypt hash** after sign-up; sent in plain form over HTTPS only for login or password change), internal **user id** (UUID), and **timestamps** on records.

**Activity and content you create in the app:** room names; habit names; pet names and related game fields; progress tied to your account; friend relationships; friend requests and their status.

**Landing (beta waitlist):** email address you submit (normalized and stored via **Supabase**).

**On your device:** access **token**, username, and user id in **Flutter Secure Storage** (mechanism on web depends on the platform).

**Automatically (depends on hosting):** IP address and HTTP metadata in server or serverless **logs**; **JWT** payload used for API auth (treat tokens as sensitive). **Redis** is used as a Celery broker/backend for scheduled jobs, not as the main user profile store.

**Third-party delivery:** **Google Fonts** on the landing may cause Google to receive technical data (e.g. IP, referrer). We do not use custom analytics cookies in the reviewed app code; hosting may set essential cookies.

## How we use your data

To run the tracker (accounts, sync, friends, rooms, habits, pets, progress), operate the waitlist, secure and improve the services, and comply with law where required.

If you are in the **EEA**, **UK**, or similar regions, applicable law (e.g. **GDPR**) may give you extra rights; see [Your rights](#your-rights).

## Sharing your data

We do not sell your personal information. We share data with **service providers** as needed to operate the product, including **Supabase** (waitlist storage), **hosting** for the API, database, Redis/Celery, and the landing (e.g. **Vercel** if you use it), and **Google** (fonts). We may disclose information if required by law or to protect rights and safety.

**Other users** may see usernames, friend links, room membership, and content in shared rooms according to how the app works.

## Retention

We keep data while your account exists and as needed after that for legal or operational reasons. You can delete your tracker account via the API (`DELETE /users/user/me/delete`). Waitlist emails remain until you remove them from Supabase or your own policy says otherwise. Logs follow your host’s settings.

## Security

We use **bcrypt** for passwords, **Bearer JWT** for the API, **HTTPS** in production, and server-side secrets (e.g. Supabase service role) not exposed in the client bundle. No method is perfectly secure.

## Your rights

Depending on where you live, you may ask to **access**, **correct**, **delete**, **restrict**, or **object** to processing, request **portability**, **withdraw consent** where it applies, or **complain** to a supervisory authority. Contact us below; we may verify your identity.

**International transfers:** If servers are in a different country than you, data may be transferred; use appropriate safeguards (e.g. standard contractual clauses) where the law requires.

## Changes to this policy

We may update this policy and change the “last updated” date below. Material changes may require further notice under applicable law.

## Contact

For questions or help open an issue or contact the maintainers listed in the repository. 

_Last updated: **March 25, 2026**_
