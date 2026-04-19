# NayanVaani

*5 lakh people in India cannot speak. Now they can.*

**[Visit the Landing Page](https://nayan-vaani.netlify.app/)** | Play Store (Coming Soon) | App Store (Coming Soon)

## The Problem
Over 5 lakh people in India live with conditions like cerebral palsy, ALS, and locked-in syndrome. They are fully intelligent, fully aware, fully conscious — but completely trapped inside their bodies. They cannot speak. They cannot move their hands. Every thought, every need, every emotion dies inside them because there is no bridge between their mind and the world.

The only device that gives them a voice is called an AAC (Augmentative and Alternative Communication) device. It costs ₹8 to ₹12 lakh. That is more than most Indian families earn in five years. So these people stay silent. Forever.

## What We Built
NayanVaani is a free Android app that lets non-verbal people communicate using only their eyes. No special hardware. No expensive equipment. Just any normal Android smartphone.

The user looks at a letter or phrase on the screen. After 1.5 seconds of looking at it — it selects. The app speaks it aloud in Hindi and English. That's it. That's the entire interaction. Eyes in, voice out.

## How It Works
* **Eye Tracking** — The front camera of the phone watches the user's eyes in real time using MediaPipe, a computer vision technology built by Google. It tracks the exact position of the iris — where the eye is pointing on the screen — 30 times per second. No special infrared camera needed. Works in normal indoor lighting. Works with glasses.
* **Calibration** — The first time a user opens the app, they do a 15-second calibration. Five dots appear on screen one by one. The user looks at each dot. The app learns that specific person's eye shape, head position, and phone angle. After calibration, accuracy goes from 70% to 94%.
* **Dwell Selection** — The user looks at a phrase or letter. A circular progress indicator fills up over 1.5 seconds. When it completes, the item is selected. This is called dwell-based selection — no clicking, no tapping, no physical movement required.
* **Communication Grid** — The screen shows a grid of phrases and letters. Quick phrases cover the most common daily needs: "I am in pain", "I am hungry", "I need water", "Call my family", "I love you". There is also a full alphabet keyboard for spelling anything. As letters are typed, word predictions appear so full words can be selected in one look instead of letter by letter.
* **Voice Output** — When something is selected, the app speaks it aloud in a natural Indian English and Hindi voice. Families who have recordings of the patient's old voice can even upload it — the app will approximate speaking in their own voice.
* **Emotion Detection** — The camera passively reads the user's facial expression using AI. If the user looks distressed, the app automatically surfaces pain and emergency phrases at the top. If they look happy, it shows greeting and positive phrases. The app responds to how the person is feeling before they even communicate it.
* **Works Offline** — Every critical feature — eye tracking, letter selection, voice output — runs entirely on the phone. No internet required. This works in rural India, in hospitals, in homes with no WiFi.

## The Tech Stack
* **React Native Expo** — cross-platform mobile app
* **MediaPipe (Google)** — real-time iris and face landmark tracking
* **Python FastAPI** — backend serving the gaze detection model
* **DeepFace / AWS Rekognition** — emotion detection from facial expressions
* **Supabase** — user profiles, custom phrase packs, authentication
* **Android Text-to-Speech** — Hindi and English voice output

## Who It's For
* People with cerebral palsy
* ALS patients (motor neurone disease)
* Locked-in syndrome survivors
* Stroke patients with speech and motor loss
* Anyone who is intelligent but cannot speak or move their hands

## Why It's Different
| Feature | Existing AAC Devices | NayanVaani |
| :--- | :--- | :--- |
| **Cost** | ₹8–12 lakh | **Free** |
| **Hardware** | Proprietary IR camera | **Any Android phone** |
| **Language** | English only | **Hindi + English** |
| **Setup** | Days with a specialist | **15 seconds** |
| **Available in India** | Barely | **Immediately** |

## The Impact
5 lakh people in India have never been able to tell their family they are in pain. They have never been able to say I love you. They have never been able to ask for a glass of water.

NayanVaani costs nothing. It runs on the phone already in every Indian home. It speaks in the languages Indians actually speak. And it is available today.

We didn't invent eye tracking. We made it free. We made it Indian. We made it available to the people who need it most.

---

## Future Features (Phase 2 & Beyond)

### Advanced Communication Features
* **Predictive AI Brain** — Over time the app learns each individual user's most common phrases, their daily routine, their personality. It starts predicting what they want to say before they finish spelling it. A user who always says "good morning" at 8am gets that phrase surfaced automatically.
* **Custom Voice Cloning** — If the family has even 10 minutes of recordings of the patient speaking before their condition progressed, the app rebuilds their voice. They speak again in their own voice. Not a robot. Them.
* **Multi-language Support** — Tamil, Bengali, Marathi, Gujarati, Telugu. Every major Indian language. A patient in Chennai communicates in Tamil. A patient in Kolkata in Bengali. Right now no AAC device in the world does this for Indian languages.
* **Symbol-Based Communication** — For users with cognitive impairments alongside physical ones, replace text with picture symbols. Look at a picture of food, the app says "I am hungry." Works for children with cerebral palsy who cannot read yet.
* **Smart Phrase Learning** — The app tracks which phrases each user selects most and automatically reorganizes the grid to put their most-used phrases closest to the center where eye movement is easiest. The interface becomes personal over time.

### Caregiver & Family Features
* **Caregiver Companion App** — A separate app for family members and caregivers. When the patient is trying to communicate, the caregiver gets a notification on their phone even from another room. The caregiver sees exactly what the patient is trying to say in real time.
* **Emergency SOS** — Patient looks at the emergency phrase for 3 seconds. It sends an automatic SMS with their location to three saved family numbers. No caregiver needs to be present.
* **Communication History Log** — Everything the patient communicated is saved with timestamps. Doctors can review what the patient reported feeling over the past week. Caregivers can see patterns — the patient consistently signals pain every evening, which leads to a diagnosis change.
* **Mood Tracking Dashboard** — The emotion detection data builds a daily mood log. Family and doctors see a graph of emotional states over time. Mental health of non-verbal patients is chronically ignored — this makes it visible.

### Medical & Clinical Features
* **Hospital Integration** — Pre-loaded medical phrase packs. Pain scale 1 to 10. Body part selector. Symptom descriptions. A non-verbal patient in an ICU can communicate with doctors without a specialist present.
* **Eye Health Monitoring** — The app already tracks eye movement constantly. With small additions it can detect early signs of eye muscle fatigue and degeneration — important for ALS patients whose condition progressively affects eye control. Alerts the medical team before communication ability is lost.
* **Neuro-adaptive Interface** — For patients with progressive conditions, as their eye control weakens, the app automatically simplifies — bigger targets, slower dwell times, fewer options. The interface degrades gracefully as the condition advances.

## Business Model

**Core Principle:** The basic app is and always will be free. A non-verbal person in rural Bihar cannot pay a subscription. Monetization happens everywhere except the patient.

* **Revenue Stream 1 — Hospital & Clinic Licensing (Primary):** Hospitals pay a monthly institutional license to deploy NayanVaani across their neurology, ICU, and rehabilitation wards. Every government and private hospital with a neurology department is a customer. Pricing: ₹5,000–₹25,000 per month per hospital depending on size. India has over 50,000 hospitals. Even 500 hospitals at ₹10,000/month = ₹5 crore/month.
* **Revenue Stream 2 — NGO & Government Partnerships:** NITI Aayog, state disability welfare departments, and NGOs working with disabled communities pay for bulk deployment and support contracts. Government's ADIP scheme already funds assistive devices for disabled citizens — NayanVaani becomes an approved device under this scheme. This is a direct replacement for the ₹10 lakh device the government was already paying for.
* **Revenue Stream 3 — Premium Family Plan:** Free tier covers everything essential. Premium plan at ₹299/month adds: custom voice cloning, unlimited phrase packs in all Indian languages, caregiver companion app, communication history export, priority support. Target: families of patients who can afford a small monthly cost to get deeper features.
* **Revenue Stream 4 — Medical Data Insights (Anonymized):** Aggregated, anonymized communication and emotion data from consenting users is genuinely valuable to pharmaceutical companies running ALS and cerebral palsy drug trials, to medical researchers studying non-verbal communication patterns, and to hospitals building better care protocols. This is opt-in only. Patients and families explicitly consent.
* **Revenue Stream 5 — White-label Licensing:** Other countries have the same problem. 450,000 non-verbal people in the US. Millions across Southeast Asia. License the technology to international healthcare companies and NGOs who adapt it for their local languages and markets. NayanVaani becomes the underlying engine.
* **Revenue Stream 6 — Adjacent Markets:** Judicial services exam viva prep — the same architecture (speech input + AI evaluation) works for law and civil services exam preparation. Vaad AI is already building this. The gaze and voice infrastructure transfers directly. Same tech, completely different market, massively larger user base.

## Growth Roadmap
* **Month 1–3 (Validation)** — Deploy in 3 hospitals in Delhi NCR for free. Get 50 patients using it. Collect feedback. Prove the core loop works in real clinical conditions.
* **Month 3–6 (Revenue)** — Sign first 10 hospital contracts. Launch premium family plan. Apply for ADIP scheme approval from Ministry of Social Justice.
* **Month 6–12 (Scale)** — 100 hospitals across India. Partner with Asha workers and district disability welfare offices for rural deployment. Launch Tamil and Bengali language packs.
* **Year 2 (Expansion)** — International licensing to Southeast Asia and Middle East. Launch caregiver app. Begin medical data partnership with one pharma company. Target 10,000 active patients.
* **Year 3 (Platform)** — NayanVaani becomes a platform. Third-party developers build phrase packs, language packs, medical specialty modules on top of it. App store model for AAC content. First AAC ecosystem built for Indian languages.

## Market Size
* 5 lakh+ non-verbal people in India — direct users
* 50,000+ hospitals — institutional customers
* 26 million people with disabilities in India — broader addressable market
* Global AAC market — $450 million and growing at 8% annually
* Indian assistive technology market — severely underserved, government-backed, first-mover advantage available right now
