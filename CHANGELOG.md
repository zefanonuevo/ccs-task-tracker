# CCS Task Tracker: change log

Every version of CCS Task Tracker, newest first, from the first sketch (0.9.0) to the current version. The same history is in the app: sign in, or use **See the full version history** on the sign-in screen, then open the **Versions** tab.

Numbering: **Major** (3.0) means how people work changes; **Minor** (2.1) means new features that leave existing steps alone; **Patch** (2.1.1) means fixes only. Status is Concept, Prototype, Pilot or Released.

## Where each version came from

| Version | Date | Source |
|---|---|---|
| 0.9.0 to 1.0.0 | 6 Oct 2026 | Written in claude.ai as the CCS Task Tracker artifact. No earlier copy was kept, so only this log records them. |
| 2.0.0 to 2.4.0 | 13 Oct 2026 | The same claude.ai artifact, updated in place. Copied into GitHub on 14 Oct at 23:49 as one commit (575ed48), so the steps between 2.0 and 2.4 are described here, not in commits. |
| Design proposal | 14 Oct 2026 | The claude.ai artifact Task Tracker Preview: a specimen sheet for the macOS look, with the motion values and colors that 2.5.0 adopted. |
| 2.5.0 | 15 Oct 2026 | GitHub. Ten commits, listed below. |
| 2.6.0 | 15 Oct 2026 | GitHub. This version history change. |
| 2.7.0 | 18 Oct 2026 | GitHub. CCS Portal colors. |

# Versions

## 2.7.0 (18 Oct 2026, Prototype, current)

The colors now match the CCS Portal website. Every feature works as before.

### Changed

- Light and dark colors follow the portal palette: Ink, Forest, Mint, Paper and Amber. Text, lines and surfaces are slightly different shades; the green accent is unchanged.
- The header version tag now reads v2.7.

### Fixed

- The favicon was still blue and is now the portal green.

### Known limits

- The status and heatmap colors in the charts are kept as they were.

## 2.6.0 (15 Oct 2026, Prototype)

The full version history can be read before signing in, and every change since the first sketch is recorded in one place.

### Added

- **See the full version history** link on the sign-in screen. It opens this page without an account, so a past change can be looked up from any device.
- **Change log by commit** below: each change with its date, time and a link to the exact commit on GitHub.
- **Where each version came from** table: which versions were first written in claude.ai and which are in the GitHub history.
- A `CHANGELOG.md` file in the repository with the same history, readable on GitHub.

### Changed

- The version tag in the header now reads v2.6.

### Fixed

- The Versions page showed only the newest entry. Versions 2.4.0 down to 0.9.0, and the notes tables, ideas and decisions below them, were missing and now appear.

### Known limits

- Versions 0.9 to 2.4 were written before the GitHub repository existed, so they have no commit links. Their dates come from this log and the claude.ai artifact.
- The time of day for versions 0.9 to 2.3 was not recorded.

## 2.5.0 (15 Oct 2026, Prototype)

A visual refresh in the style of a macOS app. Every feature works as before.

### Added

- **Dark theme** and a **theme switch** in the header: System, Light or Dark. System, the default, follows the device setting, and the choice is remembered in this browser.
- Motion that answers a press: buttons, cards and tabs scale down slightly while held, the ticket drawer slides in, and board cards rise in once when the board opens.
- Toasts fade out instead of disappearing.

### Changed

- New look: neutral surfaces, one blue accent, a frosted toolbar, segmented tabs, grouped board columns, and a floating ticket drawer.
- The system font replaces the downloaded fonts, so the page loads with no external files.
- With Reduce motion turned on, movement is replaced by a short fade.
- On phones the header scrolls away and only the tab strip stays pinned, so more of the screen is left for the board.
- On narrow screens the Workflow diagram says it scrolls sideways.
- Colors, shadows and the theme switch styles now load from one shared stylesheet, also used by the Grant Support Mockups.

### Fixed

- Text in the Workflow diagram no longer runs past the edge of its boxes. The Evaluate step now reads "Three ratings".
- On phones, the pinned tab strip no longer lets page text show above it, buttons and chips are larger to tap, and opening View as table under a chart no longer stretches the page sideways.

### Known limits

- The animations and dark theme have not yet been checked on a phone or at every screen width.

## 2.4.0 (13 Oct 2026, Prototype)

A Dean and unit head account sees the whole office without changing any task.

### Added

- **Dean and unit head** sample account (Dr. Elena Navarro). Tabs: Overview (the board, read only), All requests, Monitoring (Tasks and Staff performance), Reports with downloads, New request, Notifications, Workflow.
- The unit head receives the missed-task messages, and any rule where the coordinator ticks Unit head, in Notifications and as an in-app message.
- The unit head can send a request and evaluate it like any requester, and the simulation now includes requests from the dean's office.
- The Who can do what table in Blueprint now shows the unit head as oversight, not as an editor.

