# Privacy Policy — Repex

**Last updated: 3 November 2026**

Repex is an iOS app for tracking strength training, made by Ryan Bleecke ("I", "me"), an individual developer based in France.

This policy explains what data Repex handles, where it goes, and what your rights are. It is written to be read, not to hide things.

**Contact: repexadmin@gmail.com**

---

## The short version

- Repex works **without an account**. If you never sign in, your training data never leaves your phone.
- If you sign in, your data is backed up to a private database so you can recover it if you lose or change your phone. Only you can read it.
- Repex's AI features — Coach, reading a plan you import, and finding versions of an exercise for your gym's kit — use **Anthropic's Claude**. Nothing is sent to Anthropic until you say yes on a screen in the app that names it and lists what is shared. Your name, email, profile photo, body measurements and the heart rate or power you log are never sent, and neither is anything from Apple Health.
- **Apple Health is optional** and off until you switch it on. Health data is used only inside Repex and in your own backup; it is never sent to the AI provider, never used for advertising, and never sold.
- There is no advertising, no analytics, no tracking, and no selling of data to anyone. Ever.

---

## 1. Data stored on your device

By default, everything Repex records stays on your phone:

- Workouts: exercises, sets, weights, reps, dates and times, session duration, rest times between sets, and for cardio the distance, time, heart-rate zone and, if you type them in, average heart rate and power
- Your training splits and programmes
- Gyms you have added, their equipment lists, and any gym photo you add
- Your profile: name, profile photo, height, body-weight entries, and the body figure (male or female) used for the muscle maps, if you choose to add them
- App settings: units, language, timer preferences, theme
- Counts of how many times the app was sent to the background during a workout (used by Coach to distinguish distraction from fatigue)
- If you turn on Apple Health: the data described in Section 3

If you never sign in, none of this is transmitted anywhere.

---

## 2. Data stored in the cloud (only if you sign in)

Signing in is optional and exists so your training record survives a lost or replaced phone.

**Sign-in providers.** You may sign in with Apple or Google. Repex receives an account identifier and, unless you use Apple's "Hide My Email" feature, an email address. Apple may also share your name the first time you sign in, and Google shares your name and a link to your profile picture; these are kept with your account. If you sign in with Apple, Repex stores a token from Apple solely so it can revoke Repex's access to your Apple ID when you delete your account. Repex never sees or stores your password.

**What is uploaded when signed in.** Everything listed in Section 1 is copied to a private database hosted by Supabase (servers located in Ireland, EU):

- Your full workout history, including timestamps for individual sets
- Your splits and programmes
- Your app settings
- Your profile, including your name, profile photo, height and body-weight history
- Your gyms, their equipment lists, and gym photos
- If Apple Health is on: workouts brought in from Health, heart rate recorded during your Repex workouts, and body-weight readings (see Section 3)
- Feedback you give on Coach messages (see Section 5). Votes made before you sign in are uploaded when you do.

Photos are uploaded as part of your settings data. There is currently no way to back up your workouts without also backing up any photos you have added. If you do not want photos stored in the cloud, do not add them while backup is enabled.

**Who can read it.** Database access rules restrict every record to its owner. Only your signed-in account can read your data. I have administrative access to the database as its operator, but do not read individual users' training records except where strictly necessary to fix a fault you have reported.

**One aggregate use.** To decide which exercises to add to the built-in library, I periodically look at the exercise *names* in backed-up workouts and splits — in aggregate, as a ranked list of names with counts, not per person. This only covers accounts with backup turned on; nothing is read from a phone that has not signed in.

---

## 3. Apple Health (optional)

Apple Health is off until you switch it on in Settings and grant permission in Apple's own Health dialog. You can switch it off in Repex, or change the permissions in the Health app, at any time.

**What Repex reads from Health:**
- Your latest body weight, if it is newer than the one in your Repex profile. It is marked as coming from Health and is never counted in anything sent to the AI provider
- Heart rate (average and maximum) during workouts you logged in Repex
- Runs, rides, swims, rows and Pilates sessions that other apps saved to Health, which Repex adds to your history as completed sessions

**What Repex writes to Health:** each workout you finish in Repex, as a strength-training workout (or, for a mostly-Pilates session, a Pilates workout) with an estimate of the active energy used.

**Where it goes:** Health data stays on your phone. If you have signed in (Section 2), it is backed up with the rest of your training to your private database. It is **never sent to the AI provider** — workouts brought in from Health are left out of everything Coach reads — and it is never used for advertising or marketing, never sold, and never shared with anyone else.

---

## 4. AI features: Coach, plan import and kit versions

**Repex asks first.** Before any of its AI features sends anything, Repex shows a screen that names the provider (Anthropic, maker of Claude), lists what is sent and what is never sent, and asks you to allow it. If you choose "Not now", nothing is sent. Your answer is stored on your phone only.

**Coach is opt-in.** It does nothing until you switch it on, and it asks the question above when you do.

