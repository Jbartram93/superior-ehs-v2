# Superior EHS — Leadership Foundation Dashboard

The EHS command center for Superior Huntingdon Composites (Vanceburg KY). Three role-based views over one data layer — the pattern: status is **computed from data**, never hand-maintained.

## The Three Views

| Tab | Audience | Shows |
|---|---|---|
| **My Day** | Justin | Today's focus, priorities, corrective actions with auto AT RISK badges, Pause & Think quote |
| **Greg** | The 45-second check-in | Focus / Question / Observation brief + initiative status |
| **Board** | Leadership | TRIR vs benchmark, recordables, hand/finger share, tenure risk, 60-day roadmap, the two-problem story |

## The AT RISK Engine

Corrective actions are dates, not text. The dashboard computes:
- `days = due_date − today`
- Overdue → red **AT RISK · Nd overdue** badge
- Due within 3 days → amber **DUE** badge
- Clean → green

Nothing to remember. The dashboard remembers for you.

## How To Use

**Edit data only** — everything lives in one `DATA` object at the top of `index.html`:

```js
const DATA = {
  focus: "One sentence. What you're driving.",
  priorities: [{t:"task", done:false}],
  correctiveActions: [{t:"action", due:"2026-11-15", status:"open"}],
  greg: { focus:"...", question:"...", observation:"..." },
  ...
}
```

Change `DATA`, commit, push — live in ~1 minute.

## Deploy

GitHub Pages from `main` root. URL: `https://jbartram93.github.io/superior-ehs-dashboard/`

Add to phone: Safari → share → Add to Home Screen.

## Roadmap

- [ ] Wire corrective actions from the Corrective_Action_Tracker.xlsx (real due dates)
- [ ] TRIR auto-calc when Jodi's hours arrive
- [ ] Huntingdon PA second site view
- [ ] Weekly auto-drafted status (the video pattern)

---
Built by Justin Bartram — EHS Manager. Day counter starts 2026-10-27.
