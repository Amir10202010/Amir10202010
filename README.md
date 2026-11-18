## Amirkhan Sagyndyk

**Full-stack developer — Next.js and TypeScript on the front, Postgres and background workers behind it.**
Astana, Kazakhstan · open to full-stack roles.

I ship whole products rather than screens: auth, database, sync, queues, deploy. The projects
below are live, not slide decks — you can open them, sign in and click around.

Most of what I build starts from something that annoyed me or someone near me: a client email
buried under newsletters, a homework chat nobody could keep up with, a loyalty card that gives
you a stamp and nothing else.

### Selected projects

| | What it is | Built with |
|---|---|---|
| **[Velnox](https://github.com/Amir10202010/velnox)** · [usevelnox.com](https://www.usevelnox.com) | An AI layer over your own Gmail: explainable triage, risk alerts, review-before-send drafts, and a knowledge graph that builds itself from mail, calendar and notes | Next.js · TypeScript · Prisma · Supabase · Gemini |
| **[BEKINGED](https://github.com/Amir10202010/bekinged)** · [live](https://bekinged.vercel.app) | Checkers as a daily competitive habit — a rules engine, a minimax AI opponent with alpha-beta pruning, and realtime multiplayer on a separate Socket.IO server | Next.js · Socket.IO · Prisma · Postgres |
| **[pharma-store](https://github.com/Amir10202010/pharma-store)** | REST API for an online pharmacy — JWT auth, prescription-flagged catalogue, cart, orders and checkout across nine feature slices | Go · Gin · GORM · Postgres |
| **[ImpactLab](https://github.com/Amir10202010/ImpactLab)** · [live](https://impact-lab-blue.vercel.app) | Site for a youth initiative running healthcare hackathons for students in Kazakhstan | Next.js · Tailwind · Motion |
| **[Dentist-Ai](https://github.com/Amir10202010/Dentist-Ai)** | Dental X-ray analysis — a custom-trained YOLO model returns one annotated image per finding | Python · Flask · Ultralytics |
| **[VideoMaker-Ai](https://github.com/Amir10202010/VideoMaker-Ai)** | A topic goes in, a finished short video comes out: script, voice, word-level subtitles, burned in by FFmpeg | Python · Gemini · Whisper · FFmpeg |

### Engineering I'm glad to be asked about

Most of these live in [Velnox](https://github.com/Amir10202010/velnox), the project I've put the most into:

- **Slow work never blocks a request.** Sync, AI analysis, embeddings and outbound email are rows
  in a Postgres job queue, claimed atomically with `SELECT … FOR UPDATE SKIP LOCKED` and drained
  by either a standalone worker or a cron endpoint. Rate-limit errors come back classified as
  retryable, so the queue's backoff *is* the pacing strategy.
- **The AI layer is an interface, not an SDK call.** Business logic never imports a vendor SDK, so
  a deterministic keyword provider can stand in when there's no API key — and the UI labels those
  results as offline instead of passing them off as real analysis.
- **Incremental sync, not polling.** Gmail `users.watch` → Pub/Sub → webhook → `historyId` delta
  sync, with a bounded full-sync fallback for when history expires.
- **Search that blends two rankings.** Keyword SQL candidates unioned with semantic cosine over
  conversation embeddings, then scored together — with the ranking math pulled out as pure,
  testable functions.
- **The model stays outside the trust boundary.** The assistant only *proposes* an action;
  deterministic, user-scoped code executes it after an explicit confirm, and none of it can send mail.

### Stack

**Daily:** TypeScript · Next.js · React · Node · Postgres · Prisma · Tailwind
**Comfortable in:** Python (Flask, aiogram) · Go (Gin, GORM) · Supabase · Socket.IO · Docker-less Vercel deploys
**Have shipped with:** Gemini · Whisper · YOLO / Ultralytics · Google APIs (Gmail, Calendar, Books) · Arduino / C++

### Beyond the editor

I built the site for **ImpactLab** — healthcare hackathons, webinars and trainings that bring
students, developers and doctors together in Astana.

### Reach me

- **sagindiktar@gmail.com**
- Telegram — [@Idk_Amir](https://t.me/Idk_Amir)
- [LinkedIn](https://www.linkedin.com/in/amirkhan-sagyndyk-36760a368/)
