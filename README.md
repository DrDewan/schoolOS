# SchoolOS

Static, single-file prototypes of a mission-based classroom system. Open `index.html` to reach everything.

| File | What it is |
|---|---|
| `index.html` | Hub page linking every dashboard and mission |
| `teacher-dash-arrows-calendar.html` | Mission Control teacher dashboard (class arrows and calendar) |
| `teacher-dash-planner-above-crease.html` | Mission Control teacher dashboard, planner above the fold |
| `teacher-dash-acolyte.html` | Earlier Acolyte teacher dashboard |
| `principal-dash.html` | Principal dashboard |
| `missions/heart-v4/` | Schoolynq Stage 6 Heart Mission v4: `index.html` (the lesson), `mission.json`, `teacher-guide.html` |

The dashboard files were previously named without an `.html` extension (`newteacherdashwitharrowsandcalender`, `teacherdashcalenderplannerabovecrease`, `teacher dash`, `principal dash`). They were renamed so browsers and web hosts display them as pages.

## Launching the Heart mission

In either Mission Control dashboard, **Start Today**, **Start Mission** and **Launch Mission** for “Mission 4: The Heart” open the mission in its own window. **Teacher Notes** opens its guide. Missions that are not built yet show a short message instead.

For two screens, choose **Start with teacher screen** on the mission’s opening page. The mission opens a separate teacher window (live mirror of the projector, its controls, talking points, run-sheet, class scores and a mock-up help chat). Drag the mission window to the projector and press F11 there. Chrome may ask you to allow pop-ups the first time.

## Hosting

Everything is static: no build step, no server code, no network calls. Any static host works:

- **GitHub Pages:** repository Settings → Pages → Deploy from a branch → `main` / root. The site is then at `https://drdewan.github.io/schoolOS/`.
- **Vercel or Netlify:** import the repository with no build command and the root as the output folder.

Open the pages directly, not inside an embedding frame (Google Sites, LMS pages): those frames block the teacher-screen pop-up and file downloads.
