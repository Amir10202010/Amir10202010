Hi, I'm Amirkhan. Full-stack dev from Astana.

Mostly Next.js, TypeScript and Postgres. Sometimes Go, Python, or C++ on an ESP32.
Working on [Velnox](https://www.usevelnox.com) right now. It sorts your Gmail by which clients need a reply today.

```console
$ git log --reverse --oneline

2024-09  kahoot-bot      Kahoot-style quiz bot for my class in Telegram
2024-09  dz-bot          homework bot for the class chat
2024-10  wb-parser-bot   pulls a Wildberries seller's catalogue into Excel
2025-07  pharma-store    Go + Postgres API for an online pharmacy
2026-04  Dentist-Ai      YOLO model trained on dental X-rays
2026-04  VideoMaker-Ai   makes short videos with subtitles from a topic
2026-05  bekinged        online checkers with a bot and ELO
2026-06  velnox          Gmail assistant, my main project
2026-09  DuelBattle      1v1 webcam game over WebRTC
2026-09  campusproof     LOCUS Startup Hackathon
2026-10  egiz            NASA Space Apps Challenge 2026
2026-10  neuromove       team project: web app, ESP32 firmware, hardware
```

| | | |
|---|---|---|
| [**velnox**](https://github.com/Amir10202010/velnox)<br/><sub>Next.js, Prisma, Supabase, Gemini</sub><br/><sub>[usevelnox.com](https://www.usevelnox.com)</sub> | [**bekinged**](https://github.com/Amir10202010/bekinged)<br/><sub>Next.js, Socket.IO, Postgres</sub><br/><sub>[bekinged.vercel.app](https://bekinged.vercel.app)</sub> | [**egiz**](https://github.com/Amir10202010/nasa-space-app-2026)<br/><sub>NASA Space Apps 2026</sub><br/><sub>[egiz.vercel.app](https://egiz.vercel.app)</sub> |
| [**neuromove**](https://github.com/Amir10202010/neuromove)<br/><sub>web, ESP32, hardware</sub><br/><sub>[neuromove-nine.vercel.app](https://neuromove-nine.vercel.app)</sub> | [**pharma-store**](https://github.com/Amir10202010/pharma-store)<br/><sub>Go, Gin, GORM, Postgres</sub> | [**Dentist-Ai**](https://github.com/Amir10202010/Dentist-Ai)<br/><sub>Python, Flask, Ultralytics</sub> |

### Some things in Velnox I can talk about

- Background jobs (sync, AI analysis, sending mail) are just rows in Postgres, picked up with `SELECT ... FOR UPDATE SKIP LOCKED`. If Gemini rate-limits, the job retries later.
- Gmail sync uses `users.watch` and Pub/Sub, then pulls only the changes since the last `historyId`.
- Search combines a normal SQL keyword match with embedding similarity.
- The AI can suggest an action, but my own code runs it after you click confirm. It can't send mail by itself.

---

<sub>Astana, Kazakhstan · looking for full-stack work ·
<a href="mailto:sagindiktar@gmail.com">sagindiktar@gmail.com</a> ·
<a href="https://t.me/Idk_Amir">telegram</a> ·
<a href="https://www.linkedin.com/in/amirkhan-sagyndyk-36760a368/">linkedin</a></sub>