The three AI features are:
- **Coach** — short messages before, during and after workouts, and the "Coach's thoughts" read on Stats
- **Plan import** — when you paste a training plan as text, or add photos or screenshots of one, Repex sends that text or those images so it can be turned into a split
- **Kit versions** — when you ask for versions of an exercise that fit a gym's equipment, Repex sends the exercise name and that gym's equipment list (not the gym's name or photo)

Each request goes to Anthropic's API through a server I operate on Cloudflare.

**What Coach sends:**
- Exercise names (including any custom names you have typed)
- Weights, reps, estimated one-rep-max figures, and set counts
- Session dates, times and durations, day names, and rest times between sets
- How many times the app was sent to the background during a workout
- Distances, times, paces and heart-rate zones you type into cardio sets
- Calculated observations such as plateaus, trends, imbalances and weekly totals
- Your training style and, if you have set one, your race: its type, the name you gave it, its date, your goal time and, for Hyrox, your division (which says whether you race in a women's, men's or mixed category)
- Your language setting

**What is never sent:** your name, email, profile photo, gym names, gym photos, height, the average heart rate or power you type into cardio sets, any account identifier, or any data from Apple Health. Your body weight is never sent as a figure; note that volume totals for bodyweight exercises (such as pull-ups) include a body weight you typed in yourself — never one that came from Apple Health.

Each request is standalone. No conversation history is retained between messages.

**Technical details.** Requests pass through my server, which attaches a random per-installation identifier and your IP address only for the purpose of rate limiting. Both are hashed before being stored, are kept only for the rate-limit window (at most about a day), and are never forwarded to Anthropic. Cloudflare, as the hosting provider, records standard connection metadata. Anthropic processes the request under its commercial API terms: it does not use commercial API inputs to train its models, and keeps them only for a limited period, except where needed to investigate misuse.

**You can withdraw at any time.** Switching Coach off in Settings stops all transmission immediately and withdraws your answer, so Repex asks again before any AI feature sends anything.

---

## 5. Coach feedback

If you mark a Coach message as helpful or not helpful, Repex records that vote together with the message text and the data summary Coach was given when it wrote it. That summary contains your workout numbers.

This feedback is used solely to improve Coach's accuracy and usefulness. It is stored in the same private database and is readable by me as the operator. Feedback is not shared, sold, or published.

---

## 6. Sharing

If you share a workout, a recap or a split, that content is passed to whichever app you choose in the iOS share sheet. What happens to it after that is governed by that app and by whoever you send it to. Repex does not retain or transmit shared content itself.

Note that a shared split contains the exercise names and structure of that split in readable form, and a shared workout or recap image shows your first name if you have set one.

---

## 7. What Repex does not do

- No advertising, ad networks, or ad identifiers
- No analytics, crash reporting, or usage telemetry
- No location tracking
- No Apple Health data sent to the AI provider or anyone else, and none used for advertising or marketing
- No selling, renting, or sharing of your data with third parties for their own purposes
- No profiling for marketing

---

## 8. Data retention

Data on your device stays there until you delete it or delete the app.

Data in the cloud is kept while your account exists. You can delete your account and everything stored with it from the app: **You → Backup & help → Back up & sync → Delete account**. This removes your cloud data, including Coach feedback, at once. If you signed in with Apple, Repex also revokes its access to your Apple ID. You can also ask by emailing **repexadmin@gmail.com**, and I will action it within 30 days.

Coach feedback records are retained for the purpose of improving Coach and are deleted along with your account if you request deletion.

---

## 9. Your rights

If you are in the EU or UK, the GDPR gives you the right to access, correct, delete, restrict, object to, and receive a copy of your personal data. To get a copy of your data, email me and I will send it to you as a file.

To exercise any of these rights, email **repexadmin@gmail.com**.

The legal bases for processing are: performance of a contract (providing the app and its backup feature), your explicit consent (the AI features, Apple Health, and the body measurements you choose to enter, which you enable yourself and can withdraw at any time), and legitimate interests (keeping the service secure and functioning).

**International transfers.** Anthropic (USA) and Cloudflare process requests outside the EU under the European Commission's Standard Contractual Clauses.

You have the right to complain to your local data protection authority. In France, this is the CNIL (cnil.fr).

---

## 10. Children

Repex is not directed at children under 16 and should not be used by them. I do not knowingly collect data from children under 16. If you believe a child has provided data, email me and it will be deleted.

---

## 11. Data processors

The following services process data on my behalf:

- **Supabase** — database and authentication (EU, Ireland)
- **Cloudflare** — the server that relays requests to Anthropic
- **Anthropic** — Claude, which writes Coach's messages, reads imported plans and suggests kit versions
- **Apple** — app distribution, and sign-in if you use it
- **Google** — sign-in only, if you use it

---

## 12. Security

Data in transit is encrypted. Database access is restricted per user. API credentials are held on the server, never inside the app. No system is perfectly secure, and I cannot guarantee absolute security, but I take reasonable measures appropriate to the scale of the service.

---

## 13. Changes

If this policy changes materially, the app will make the change apparent. The "last updated" date above always reflects the current version.

---

## 14. Contact

Ryan Bleecke
France
**repexadmin@gmail.com**