### Changed

- Assigning, updating, availability, rules and the calendar stay with the coordinator, so the unit head cannot change a task by accident.

### Known limits

- A unit head who should approve target times or assignments needs a small approval step. It is in the ideas list.

## 2.3.0 (13 Oct 2026, Prototype)

Reports and Monitoring now show patterns, not only totals: charts, comparison with the previous period, and plain-language findings.

### Added

- **What stands out** at the top of every report: findings the data supports (late services, a falling on-time rate, uneven workload, busy hours, low evaluation response), each with a suggested next step.
- **Comparison with the previous period** on every headline number, with the direction marked better or worse.
- **Charts**: requests received and completed, on-time rate by week against a goal, time to complete against target by service, how long requests take, when requests arrive (weekday by hour), evaluation by criterion, and on-time rate by assistant. Each has hover details, keyboard access, and a table view.
- **Report goals** in Settings: the on-time goal (80% to start).
- The downloaded summary now carries the findings and the charts.
- **Sample history**: three weeks of generated requests (14 to 30 Sep) so trends and patterns have something to show. Replace with real data in use.

### Changed

- Monitoring Tasks gained a Patterns section. Staff performance gained the evaluation and weekly on-time charts.
- Each assistant keeps one colour across every chart.

### Known limits

- The sample history is generated. Treat its numbers as an illustration.
- Findings are rules of thumb (for example, a service over 120% of target). The thresholds are not editable yet.
- Charts are drawn for screens. Print the downloaded summary for paper.

## 2.2.0 (13 Oct 2026, Prototype)

Anyone can find an earlier request, and the coordinator can produce a summary and files for any period.

### Added

- **All requests** tab (called History for requesters): every ticket, completed or not, with search and filters for status, service, assistant, result, and request date. Open any row to see its full timeline.
- **Earlier requests from the same person** appear inside a ticket for the coordinator and assistants, with a link to see them all.
- The board's Completed column now links to the full list instead of only saying how many are earlier.
- **Reports** tab for the coordinator: pick a period, read a plain-language summary, and see tables by service, assistant, and department, plus a needs-attention list.
- **Downloads**: the request list or a report as a CSV file (opens in Excel), the report as a printable page, and a Copy summary button.

### Changed

- The idea "Reports export" from the 2.1 list is now built.

### Known limits

- Reports use the demo data and the demo clock.
- No charts, PDF, or scheduled emailing yet. The downloaded summary can be printed to PDF from the browser.
- Downloads and Copy depend on the browser allowing them. If a button is missing, the viewer has not allowed downloads for this page.

## 2.1.0 (13 Oct 2026, Prototype)

Working time follows an office calendar, evaluations close on their own with a reminder, and Monitoring is split into Tasks and Staff performance.

### Added

- **Settings** tab for the coordinator. **Holidays and non-working weekdays**: add one day or a range, with a name and a type. Weekends in a range are skipped.
- Every clock now skips those days: target times, the time tracker, time on hold, notification rules, and the evaluation window. Changing the calendar re-dates open requests.
- **Evaluation auto-close**: 3 working days after completion, a request closes without an evaluation. The window and the reminder are adjustable under Settings.
- **Reminder** 1 working day before it closes, sent by email and in-app. A closing notice goes to the requester and coordinator when it closes.
- The board card and the ticket show when the evaluation closes, and the timeline records the reminder and the closing.
- **Monitoring, Tasks**: task status, types of tasks with time to complete against target, open tasks, the evaluation queue, and requests by department.
- **Monitoring, Staff performance**: assignments right now, task outcomes, a new Evaluation section with response rate and low evaluations, and the ranking.
- Sample calendar entries and a sample request that closed without an evaluation.

### Changed

- Monitoring now opens on the Tasks view. The earlier Monitoring content is under Staff performance, with Assignments right now first.
- Average time to complete leaves out time on hold, to match the time tracker.
- Assistants see the Staff performance view only, as before.

### Known limits

- The calendar applies to the whole office. Closing a day for one person is still done with availability.
- Whole days only. Half-day closures are not supported.
- A request that closed without an evaluation cannot be reopened yet.
- Changing the calendar re-dates open requests only. Finished requests keep their result.
- Everything still lives in this browser tab and resets on reload.

## 2.0.0 (13 Oct 2026, Prototype)

Task updates with remarks, a time tracker that pauses on hold, evaluation in three parts, monitoring for the coordinator, and rules for when to notify.

### Added

