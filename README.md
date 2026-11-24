# SchoolOS

Static, single-file prototypes of a mission-based classroom system, presented as a demo school called **Schoolynq School**. Open `index.html` to reach everything. All students, guardians, staff and data are invented.

| File | What it is |
|---|---|
| `index.html` | Hub page linking every dashboard and mission |
| `teacher-dash-arrows-calendar.html` | Mission Control teacher dashboard (class arrows and calendar) |
| `teacher-dash-planner-above-crease.html` | Mission Control teacher dashboard, planner above the fold |
| `teacher-dash-acolyte.html` | Earlier Acolyte teacher dashboard |
| `principal-dash.html` | Principal dashboard |
| `lesson-planner.html` | Adaptive lesson planner mock-up: re-plans a class’s remaining lessons around pace and calendar changes, inside fixed school rules (mock whole-school data) |
| `student-analysis.html` | Student analysis mock-up for the whole school: 192 students in 8 sections (Grades 3–8) and the 9 classes from the lesson planner, combining ten mock sources (missions, exit tickets, homework, block assessments, attendance, baseline test, behaviour log, wellbeing check-ins, school records, teacher notes). School view for the principal, class view with mastery by lesson, and a full student profile; flags say which sources they come from. Links: `student-analysis.html#school`, `#class-8A-sci`, `#SQ-5A-21` |
| `presenter.html` | Presenter: a 12-slide Schoolynq product tour. Slides are images in `slides/` (1920×1080 WebP, thumbnails in `slides/thumbs/`); buttons on each slide open that part of the demo. Setup panel: tick slides, set seconds per slide, reorder (arrows or drag), presets (full tour, teachers, school leaders, two-minute), autoplay and loop. While presenting, a thin blue bar shows when autoplay moves on; Space pauses, arrows or a clicker move. “Present with laptop screen” opens a notes window (talking points, next slide, timer, controls) and keeps it in step with the TV window. **Your own presentations:** “New presentation”, then add slide images (PNG, JPEG, WebP or GIF; big ones are scaled to 1920×1080); set titles, seconds, order, on/off, talking points, up to 6 link buttons and the corner they sit in. They are saved in that browser (IndexedDB); Export writes one `.schoolynq-presentation.json` file with the images, and Import opens it on another computer (imports are checked: images only, safe links only) |
| `brand/` | Schoolynq logo, mark and Nunito font (from schoolynq.com), and `brand.css`, which every page loads for the brand font, colours and logo tile |
| `missions/heart-v4/` | Schoolynq Stage 6 Heart Mission v4: `index.html` (the lesson), `mission.json`, `teacher-guide.html` |
| `missions/blood/` | Grade 5 Science “Operation Blood Flow” (mission 2.7.2-blood-lab) built into the Schoolynq player v2.9.2, the same player as schoolynq.com/demo/breathing/; `teacher-guide.pdf` is extracted from the mission |
| `missions/*/printables/` | Print-ready A4 PDFs for each mission: pupil notes, worksheet (with square-grid and ruled answer space, a sample QR code and an answer key), teacher guide and resource list. The same PDFs are embedded in each mission's resource list. The Teacher dashboard's Resources page links them |

The dashboard files were previously named without an `.html` extension (`newteacherdashwitharrowsandcalender`, `teacherdashcalenderplannerabovecrease`, `teacher dash`, `principal dash`). They were renamed so browsers and web hosts display them as pages.

## Launching the Heart mission

In either Mission Control dashboard, **Start Today**, **Start Mission** and **Launch Mission** for “Mission 4: The Heart” open the mission in its own window. **Teacher Notes** opens its guide. In the same dashboards, **Class 55: Blood Vessels** (the class arrow or the Mission Grid **View** button) opens its mission page, where **Launch Mission** starts the Blood lesson and **Teacher Guide** opens its PDF. Missions that are not built yet show a short message instead.

For two screens, choose **Start with teacher screen** on the mission’s opening page. The mission opens a separate teacher window (live mirror of the projector, its controls, talking points, run-sheet, class scores and a mock-up help chat). Drag the mission window to the projector and press F11 there. Chrome may ask you to allow pop-ups the first time.

## Hosting

Everything is static: no build step, no server code, no network calls. Any static host works:

- **GitHub Pages:** repository Settings → Pages → Deploy from a branch → `main` / root. The site is then at `https://drdewan.github.io/schoolOS/`.
- **Vercel or Netlify:** import the repository with no build command and the root as the output folder.

Open the pages directly, not inside an embedding frame (Google Sites, LMS pages): those frames block the teacher-screen pop-up and file downloads.
