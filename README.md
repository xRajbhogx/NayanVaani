# NayanVaani

**Won 1st place at HackDUCS (Delhi University).** Built in 36 hours. See the app and certificate: [LinkedIn Post](https://www.linkedin.com/posts/pushkarshukla0_first-hackathon-top-8-second-hackathon-activity-7454614214268088320-Rrtb?utm_source=share&utm_medium=member_android&rcm=ACoAAELhGXkBJ2CN4tZx-0uarVgTpK6UeCgMc4w)

Play Store · Coming Soon
<img width="4096" height="1820" alt="IMG_20260426_174015 jpg" src="https://github.com/user-attachments/assets/03061a2a-8e8d-458c-b54f-bcf46c64d8bb" />

---

Over 5 lakh people in India have conditions like ALS, cerebral palsy, or locked-in syndrome. They're fully aware, fully intelligent, completely trapped. The AAC devices that give them a voice cost ₹8 to ₹12 lakh. Most families never afford one.

NayanVaani is a free Android app that lets non-verbal people communicate using only their eyes and any normal smartphone.

## What it does

The user looks at a phrase or letter on screen. After 1.5 seconds, it selects and speaks aloud. That's the entire interaction... eyes in, voice out.

A 15-second calibration on first launch (look at 5 dots) takes accuracy from ~70% to 94% for that specific person's eye shape and head position. The communication grid has quick phrases for daily needs plus a full alphabet keyboard with word prediction. Everything - eye tracking, selection, voice output — runs offline. No internet needed. This matters for rural India, hospitals, homes without WiFi.

The camera also passively reads facial expressions. If the user looks distressed, pain and emergency phrases surface automatically before they've even started communicating.

## Stack

React Native + Expo + TypeScript for the UI. Kotlin + MediaPipe for the eye tracking, running as a native Android module. Supabase for auth and user data. Claude API for AI features. Android TTS for voice output.

The architecture is clean: Kotlin owns all sensing and fires gaze events to the JS layer. React Native owns everything else. This keeps the two codebases independent and the bridge minimal.

## Getting started

You'll need Node 18+, Android Studio, Expo CLI, and a physical Android device (eye tracking requires a real camera, won't work on emulator).

```bash
git clone https://github.com/yourusername/nayanvaani.git
cd nayanvaani
npm install
npx eas build --profile development --platform android
```

Create a `.env` file:

```
EXPO_PUBLIC_SUPABASE_URL=your_supabase_url
EXPO_PUBLIC_SUPABASE_ANON_KEY=your_supabase_anon_key
ANTHROPIC_API_KEY=your_claude_api_key
```

Then `npx expo start` and open on device using the dev build, not Expo Go (custom native modules require a dev build).

## Project structure

```
nayanvaani/
├── app/                  # Expo Router screens
├── components/           # UI components
├── modules/
│   └── eye-tracking/     # Kotlin native module (MediaPipe)
├── lib/
│   ├── supabase.ts
│   └── ai.ts
└── android/              # Native Android project
```

## What's next

Smart home control is the big one — lights, fans, AC via Alexa and Matter protocol. After that, eye-controlled reel scrolling (a paralyzed person independently scrolling Shorts with just their eyes is the feature that makes this go viral). Multi-language support for Tamil, Bengali, Marathi. Caregiver companion app. Emergency SOS via gaze hold.

The core app is and will stay free. Monetization happens through hospital licensing and an optional premium family plan, never from patients.

## Why it's different

Most AAC devices require proprietary infrared cameras, cost lakhs, are English-only, and take days to set up with a specialist. NayanVaani runs on any mid-range Android, is free, supports Hindi and English, and takes 15 seconds to set up.

## Contributing

Open an issue or reach out directly. Especially interested in help from anyone working in AAC, speech-language pathology, or assistive tech.

## License

MIT. A non-verbal person in rural Bihar should never have to pay to speak.

Built by [Pushkar Shukla](https://github.com/yourusername) · B.Tech CSE, IP University Delhi · [your@email.com]
