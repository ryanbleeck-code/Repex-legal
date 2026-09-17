[privacy_1.md](https://github.com/user-attachments/files/32068391/privacy_1.md)[Uploading privacy_1.m# Privacy Policy — Repex

**Last updated: 17 September 2026**

Repex is an iOS app for tracking strength training, made by Ryan Bleecke ("I", "me"), an individual developer based in France.

This policy explains what data Repex handles, where it goes, and what your rights are. It is written to be read, not to hide things.

**Contact: repexadmin@gmail.com**

---

## The short version

- Repex works **without an account**. If you never sign in, your training data never leaves your phone.
- If you sign in, your data is backed up to a private database so you can recover it if you lose or change your phone. Only you can read it.
- The AI Coach feature is **off until you turn it on**. If you turn it on, your workout numbers (exercise names, weights, reps, dates) are sent to an AI provider to generate its messages. Your name, photo, email and body measurements are never sent.
- There is no advertising, no analytics, no tracking, and no selling of data to anyone. Ever.

---

## 1. Data stored on your device

By default, everything Repex records stays on your phone:

- Workouts: exercises, sets, weights, reps, dates and times, session duration, rest times between sets
- Your training splits and programmes
- Gyms you have added, their equipment lists, and any gym photo you add
- Your profile: name, profile photo, height, and body-weight entries, if you choose to add them
- App settings: units, language, timer preferences, theme
- Counts of how many times the app was sent to the background during a workout (used by Coach to distinguish distraction from fatigue)

If you never sign in, none of this is transmitted anywhere.

---

## 2. Data stored in the cloud (only if you sign in)

Signing in is optional and exists so your training record survives a lost or replaced phone.

**Sign-in providers.** You may sign in with Apple or Google. Repex receives an account identifier and, unless you use Apple's "Hide My Email" feature, an email address. Repex never sees or stores your password.

**What is uploaded when signed in.** Everything listed in Section 1 is copied to a private database hosted by Supabase (servers located in Ireland, EU):

- Your full workout history, including timestamps for individual sets
- Your splits and programmes
- Your app settings
- Your profile, including your name, profile photo, height and body-weight history
- Your gyms, their equipment lists, and gym photos
- Feedback you give on Coach messages (see Section 4)

Photos are uploaded as part of your settings data. There is currently no way to back up your workouts without also backing up any photos you have added. If you do not want photos stored in the cloud, do not add them while backup is enabled.

**Who can read it.** Database access rules restrict every record to its owner. Only your signed-in account can read your data. I have administrative access to the database as its operator, but do not read individual users' training records except where strictly necessary to fix a fault you have reported.

**One aggregate use.** To decide which exercises to add to the built-in library, I periodically look at the exercise *names* in backed-up workouts and splits — in aggregate, as a ranked list of names with counts, not per person. This only covers accounts with backup turned on; nothing is read from a phone that has not signed in.

---

## 3. The AI Coach

**Coach is opt-in.** It does nothing until you switch it on.

When Coach is enabled, Repex sends a short text summary of your training to Anthropic's AI service, via a server I operate on Cloudflare, in order to generate Coach's messages.

**What is sent:**
- Exercise names (including any custom names you have typed)
- Weights, reps, and estimated one-rep-max figures
- Session dates, day names, and rest-gap patterns
- Calculated observations such as plateaus, trends and imbalances
- Your language setting
- If you use the "import a programme" feature, the text you paste

**What is never sent:** your name, email, profile photo, gym names, gym photos, body weight, height, or any account identifier.

Each request is standalone. No conversation history is retained between messages.

**Technical details.** Requests pass through my server, which attaches a random per-installation identifier and your IP address only for the purpose of rate limiting. Both are irreversibly hashed before being briefly stored, and neither is forwarded to Anthropic. Cloudflare, as the hosting provider, records standard connection metadata. Anthropic processes the request under its commercial API terms; Anthropic does not use commercial API inputs to train its models.

**You can turn Coach off at any time** in Settings. Doing so stops all transmission immediately.

---

## 4. Coach feedback

If you mark a Coach message as helpful or not helpful, Repex records that vote together with the message text and the data summary Coach was given when it wrote it. That summary contains your workout numbers.

This feedback is used solely to improve Coach's accuracy and usefulness. It is stored in the same private database and is readable by me as the operator. Feedback is not shared, sold, or published.

---

## 5. Sharing

If you share a workout, a recap or a split, that content is passed to whichever app you choose in the iOS share sheet. What happens to it after that is governed by that app and by whoever you send it to. Repex does not retain or transmit shared content itself.

Note that a shared split contains the exercise names and structure of that split in readable form.

---

## 6. What Repex does not do

- No advertising, ad networks, or ad identifiers
- No analytics, crash reporting, or usage telemetry
- No location tracking
- No health data from Apple Health or any other source
- No selling, renting, or sharing of your data with third parties for their own purposes
- No profiling for marketing

---

## 7. Data retention

Data on your device stays there until you delete it or delete the app.

Data in the cloud is kept while your account exists. You can request deletion of your account and all associated data at any time by emailing **repexadmin@gmail.com**, and I will action it within 30 days.

Coach feedback records are retained for the purpose of improving Coach and are deleted along with your account if you request deletion.

---

## 8. Your rights

If you are in the EU or UK, the GDPR gives you the right to access, correct, delete, restrict, object to, and receive a copy of your personal data. Repex also includes an in-app export of your data.

To exercise any of these rights, email **repexadmin@gmail.com**.

The legal bases for processing are: performance of a contract (providing the app and its backup feature), your consent (the AI Coach feature, which you enable explicitly), and legitimate interests (keeping the service secure and functioning).

You have the right to complain to your local data protection authority. In France, this is the CNIL (cnil.fr).

---

## 9. Children

Repex is not directed at children under 16 and should not be used by them. I do not knowingly collect data from children under 16. If you believe a child has provided data, email me and it will be deleted.

---

## 10. Data processors

The following services process data on my behalf:

- **Supabase** — database and authentication (EU, Ireland)
- **Cloudflare** — the server that relays Coach requests
- **Anthropic** — generates Coach's messages
- **Apple** — app distribution, and sign-in if you use it
- **Google** — sign-in only, if you use it

---

## 11. Security

Data in transit is encrypted. Database access is restricted per user. API credentials are held on the server, never inside the app. No system is perfectly secure, and I cannot guarantee absolute security, but I take reasonable measures appropriate to the scale of the service.

---

## 12. Changes

If this policy changes materially, the app will make the change apparent. The "last updated" date above always reflects the current version.

---

## 13. Contact

Ryan Bleecke
France
**repexadmin@gmail.com**
d…]()
