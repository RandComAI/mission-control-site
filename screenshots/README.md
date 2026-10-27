# The screenshots the landing page expects

Drop a file in here with the right name and it appears on the page. Nothing else
has to be edited — the frame shows its placeholder until the image actually
loads, so a name that is missing or misspelled shows the placeholder rather than
a broken icon.

All six are **real captures of the current v2 app** (1920 x 1200), taken by
driving the live UI with Playwright (light theme unless noted, captured at 2x
and scaled to 1920 wide) against a clean demo home: two delivered projects, the
English "Plan a 3-day Tokyo trip for a family" and the Chinese "记账小网页". No
concept art. Re-capture when the UI changes materially; keep the filenames so
the pages need no edits.

**Retaken 2026-10-24 from build ce940ed3** (the English set from the English UI
on the Tokyo project). Replaces the stale 10-13 set, which predated the task
page, "Add files" and "Open coordinator in Terminal". Two cosmetic touches
before each capture: the machine-specific project folder path and internal
session ids were replaced in the page text (folder shows as
`~/RandComp Studio/Projects`). Nothing else is edited.

| File | The screen it shows | Size |
|---|---|---|
| `task-tree-preview.png` | Project workspace (light), scrolled to the lower half: chat with the coordinator, the project flow and the project plan with its delivered task | 1920 x 1200 |
| `workspace-overview.png` | The project workspace top in dark mode: Now strip, who is doing what, just happened, folder and report button | 1920 x 1200 |
| `outcome-preview.png` | A task page: the helper chips (Coordinator, QA, Technical Writer, Add a helper), what the task produced (documents, code and logs), and how it went | 1920 x 1200 |
| `org-chart.png` | The My projects home with the Delivered group open: both project cards | 1920 x 1200 |
| `role-picker.png` | A helper's full session panel (QA's conversation) open over the task page. The old shot showed switching an agent's AI tool; that panel is now a conversation view, so this is the closest equivalent | 1920 x 1200 |
| `role-library.png` | The role library: Architect through Technical Writer | 1920 x 1200 |

The frames scale the image to their own width, so anything close enough is fine.

PNG is what the page asks for. For another format, change the one `src` on that
frame in `../index.html`.

After dropping files in here, run `make package` from `app/` to refresh
`dist/index.html` and `dist/screenshots/`, which is the copy to look at — its
download link points at the archive sitting beside it.

## Chinese set (`zh/`)

Same six names plus `hero-poster.png` (1440 x 900), retaken 2026-10-24 from
build ce940ed3 with a Playwright browser at locale `zh-CN`, so the UI chrome is
Chinese, on the 记账小网页 project (the project folder path and ids masked as
above). The task page and session panel shots show the Developer helper; the
role library and the home also list the English Tokyo project, which is user
data. `hero-poster.png` is the project top (Now strip, who is doing what).
The older `capture_zh_screenshots.mjs` targeted the founder's real company and
the old UI; it is not what produced this set.
The zh page should point at `../screenshots/zh/<name>.png`.

## The hero picture and the "Three ways" plan crop (2026-10-26)

| File | What it shows | Size |
|---|---|---|
| `project-diagram.png` | Hero picture. The project page on the Tasks tab: the whole task diagram of a demo project, "Reading-list website" (3 of 7 tasks done, 2 in progress, 2 not started), up to the bottom of the diagram card. Light theme, 1440 x 1341 CSS px at 2x, scaled to 2160 wide | 2160 x 2011 |
| `project-plan.png` | The Plan overlay opened from its "Plan · 7" button, cropped with the button, for the app card in "Three ways to use it" | 760 x 641 |
| `zh/project-diagram.png`, `zh/project-plan.png` | The same two from the Chinese UI (locale `zh-CN`) on the Chinese twin project, 阅读清单小网站 | same |

Captured from the tree built tonight from HEAD (`/private/tmp/mc-build/app`,
served bundle `mission_control/web/assets/v2-CzXvePrM.js`, which has the
Tasks / Agents tabs and `workspace.planButton`) — not from the main checkout,
whose compiled `mission_control/web` is from 2026-10-24 and still shows the
older Steps / Helpers layout. Run with `python -m mission_control ui
--no-model` against a private, throwaway `MISSION_CONTROL_HOME` and
`--company`, seeded straight through `ProjectV2Repository`; no agent session
was started. The two working tasks carry a helper role but no agent id, so the
page shows the plain "Working" word instead of asking a session that does not
exist. Nothing in the pictures is edited.
