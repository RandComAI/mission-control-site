# The screenshots the landing page expects

Drop a file in here with the right name and it appears on the page. Nothing else
has to be edited — the frame shows its placeholder until the image actually
loads, so a name that is missing or misspelled shows the placeholder rather than
a broken icon.

All six are **real captures of the current v2 app** (1920 × 1200), taken by
driving the live UI with Playwright against a throwaway company — no concept
art. Re-capture with Playwright when the UI changes materially; keep the
filenames so the pages need no edits.

The current set is one **live demo project** ("Build a tiny personal
reading-list website") run entirely by a Kimi coordinator and Kimi helpers, so
every screen shows real working state — working pills, live helper dots,
populated agent map, a running session — rather than empty placeholders.

| File | The screen it shows | Size |
|---|---|---|
| `task-tree-preview.png` | Project workspace (light): the request receipt, the coordinator's plan of two focused tasks both Working, with helper rows live | 1920 × 1200 |
| `workspace-overview.png` | The same live project workspace in dark mode | 1920 × 1200 |
| `outcome-preview.png` | A task's detail: the AGENT MAP (Coordinator → Designer, Running), state, and the outcome section | 1920 × 1200 |
| `org-chart.png` | The My projects grid: every project card with live state | 1920 × 1200 |
| `role-picker.png` | An agent's session panel: attach/stop, steer it, or switch its AI tool — shown running on Kimi | 1920 × 1200 |
| `role-library.png` | The helper library: reusable roles from Coordinator to Security Reviewer | 1920 × 1200 |

The frames scale the image to their own width, so anything close enough is fine.

PNG is what the page asks for. For another format, change the one `src` on that
frame in `../index.html`.

After dropping files in here, run `make package` from `app/` to refresh
`dist/index.html` and `dist/screenshots/`, which is the copy to look at — its
download link points at the archive sitting beside it.