- **Update** and **Put on Hold** buttons, each with a Remarks box. Both appear in the Timeline with time, author, and remarks.
- **Time tracker** on every ticket. Put on Hold pauses it and moves the target by the time on hold. Update leaves it running.
- **Requester messages and replies**, so the office can clarify an issue before work resumes.
- **Evaluation** of quality, punctuality, and expertise (1 to 5 stars each) with an optional comment.
- **Assignment by availability, function, and expertise**, with availability set by the coordinator or the assistant.
- **Monitoring**: completed on time, completed late, delayed now, most punctual, most accomplished, and who needs attention (low assignments or delays).
- **Notification rules**: at risk, missed (with reminders), not assigned, not started, and long hold, with choosable recipients.
- This Versions tab.

### Changed

- Statuses are now New, Assigned, In progress, On hold, and Completed. "Resolved" and "Done" are renamed.
- The Actions section is replaced by Update this task.
- The single star rating is now the average of the three evaluation ratings.
- Scoreboard is called Monitoring for the coordinator and has more measures.
- Hold reasons are written as remarks, with common reasons as shortcuts.

### Removed

- The Actions section.
- The hold-reason dropdown and the one-line "Mark done" note.

### Fixed

- Text typed in remarks and comments is kept when the simulation refreshes the screen.

### Known limits

- Data lives in this browser tab and resets on reload.
- Emails are previews only. Nothing is sent.
- Sign-in is a demo with sample accounts.
- Unrated tasks do not close on their own yet (added in 2.1.0).

## 1.0.0 (6 Oct 2026, Prototype)

First office version, with sign-in and Office Assistants A, B, and C.

### Added

- Sign-in with sample accounts and three roles.
- Catalog of 11 office services and a request form that fills in the signed-in user.
- Board, ticket drawer, scoreboard, notification center, workflow, blueprint, and a day simulation.

### Changed

- Moved from IT services to office administration tasks.

## 0.9.0 (6 Oct 2026, Concept)

First sketch, written as an IT service desk.

### Added

- Catalog, board, scoring, and notifications for IT services.

### Removed

- Replaced by version 1.0.

# Change log by commit

Every commit in the GitHub history, newest first. The version 2.6.0 commit is added when it is published.

| Commit | When (UTC+8) | Version | Change |
|---|---|---|---|
| [c61e20e](https://github.com/zefanonuevo/ccs-task-tracker/commit/c61e20e) | 15 Oct 01:21 | 2.5.0 | Mobile fixes: pinned tab bar, larger touch targets, inline favicon; View as table no longer widens the page. |
| [58e5f80](https://github.com/zefanonuevo/ccs-task-tracker/commit/58e5f80) | 15 Oct 01:08 | 2.5.0 | Colors, shadows and theme switch styles now load from the shared ccs-design stylesheet. |
| [48e9399](https://github.com/zefanonuevo/ccs-task-tracker/commit/48e9399) | 15 Oct 00:53 | 2.5.0 | README: live link and a note on the shared design system. |
| [5a2d047](https://github.com/zefanonuevo/ccs-task-tracker/commit/5a2d047) | 15 Oct 00:30 | 2.5.0 | Added the System, Light and Dark theme switch in the header. |
| [2a6f6d8](https://github.com/zefanonuevo/ccs-task-tracker/commit/2a6f6d8) | 15 Oct 00:27 | 2.5.0 | Added a scroll hint above the Workflow diagram on narrow screens. |
| [eeba0ee](https://github.com/zefanonuevo/ccs-task-tracker/commit/eeba0ee) | 15 Oct 00:26 | 2.5.0 | Mobile: the header scrolls away and only the tab strip stays pinned. |
| [cd602e9](https://github.com/zefanonuevo/ccs-task-tracker/commit/cd602e9) | 15 Oct 00:22 | 2.5.0 | Fixed Workflow diagram text running past its boxes with the system font. |
| [e634f7d](https://github.com/zefanonuevo/ccs-task-tracker/commit/e634f7d) | 15 Oct 00:20 | 2.5.0 | Mobile: scrolling tab strip fades at the edge; simulation controls tidied. |
| [e7253d3](https://github.com/zefanonuevo/ccs-task-tracker/commit/e7253d3) | 15 Oct 00:16 | 2.5.0 | Bumped the tracker to v2.5 and added its entry to this log. |
| [9f91ed9](https://github.com/zefanonuevo/ccs-task-tracker/commit/9f91ed9) | 15 Oct 00:16 | 2.5.0 | Redesigned the tracker as a macOS-style app. |
| [575ed48](https://github.com/zefanonuevo/ccs-task-tracker/commit/575ed48) | 14 Oct 23:49 | 2.4.0 | Imported the v2.4 prototype into GitHub from the claude.ai artifact (first commit). |
