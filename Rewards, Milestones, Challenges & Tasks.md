# Rewards, Milestones, Challenges & Tasks

## Changes in v2

1. Excusals lower the locked target and the Milestone completion count by the difficulty % of what was excused, with a preview; undoing an excusal reverses it (TSK-13 to TSK-15).
2. Adding a Milestone to a running reward raises the target with a preview; deleting one lowers it back (MS-32, MS-38 to MS-40, GR-4a).
3. Milestones can be added only in a reward's first 14 active days and while its balance is below target; the parent gets a reminder push on active days 3, 6, 9 and 12 (MS-38, MS-41).
4. Milestones are never standalone: they are deleted with their reward and close into history when it is achieved (MS-3, MS-42, GR-17). Orphaned Milestones (old MS-34 to MS-37) are removed.
5. After early completion, a Milestone's checkpoint windows keep running to its deadline (10.6, MS-19).
6. A Milestone that misses its deadline goes into review (MS-22a).
7. Checkpoints get the same 3-day grace period as shared windows (MS-17).
8. A correction within the 3-day grace period that breaks the streak behind a paid bonus revokes it; the child can qualify again (APR-19).
9. Confirming a challenge handover early approves everything still pending (CH-11).
10. Occurrence states: approved can no longer become excused; excusals can be undone; pending occurrences that lock are auto-approved (6.0, APR-18).
11. Shared window shares are topped up at window close, rounded up, and an empty window's bonus comes off the target (SSW-14, SSW-16a, SSW-21).
12. Cancelling a shared reward shows the remaining child's contribution and suggests pausing (SH-8).
13. Multiple guardians (ROL-1).
14. Wording: separate personal and shared target formulas (8.2); qualifying again starts a fresh confirmation window (CW-1); "eligible days" used consistently (MS-12); example 17.9 prize changed to 400.
15. Target changes are adjustments to the current target, rounded in the child's favour, never a recalculation; a change that brings the target to the balance reaches the reward at once (GR-4a). Renegotiation is defined: change difficulty or type a new target (GR-4b).
16. Every Milestone, required or optional, ends on or before the reward's end date. Milestone pauses are capped there, and a checkpoint that the cap makes unearnable comes off the target; extensions past it are blocked (GR-16, MS-22, MS-24).
17. Remaining checkpoints still pay after early completion (MS-21). A completed Milestone moves to history 3 days after its deadline, so the last checkpoint keeps its grace period (10.6, APR-10).
18. Excusals lower the completion count by the Milestone's own count ÷ planned ratio, cumulatively (TSK-13). On-time re-completion is judged by activity date (MS-20, 10.6).
19. Undoing an excusal is blocked during a confirmation window, and never restores a window headcount or a removed window bonus (TSK-14, TSK-15, SSW-17, SSW-21).
20. Removing a sibling takes their remaining planned points off the target, and future windows are recalculated without them (SH-7).
21. Activity on a reward's paused days never credits it (APR-16). Confirming a reward early also confirms a required Milestone still confirming (GR-14). A rejected Challenge's fail is final when its window closes (CW-8).

## 1. Overview

Golden Rewards is a parent-managed chore and goal system in which children earn points toward one tangible, parent-agreed prize — a Golden Reward. The parent picks the prize, the timeframe and the difficulty; the app calculates an achievable point target from the child's planned tasks and bonus opportunities, so the child never chases an arbitrary number. Milestones add outcome-based sub-goals, shared Golden Rewards let siblings work toward one prize together, and Challenges reward a consistent completion rate over a few days or weeks.

### Problem

Chore charts fail when targets feel arbitrary, when one bad day wipes out progress, and when rules shift without warning. Parents also lack a fair way to run one reward across siblings with different schedules and abilities.

### Goals

- Turn a prize the child wants into a target they can see is reachable from their own schedule.
- Reward consistency (streaks) and real outcomes (milestones), not just volume.
- Protect progress: missing a bonus means not earning it, never losing what was banked.
- Support one personal and one shared (sibling) Golden Reward per child, for children of any age, with one scoring engine.
- Keep the parent in control with low effort: one daily summary, automatic approval as a fallback, and a short window to catch dishonest claims.

### Success measures

| **Measure** | **Definition** |
| --- | --- |
| Reward completion rate | Share of activated Golden Rewards achieved by their planned end date or an agreed extension |
| Task completion rate | Approved occurrences ÷ eligible scheduled occurrences, per child, per Challenge period |
| Streak qualification rate | Share of checkpoint and shared streak windows in which each child qualifies |
| Challenge success rate | Share of Challenges whose final result is success |
| Parent effort | Share of submissions resolved by the parent before auto-approval |
| Correction rate | Rejected completions ÷ submitted completions (signals honesty issues or unclear tasks) |
| Prize rejection rate | Share of reached Golden Rewards, completed Milestones and successful challenges rejected in their confirmation window |

Targets for these measures are not yet set (see Section 19).

## 2. Users, roles and permissions

The parent configures and confirms everything; the child sees progress and submits completed tasks.

| **Action** | **Parent** | **Child** |
| --- | --- | --- |
| Create, edit, pause, extend, delete Golden Rewards, Milestones and Challenges | Yes | No |
| Schedule tasks, assign them to slots, link tasks to Milestones, select streak-linked tasks | Yes | No |
| Set difficulty, Milestone completion count, window length, streak lengths | Yes | No |
| Use the Prize Calculator and see prize values | Yes | No |
| Submit a task completion | Yes (records directly) | Yes, before the slot deadline only |
| Approve or reject task completions, including retrospectively | Yes | No |
| Mark an occurrence excused, or undo an excusal *(v2)* | Yes | No |
| Confirm a completed Milestone, a challenge result or a reached Golden Reward early (closes its confirmation window) | Yes | No |
| Reject a prize during its confirmation window (through corrections) | Yes | No |
| Confirm physical prize handover | Yes | No |
| Remove participants from a shared reward | Remove only (no mid-reward joins) | No |

Trust mode (child self-report without approval) is removed from this feature. Every completion is parent-approved, either explicitly or by the 72-hour auto-approval. Children never submit Milestone outcomes or challenge results: both are calculated by the app.

- **ROL-1** A household can have more than one guardian. Every guardian can take every parent action; when two act on the same item, the most recent action wins. The daily summary and event notifications go to all guardians, and every parent action is logged with who took it. In this document "parent" means any guardian. *(v2)*

## 3. Core principles

1. **Points are never a punishment.** No negative balances; points are never removed for misbehaviour. Missing a bonus means not earning it. The only removal is a parent correcting a dishonest or mistaken completion claim (Section 6.5). A prize can be rejected only through such corrections (Section 13).
2. **The parent is the final authority**, with automatic approval as a fallback so a busy parent never costs a child earned progress.
3. **The agreement is explicit.** Targets, budgets, completion counts, difficulty, streak requirements and windows lock at activation; later changes need an explicit parent action with a preview of effects. Locked numbers never change silently. Excusals, adding or deleting a Milestone, removing a participant, a shared window no child can earn and renegotiation change the target only through such a previewed action (GR-4a, GR-4b). *(v2)*
4. **One scoring engine.** Every approved occurrence is worth 10 points for every child. Difficulty shapes targets, streaks and thresholds; it never changes the task value.
5. **Early achievement is allowed.** A child can reach a reward, Milestone or challenge threshold before its planned end.
6. **Destructive actions are warned.** Deleting or cancelling a reward, Milestone or challenge always shows its consequences first.
7. **No retroactive credit.** Activity performed with no active destination never earns points later.
8. **Points have no cash value.** A prize's monetary value can help choose a timeframe (Section 9) but never enters any point calculation.

## 4. Glossary

| **Term** | **Meaning** |
| --- | --- |
| Golden Reward | A parent-agreed tangible prize with a locked point target and a 28–365 day timeframe. Personal (one child) or shared (two or more children). |
| Open (Golden Reward) | Active, paused, confirming, or past its end date awaiting review. Counts toward the one-per-type limit. |
| Occurrence | One scheduled instance of a task, assigned to one child, in one slot on one date. |
| Slot | The morning or evening time block an occurrence belongs to. Slot times are set app-wide. "Time block" means only this. |
| Routine task | A task that is not linked to a Milestone. |
| Milestone-linked task | A task linked to exactly one personal Milestone. |
| Streak-linked task | A task assignment the parent selects as counting toward a child's shared streak in a shared Golden Reward. |
| Greyed out points | Points shown for a submitted occurrence that is not yet approved. Provisional only. |
| Earned points | Points from approved occurrences and paid bonuses. Only earned points move balances, streaks and results. |
| Approved | An occurrence confirmed by the parent or auto-approved 72 hours after submission. |
| Excused | Marked by the parent (illness, holiday). Earns nothing, counts for nothing, breaks nothing, and lowers the target and completion count it would have counted toward (TSK-13). *(v2)* |
| Difficulty | Easy, Normal or Hard, set by the parent at setup of every Golden Reward, Milestone and Challenge. |
| Milestone | A personal sub-goal that always belongs to one personal Golden Reward *(v2)*, with milestone-linked tasks, a completion count, checkpoint bonuses and a completion bonus. |
| Milestone completion count | The number of approved milestone-linked occurrences that completes a Milestone. Locked at activation. |
| Checkpoint | A non-overlapping window inside a Milestone that pays a bonus once when the child completes a streak. |
| Shared streak window | A 7- or 14-day window in a shared Golden Reward that pays each qualifying child an equal share once. |
| Complete day | A scheduled day on which every relevant linked occurrence due that day is approved. |
| Available points | All planned task points plus all planned bonuses for a reward, computed at activation and adjusted only under GR-4a. *(v2)* |
| Target | Available points × difficulty percentage, rounded up, locked at activation. |
| Confirmation window | The 72 hours after a Golden Reward is reached, a Milestone completes or a challenge period ends, during which the parent can still correct occurrences. An item that qualifies again after being reopened starts a fresh window. *(v2)* |
| Voucher | The record issued when a Golden Reward's confirmation window closes; separate from the physical handover. |
| Challenge | A 3–28 day challenge judged on completion rate, and the non-point prize it unlocks. One name for both. |
| Challenge period | The length of a Challenge, excluding paused days. |
| Collaborative challenge | A Challenge with two or more children and one team prize. |
| Prize Calculator | An optional setup helper that suggests a Golden Reward timeframe from the prize's value. |
| Daily rate | The prize value per day the parent uses in the Prize Calculator, in their currency. |

## 5. Tasks, slots and scheduling

Every approved, eligible task occurrence earns exactly 10 points, regardless of difficulty, task type or linking.

### 5.1 Task rules

- **TSK-1** Points are awarded once per scheduled occurrence. Unplanned repetitions earn nothing extra.
- **TSK-2** Each occurrence is assigned to exactly one child. There are no joint occurrences; shared rewards and collaborative challenges pool individual contributions.
- **TSK-3** A task is either routine or linked to exactly one personal Milestone. Milestone-linked tasks earn the same 10 base points as routine tasks, count toward checkpoint streaks, and count toward the Milestone completion count.
- **TSK-4** A task assignment can additionally be selected as streak-linked for a shared reward, whether or not it is milestone-linked.
- **TSK-5** Schedule changes apply prospectively only. Past approved completions are never rewritten.
- **TSK-6** The app records the activity date separately from the approval timestamp. Late approval never makes a timely completion late.

### 5.2 Slots and due times

- **TSK-7** Every occurrence belongs to the morning or evening slot. Slot start and end times are configured app-wide, outside this feature.
- **TSK-8** The occurrence's due time is the end of its slot. A child cannot submit after it.
- **TSK-9** Recommended load: no more than 5 occurrences per slot and 10 per day per child. The app warns, but does not block, when a schedule exceeds either, or when the same task is scheduled more than once on the same day.

### 5.3 Excused occurrences

- **TSK-10** The parent can mark an occurrence excused. It earns no points and is excluded from challenge rates, Milestone completion counts and streak counts.
- **TSK-11** A day on which every relevant linked occurrence is excused is neutral for streaks: it neither advances nor breaks them. If some linked occurrences remain on that day, the day qualifies only if all of those are approved.
- **TSK-12** Excusals are always an explicit parent action and are never auto-approved.
- **TSK-13** Excusing an occurrence lowers the target of each open Golden Reward it would have credited (GR-4a), and, for a milestone-linked occurrence, lowers its Milestone's completion count. The count is reduced by ⌊ratio × excused linked occurrences⌋, recalculated over all excusals each time, never below 1. The ratio is the Milestone's completion count ÷ its planned milestone-linked occurrences, both as locked at activation. When the parent explicitly edits the count, the edited count becomes the new base, the ratio becomes the edited count ÷ the remaining non-excused planned occurrences, and only later excusals reduce it. The excusal screen previews the new target and count before the parent confirms. *(v2)*
- **TSK-14** Undoing an excusal reverses its TSK-13 changes exactly, with the same preview. Two things are not reversed: the child stays out of any window headcount the excusal removed them from (SSW-17), and a window bonus removed under SSW-21 stays removed. *(v2)*
- **TSK-15** The parent can undo an excusal while the occurrence is unlocked (APR-10), except while a reward it credits or its Milestone is in its confirmation window. It returns to Scheduled if its slot has not ended, otherwise to Missed, from where it can be approved retrospectively. *(v2)*

## 6. Submission, approval and correction

A child's submission shows greyed out points at once, but only approved completions move rewards, streaks, Milestones and challenges; any submission the parent hasn't acted on within 72 hours approves itself.

### 6.0 Occurrence states

| **State** | **Meaning** | **Can move to** |
| --- | --- | --- |
| Scheduled | Planned, not yet submitted | Pending (child submits before slot end), Approved (parent records), Missed (slot ends), Excused |
| Pending | Submitted by the child; shown as greyed out points | Approved (parent, automatically after 72 hours, or automatically when it locks *(v2)*), Missed (parent rejects), Excused |
| Approved | Earned; counts everywhere it applies | Corrected (parent rejects later). No longer to Excused *(v2)* |
| Missed | Not done, or rejected while pending | Approved (parent, retrospectively, while unlocked), Excused |
| Excused | Neutral; counts for nothing | Scheduled or Missed (parent undoes the excusal while unlocked, TSK-15) *(v2)* |
| Corrected | An approval later rejected; its base points removed | Final |

An occurrence becomes locked, and stays in its current state, under APR-10. A pending occurrence is approved automatically at the moment it locks (APR-18). *(v2)*

### 6.1 Submission

- **APR-1** The child can submit a task completion only before its slot ends. After the deadline only the parent can record it (6.4).
- **APR-2** Children submit task completions only. Milestone completion and challenge results are calculated by the app (Sections 10.5 and 12.3).
- **APR-3** Nobody marks a Golden Reward complete. It is reached automatically when its eligibility rules are met (Section 8.4).

### 6.2 Greyed out points and child feedback

- **APR-4** A submitted task shows immediate visual feedback to the child: its points appear as greyed out points (for example a grey segment of the progress bar).
- **APR-5** Greyed out points never count toward reward eligibility, voucher issue, Milestone completion, checkpoint or shared-window qualification. The only exception is the provisional challenge result shown at period end (CH-9).
- **APR-6** On approval, greyed out points become earned points.

### 6.3 Approval

- **APR-7** The parent approves or rejects pending submissions, typically from the daily summary (Section 15).
- **APR-8** A task submission not acted on within **72 hours of submission** is auto-approved, whether or not notifications were opened. It then counts exactly like a manual approval, dated on its activity date.
- **APR-9** Excusals and prize handovers are never auto-approved. Confirmation windows close automatically after 72 hours (Section 13).

### 6.4 Retrospective actions

- **APR-10** The parent can approve or reject an occurrence retrospectively, including occurrences the child never submitted, while the occurrence is unlocked. It is unlocked while any of these holds:
- a Golden Reward it credits is open;
- for a milestone-linked task: its Milestone is open — active, paused, complete with checkpoint windows or their 3-day results still running, in its confirmation window, or past its deadline awaiting review *(v2)*;
- a Challenge it belongs to is running, paused, or in its confirmation window.

When none holds, the occurrence is locked and cannot change.

- **APR-11** A retrospective approval earns base points for the reward(s) active (not paused) on the activity date. It does not reopen a checkpoint or shared-window result that has already closed (checkpoint and shared-window results close 3 days after the window ends — MS-17, SSW-12 *(v2)*).

### 6.5 Rejection and correction

- **APR-12** Rejecting a pending submission marks the occurrence missed. No points were ever earned.
- **APR-13** Rejecting an already approved completion (manual or automatic) is a correction, not a punishment. It removes that occurrence's 10 base points from every balance it was credited to that is still open.
- **APR-14** A correction never revokes a voucher already issued. It revokes a checkpoint bonus or shared-window share already paid only under APR-19. *(v2)* It can reopen a Milestone, a challenge or a reached Golden Reward that is still in its confirmation window (Section 13). Balances cannot go below zero.
- **APR-15** The child sees a neutral notice — e.g. "Not approved: Tidy room, Tuesday" — with an optional parent note. Points disappear without any penalty animation.

### 6.6 Earnings ownership

- **APR-16** Earnings belong to the reward(s) open and not paused on the occurrence's activity date (GR-10). *(v2)* If such a reward has since been achieved, deleted or cancelled, the occurrence is recorded in history only. It is never credited to a reward that started after the activity.
- **APR-17** All earnings triggered by one approval or correction — base points, any checkpoint or window share it completes, any Milestone completion or reopening, any completion bonus — are processed together before reward eligibility is evaluated.
- **APR-18** When a pending occurrence locks (for example because the parent confirmed its reward early), it is approved automatically and recorded in history; it credits nothing that has already closed. *(v2)*

### 6.7 Revoking a bonus after a correction *(v2)*

- **APR-19** A correction revokes a paid checkpoint bonus or shared-window share when both hold: the corrected occurrence's activity date is inside that window, and the correction is made before the window's result closes (3 days after the window ends). It applies only if, without the corrected occurrence, the child no longer has the required run of complete days in that window. The window then reopens for that child, who can qualify again under the normal rules; a revoked share leaves the headcount unchanged. After the result closes, paid bonuses and shares are final. *(v2)*

## 7. Difficulty

Difficulty is the single setting that shapes how demanding each item is. The parent sets it at setup of every Golden Reward, Milestone and Challenge; it defaults to Normal. There are no age profiles: the app does not store or use the child's age.

| **Difficulty** | **Golden Reward target** | **Milestone completion count** | **Suggested streak (checkpoints and shared windows)** | **Challenge threshold** |
| --- | --- | --- | --- | --- |
| Easy | 60% of available points | 60% of planned milestone-linked occurrences | 3 complete days | 60% completion rate |
| Normal | 80% of available points | 80% of planned milestone-linked occurrences | 5 complete days | 80% completion rate |
| Hard | 90% of available points | 90% of planned milestone-linked occurrences | 7 complete days | 90% completion rate |
- **DIF-1** A personal Golden Reward's difficulty is set by the parent at setup.
- **DIF-2** A shared Golden Reward has one team difficulty, set by the parent for that reward. It is never inherited from any participant's personal reward.
- **DIF-3** A Milestone has its own difficulty, set at setup. It drives the suggested completion count and checkpoint streak (Section 10).
- **DIF-4** A Challenge's difficulty is set per child. In a collaborative challenge each child can have a different difficulty (Section 12.4).
- **DIF-5** Difficulty locks at activation (or at a challenge's start). Changing it later needs an explicit parent action with a preview of effects.
- **DIF-6** Suggestions derived from difficulty (completion counts, streak lengths) are prefills; the parent can edit them within the allowed ranges.

## 8. Golden Rewards and point routing

A Golden Reward lasts 28–365 days, has a target locked at activation, and is reached the moment its earned balance reaches the target and any required Milestone is complete. A 72-hour confirmation window follows before the voucher is issued.

### 8.1 Limits

- **GR-1** A child can be in at most **one open personal** and **one open shared** Golden Reward at a time. "Open" means active, paused, confirming, or past its end date awaiting review. This is a hard limit.
- **GR-2** Every Golden Reward requires a planned end date. Duration must be **28 to 365 days**. Paused days do not count toward the 365-day maximum. The Prize Calculator can suggest a duration (Section 9).

### 8.2 Target

Personal Golden Reward:

\text{Target} = \left\lceil \text{Difficulty \%} \times \left( 10 \times \text{planned occurrences} + \text{planned milestone bonuses} \right) \right\rceil

Shared Golden Reward:

\text{Target} = \left\lceil \text{Team difficulty \%} \times \left( 10 \times \text{all participants' planned occurrences} + \text{planned shared window bonuses} \right) \right\rceil

*(v2: one formula per reward type.)*

- **GR-3** Planned occurrences are those scheduled within the reward's timeframe at activation, including days that fall outside any shared window. Bonuses are included at their full planned value. Bonuses are therefore part of the target, not points on top of it.
- **GR-4** The target is **locked at activation**. Schedule changes never recalculate it silently.
- **GR-4a** The target changes only through previewed parent actions: excusing or un-excusing an occurrence (TSK-13, TSK-14), adding a Milestone (MS-39), deleting a Milestone (MS-32), a Milestone pause that makes a checkpoint unearnable (MS-24), a shared window no child can earn (SSW-21), removing a participant (SH-7), or an explicit renegotiation (GR-4b). Each adjusts available points by the points added or removed, and changes the current target by the reward's difficulty % of that amount, rounded in the child's favour: a decrease is rounded up, an increase rounded down. The target is never recalculated from scratch, so a renegotiated target is kept. Bonuses or base points already earned are never affected. If a change brings the target to or below the earned balance, the reward is reached at once and its confirmation window starts; the preview warns of this beforehand (as in MS-31). *(v2)*
- **GR-4b** Renegotiation is an explicit parent action, in one of two ways: change the reward's difficulty, which changes the target by the difference in difficulty % × current available points (DIF-5); or type a new target between the earned balance + 1 and the available points. A typed target at or below the balance is allowed only with the warning that the reward will be reached at once. Either way the parent sees the old and new target before confirming, and the child sees a neutral notice: "Your goal changed". *(v2)*
- **GR-5** The app updates the forecast on every schedule change and warns the parent when remaining available points can no longer reach the target. It offers replanning: extend the timeframe, add earning opportunities, or renegotiate the target.
- **GR-6** Setup must make clear that, because bonuses are in the target, missed bonuses may require extra tasks or more time.
- **GR-7** Activation is blocked when there are zero earning opportunities or the target exceeds available points.

### 8.3 Point routing

Each approved eligible occurrence credits every applicable open reward independently — parallel credit, not a split pool.

| **Child's open rewards** | **Personal credit per occurrence** | **Shared credit per occurrence** |
| --- | --- | --- |
| Personal only | 10 | — |
| Shared only | — | 10 |
| Both | 10 | 10 |
| Neither | 0 (tracked only) | 0 (tracked only) |
- **GR-8** Milestone bonuses (checkpoint and completion) go exclusively to the child's personal reward.
- **GR-9** Shared window shares go exclusively to the shared reward.
- **GR-10** Points accrue only while a reward is active, confirming, or past its end date awaiting review — never while it is paused. Starting a new reward never credits earlier activity.

### 8.4 Eligibility, confirmation and achievement

- **GR-11** A reward is reached when its earned balance is at or above the target **and**, if the parent set one, its required Milestone is complete (including a Milestone still in its own confirmation window).
- **GR-12** If only the points condition is met, the child sees "Points achieved — milestone remaining". The balance is not reset.
- **GR-13** When reached, the reward enters its **confirmation window** (Section 13): the child sees "Reward reached — confirming", the voucher is held, earnings continue to credit the balance, and shared streak windows stay open.
- **GR-14** When the window closes — after 72 hours, or earlier if the parent confirms — the app issues one voucher, marks the reward achieved, records the final total and earning history, and resets that reward's balance to zero. Any connected Milestones still open close at the same moment (GR-17). *(v2)* Surplus points do not carry forward. Resetting one reward never affects the other. If the reward requires a Milestone, the voucher waits until both the Milestone's and the reward's windows have closed. Confirming the reward or its handover early also confirms a required Milestone still in its confirmation window; the confirmation screen says so. *(v2)*
- **GR-15** A voucher is never revoked once issued. The parent confirms the physical handover separately from the voucher; confirming the handover during the window also confirms the reward.
- **GR-16** Every Milestone, required or optional, must have a deadline on or before the reward's planned end date, including after a Milestone pause (MS-24) or extension (MS-22). A required Milestone can be set at setup or added later under MS-38 to MS-40. *(v2)*
- **GR-17** Early achievement is allowed. When a personal reward is achieved (its voucher issued), every connected Milestone closes and moves to history: its progress is recorded, unearned bonuses are forfeited, remaining checkpoint windows end, and future milestone-linked tasks become routine tasks. The Reward reached notification states this. *(v2)*

### 8.5 Changing the prize

- **GR-18** Replacing the prize (e.g. bike to RC car) keeps the balance and target unless the parent explicitly renegotiates. The Prize Calculator shows the new prize's suggested timeframe beside the current one for information only (PC-7).

## 9. Prize Calculator

The Prize Calculator helps a parent choose a fair timeframe for a prize of a given value. It suggests a duration; the target is still calculated only from the schedule and difficulty.

- **PC-1** The Prize Calculator is optional and is offered at setup of personal and shared Golden Rewards. It is not offered for Challenges.
- **PC-2** The parent enters the prize's value in the currency set in the app's user settings.
- **PC-3** The calculator uses the parent's **daily rate**: the prize value one day of effort is worth (e.g. 5 per day). There is no built-in default. The first time the calculator is used, the parent enters a daily rate and the app remembers it for later rewards. The parent can edit it in the app's user settings, outside this feature.
- **PC-4** Suggested timeframe:

\text{Suggested days} = \min\left(365,\ \max\left(28,\ \left\lceil \frac{\text{Prize value}}{\text{Daily rate}} \right\rceil \right)\right)

When the unclamped result is above 365, the app notes that the prize may suit a longer plan or a higher daily rate.

- **PC-5** The suggestion only prefills the reward's timeframe. The parent can type any duration within 28–365 days. The prize value never enters the target, the forecast or any other point calculation.
- **PC-6** The prize value is visible to the parent only. The child sees the prize and their progress, never its price.
- **PC-7** When the parent replaces a prize (GR-18), the calculator shows the new value's suggested timeframe beside the current timeframe. Extending or renegotiating remains a separate, explicit parent action.

## 10. Milestones and checkpoints

A Milestone is a personal sub-goal that completes automatically when the child reaches its completion count of approved milestone-linked occurrences. Its bonus budget is 50% of its planned milestone-linked task points, split equally between consistency checkpoints and an on-time completion bonus.

### 10.1 Structure and limits

- **MS-1** A Milestone has a name describing the outcome (e.g. "Read three books"), a difficulty, milestone-linked tasks, a completion count, 2–10 checkpoints, and a deadline. The name is descriptive only; it is not separately verified.
- **MS-2** Milestones are personal only. There are no shared Milestones.
- **MS-3** A Milestone can be drafted freely but activated only when connected to the child's open personal Golden Reward. It always belongs to exactly one reward: it is never standalone and never moves to another reward. It is activated with its reward at setup, or added to a running reward under MS-38. *(v2)*
- **MS-4** A child can have up to two concurrent active Milestones. Activating a third shows a warning recommending two, but is not blocked.
- **MS-5** Concurrent Milestones run in parallel, each with its own tasks, checkpoints, count and bonuses.

### 10.2 Bonus budget

- **MS-6** Budget = 50% of planned milestone-linked task points at activation. Example: 40 planned occurrences → 400 task points + 200 bonus points.
- **MS-7** The budget is locked at activation. Linked tasks added later earn base points only; removing future linked tasks never shrinks committed bonuses.
- **MS-8** Checkpoint pool = 50% × budget, rounded to the nearest point (halves up). Completion bonus = budget − checkpoint pool.
- **MS-9** The checkpoint pool is split equally between checkpoints; leftover single points go to the earliest checkpoints.

### 10.3 Checkpoints

- **MS-10** 2–10 non-overlapping checkpoint windows cover the Milestone's timeline.
- **MS-11** The checkpoint streak is prefilled from the Milestone's difficulty (Easy 3, Normal 5, Hard 7 complete days); the parent can edit it.
- **MS-12** The app suggests the largest checkpoint count from 2–10 that leaves each window at least twice the streak length in eligible days — days with at least one non-excused milestone-linked occurrence (recovery buffer). *(v2)* The parent can override.
- **MS-13** Feasibility: a window with fewer eligible days than the streak is blocked. A window between one and two streak-lengths is allowed with a warning that there is little room to recover from a miss.

### 10.4 Checkpoint streak rule

- **MS-14** A streak advances by one on each complete day: every milestone-linked occurrence due that day is approved.
- **MS-15** Unscheduled, fully excused and paused days are neutral. A missed due occurrence resets the streak.
- **MS-16** The child can restart at any time and still qualify if enough scheduled days remain in the window.
- **MS-17** Each checkpoint pays at most once, at the moment of qualification. A later miss never revokes it; a correction can only under APR-19. Streaks do not carry across windows. Approvals for activity inside a checkpoint window can still complete qualification for **3 days after the window ends**; after that the result is final. *(v2)*

### 10.5 Completion count and completion

- **MS-18** The completion count is prefilled as difficulty % × planned milestone-linked occurrences, rounded up. The parent can edit it from 1 up to the planned number. It locks at activation, and changes later only through excusals (TSK-13) or an explicit parent edit. *(v2)*
- **MS-19** The Milestone completes automatically the moment the count of approved milestone-linked occurrences reaches the completion count. Excused and paused-day occurrences do not count. Approved milestone-linked occurrences after completion keep counting, so a Milestone reopened by a correction can be completed again. *(v2)*
- **MS-20** Completion is on time when the activity date of the occurrence that reaches the count is on or before the deadline. This also applies to re-completion after a reopening (10.6), even when the deadline has passed by then. *(v2)*
    - On time: satisfies any reward prerequisite and earns the completion bonus.
    - Late: satisfies the prerequisite, no completion bonus.
    - Not completed: keeps blocking a reward that requires it.
- **MS-21** Early completion earns the completion bonus. Remaining checkpoint bonuses are not paid automatically: their windows keep running to the deadline and pay normally when the child qualifies (10.6). *(v2)*
- **MS-22** The parent can extend the deadline before it passes (bonus eligibility kept). After it passes, an extension restores the completion bonus only if the parent explicitly chooses to. An extension adds no checkpoint windows. An extension can never move the deadline past the reward's end date (GR-16); the parent must extend the reward first. *(v2)*
- **MS-22a** A Milestone not complete when its deadline passes moves to **past deadline, awaiting review**. The parent gets a daily reminder to extend the deadline, lower the completion count, or delete the Milestone. Until they decide, approved linked occurrences keep counting toward the completion count (completion will be late, MS-20) and earn base points; no new checkpoint windows start. A required Milestone in review keeps blocking its reward. *(v2)*
- **MS-23** The app updates the Milestone forecast on every schedule change or excusal and warns when remaining scheduled milestone-linked occurrences can no longer reach the completion count. It offers to extend the deadline or lower the count, with a preview.

### 10.6 Confirmation window and closing

When a Milestone completes, it enters a 72-hour confirmation window (Section 13). The parent is notified at once.

1. During the window the Milestone shows as complete to the child. Its completion bonus and prerequisite status apply, its linked occurrences stay unlocked, and its checkpoints continue.
2. A correction that drops the approved count below the completion count reopens the Milestone: the completion bonus is removed, any prerequisite on it becomes unmet again, and the Milestone continues. Re-completion is on time or late by the activity date of the occurrence that reaches the count (MS-20). Re-completion starts a fresh 72-hour confirmation window. *(v2)*
3. When the window closes — after 72 hours, or earlier if the parent confirms — the completion is confirmed. The Milestone stays open so its remaining checkpoint windows can run, and its linked tasks stay milestone-linked up to the deadline; tasks scheduled after the deadline become routine from the day after it. It moves to history once both the window has closed and the last checkpoint result has closed (3 days after the deadline, MS-17), or earlier when its reward is achieved (GR-17). This is not a deletion and shows no deletion warning. *(v2)*
4. On moving to history: linked occurrences lock and future milestone-linked tasks become routine tasks. The parent can choose from the completion notification to delete them instead. *(v2)*

### 10.7 Pause

- **MS-24** The parent can pause a Milestone. The deadline and checkpoint window clocks freeze, and the deadline shifts by the pause length, but never past the reward's end date (GR-16): at that cap the remaining windows are shortened instead. If a shortened checkpoint window ends up with fewer eligible days than its streak, its bonus is removed from available points and the target is lowered (GR-4a). The pause preview shows this. *(v2)*
- **MS-25** While a Milestone is paused, its linked occurrences still earn base points toward any open Golden Reward, but they do not count toward its completion count and are neutral for its streaks.
- **MS-26** A Milestone's own pauses last at most **14 days in total**. At 14 days it resumes automatically and the parent is notified.
- **MS-27** Pausing the connected Golden Reward also freezes the Milestone (LC-2). That freeze is governed by the reward's pause limit, not the Milestone's.

### 10.8 Deletion

- **MS-28** Deleting a Milestone always shows a warning first.
- **MS-29** Points and bonuses already earned from it stay in the connected reward's balance.
- **MS-30** If it is a reward's required Milestone, deletion removes the requirement. The warning says this may change the child's path to the reward.
- **MS-31** If the child's earned balance already meets the target and this Milestone was the only blocker, the reward is reached on deletion and its 72-hour confirmation window starts. The warning states this beforehand.
- **MS-32** The Milestone's unearned bonuses are removed from available points, and the target is lowered by the reward's difficulty % × those bonuses (GR-4a). The deletion warning previews the new target. *(v2)*
- **MS-33** Future milestone-linked tasks become routine tasks unless the parent deletes them. Linked occurrences lock for retrospective actions.

### 10.9 Adding a Milestone to a running reward *(v2)*

Old MS-34 to MS-37 (Orphaned Milestones) are removed: a Milestone is never standalone.

- **MS-38** A Milestone, required or optional, can be added to the child's running personal Golden Reward only within the reward's **first 14 active days** (paused days don't count), and only while the reward's earned balance is below its target. After that, a new Milestone needs a new reward.
- **MS-39** Adding a Milestone raises the target (GR-4a): available points rise by the Milestone's bonus budget plus 10 × its linked occurrences that were not already planned in the reward, and the target rises by the reward's difficulty % of that. A warning shows the old and new target, and the parent must confirm. The child sees a neutral notice: "Your goal changed: new Milestone added".
- **MS-40** If the added Milestone is required, the warning also states that the reward will now wait for this Milestone as well as the points. Its deadline must be on or before the reward's end date (GR-16).
- **MS-41** The parent receives a separate push notification on the reward's active days 3, 6, 9 and 12, e.g. "You can still add a Milestone to Bike reward until Sat 5 Dec (5 days left)". The reminders stop early once the child has two active Milestones (MS-4) or the reward's earned balance has reached its target.

### 10.10 When the reward is deleted *(v2)*

- **MS-42** Deleting a personal Golden Reward deletes all its Milestones with it, including their points and bonuses, which were part of the reward's balance (LC-13). The deletion warning lists each Milestone. Future milestone-linked tasks stay on the schedule as routine tasks unless the parent ticks "Also delete these tasks" in the warning. Each Milestone's progress is kept in history as a record only.
- **MS-43** When the reward is achieved, its Milestones close into history (GR-17).

## 11. Shared Golden Rewards and shared streak windows

A shared reward has one target, one balance and one team voucher; siblings stay motivated through repeating 7- or 14-day windows in which each child builds their own streak and earns an equal share of the window bonus.

### 11.1 Structure

- **SH-1** Participants: two or more children, fixed at activation. Children cannot join an open shared reward.
- **SH-2** Each participant's approved occurrences credit 10 points to the shared balance (routing table, Section 8.3).
- **SH-3** Target = team difficulty × (all participants' planned task points + all planned window bonuses), rounded up, locked at activation.
- **SH-4** There are no shared Milestones and no shared prerequisites. Milestone bonuses never enter the shared balance.
- **SH-5** On reaching the target the shared reward enters its confirmation window (GR-13). When the window closes: one team voucher is issued, the reward is marked achieved, and the shared balance resets to zero. Personal balances are unaffected.

### 11.2 Window calendar

- **SSW-1** The parent sets one window length for the whole team: **7 or 14 days**.
- **SSW-2** Windows run back to back from the activation date. Number of windows = whole windows that fit in the duration.
- **SSW-3** Days left at the end that don't fill a whole window get no window. Occurrences on those days still earn base points and count toward the target. The setup screen shows which days have no window.
- **SSW-4** Example: a 30-day reward with 14-day windows has 2 windows (days 1–28); days 29–30 have no window.

### 11.3 Streak-linked tasks

- **SSW-5** The parent selects which task assignments count toward each child's shared streak. All of the child's tasks are preselected; at least one must remain per child. Children can have different numbers (e.g. Dan 3, Zoe 2).
- **SSW-6** Streak-linked tasks stay individually owned and may also be milestone-linked. The selection controls streak qualification only; every approved occurrence still earns base points.

### 11.4 Streak length per child

- **SSW-7** An eligible day for a child is a day with at least one non-excused streak-linked occurrence assigned to them. Several tasks on one day make one eligible day.
- **SSW-8** The parent sets each child's streak length; children cannot set their own. The app prefills it as:

\text{Suggested streak} = \min\left(\text{Team-difficulty streak},\ \left\lfloor \frac{\text{Eligible days in window}}{2} \right\rfloor \right)

- **SSW-9** Allowed range: 2 up to the child's eligible days in the window. Above half of those days the app warns that recovery room is limited. If a child has fewer than 2 eligible days in a window, activation is blocked until the schedule or window length changes.
- **SSW-10** Each child's requirement is frozen at the start of each window. Schedule or streak-length edits apply from the next window.

| **Team difficulty (child with a daily schedule)** | **7-day window** | **14-day window** |
| --- | --- | --- |
| Easy (streak 3) | 3 | 3 |
| Normal (streak 5) | 3 | 5 |
| Hard (streak 7) | 3 | 7 |

A child scheduled twice a week has 4 eligible days in a 14-day window, so the suggestion is 2 at any difficulty.

### 11.5 Qualification

- **SSW-11** A complete day = every streak-linked occurrence assigned to that child and due that day is approved. The streak counts consecutive eligible days and can start on any day. Unscheduled and fully excused days are neutral. A missed day resets only that child's streak.
- **SSW-12** A child qualifies once per window. A later miss never removes qualification; a correction can only under APR-19. *(v2)* Streaks never carry into the next window. Approvals for activity inside a window can still complete qualification for **3 days after the window closes**; after that the result is final.

### 11.6 Window bonus

- **SSW-13** Maximum window bonus = 50% of the streak-linked task points planned in that window across all participants, rounded **up** to a multiple of the participant count.
- **SSW-14** Each qualifying child earns an equal share by headcount, regardless of their task count: share = maximum ÷ headcount, rounded up to a whole point. *(v2)*
- **SSW-15** Example: Dan has 3 and Zoe 2 streak-linked tasks daily; 14 days → 70 occurrences → 700 points → maximum 350 (already a multiple of 2) → 175 per qualifying child.

### 11.7 Payout and headcount

- **SSW-16** A child's share is credited immediately when the approval that completes their streak is processed, at the headcount at that moment.
- **SSW-16a** When the window's result closes (3 days after the window ends), every child who qualified is topped up to the full share for the final headcount. Example: in a window running days 15–28, Dan qualifies on day 19 at headcount 2 (+175); Zoe, who has not qualified, falls ill and is excused out of the rest of the window on day 20; at close Dan is topped up by 175 to the single-child share of 350. *(v2)*
- **SSW-17** The headcount is frozen at window start, with two exceptions that remove a child who has not yet qualified: excusals that make qualification impossible, and leaving the reward (11.8). A child who already qualified keeps their share and stays counted. A child removed by excusal stays out of that window's headcount even if the excusal is later undone; the undo restores only their task points and target change (TSK-14). *(v2)*
- **SSW-18** When the headcount shrinks, the remaining qualifiers' shares rise, because the full window bonus is divided among fewer children. This is intended: the full window bonus is part of the target, so an ill or departed sibling never takes their part of the window bonus away from the team. (Their excused task points come off the target under TSK-13.) *(v2)* Setup and the window view explain this to the parent.
- **SSW-19** Shared streak windows stay open while the reward is confirming. When the confirmation window closes and the reward is achieved, the current and all future windows close; no further shares are paid.
- **SSW-20** If the reward is extended, new whole windows are added for the extension period; the target is unchanged (Section 14).
- **SSW-21** If the headcount of a window reaches zero (every participant excused out of it), its maximum bonus is removed from available points and the target is lowered by team difficulty % × that maximum (GR-4a), previewed in the excusal that causes it. Undoing an excusal never restores it, since the headcount stays zero (SSW-17). *(v2)*

### 11.8 Leaving and cancellation

- **SH-6** Only the parent can remove a child. Points the child contributed stay in the shared balance.
- **SH-7** The leaver is excluded from all future windows. Their remaining planned task points come off available points, and the target drops by team difficulty % of them (GR-4a). Future windows are recalculated without them: each window maximum is recomputed from the remaining participants' streak-linked points and rounded up to the new participant count, and the target drops by team difficulty % of the difference. The current window keeps its full maximum (SSW-18). The removal warning previews the new target; the forecast updates and replanning is offered if the target is no longer reachable. *(v2)*
- **SH-8** If removing a child would leave one participant, the reward is cancelled. Before the parent confirms, a warning states that the shared balance will be deleted, shows how many of those points the remaining child contributed, and suggests pausing the reward instead. *(v2)* Earning history is kept as a record only.

## 12. Challenges

A Challenge succeeds when the task completion rate over its challenge period meets the difficulty threshold. It is judged on completion rate, never points; it never costs or deducts points, and it works with or without an open Golden Reward.

\text{Completion rate} = \frac{\text{Approved occurrences}}{\text{Eligible scheduled occurrences}} \times 100\%

### 12.1 Structure and limits

- **CH-1** A Challenge has one or more children, a challenge period of **3 to 28 days** (excluding paused days), a difficulty per child, and a prize. The prize is any non-point reward the parent defines (e.g. pizza night, family cinema time).
- **CH-2** A child can have up to two running Challenges. Starting a third shows a warning, but is not blocked.
- **CH-3** Challenges never spend, reduce or add to a Golden Reward balance.

### 12.2 What counts

- **CH-4** Every occurrence scheduled for the child in the challenge period counts once and equally: routine, milestone-linked and streak-linked, at any frequency. The parent does not select tasks.
- **CH-5** Excused occurrences, and occurrences on paused days, are excluded from both numerator and denominator.
- **CH-6** Milestone and window bonuses never enter the rate.
- **CH-7** Schedule edits apply prospectively: new occurrences enter from their effective date; removed future occurrences leave from that date.
- **CH-8** Zero eligible occurrences → the result is "No eligible tasks", not success.

### 12.3 Result and confirmation window

- **CH-9** The result is shown to the child the moment the challenge period ends. At that moment, occurrences still pending count as if approved (greyed out), because they will auto-approve within the window unless the parent rejects them.
- **CH-10** The challenge then enters a 72-hour confirmation window (Section 13). Parent approvals, rejections and retrospective approvals during the window update the result live: a fail can become a success, and a success can be withdrawn.
- **CH-11** The result becomes final when the window closes, or earlier when the parent confirms the prize handover. Confirming the handover early first approves every occurrence still pending in the challenge; the confirmation screen says so. *(v2)* The final result counts approved occurrences only.

### 12.4 Thresholds and collaborative challenges

- **CH-12** A single-child challenge succeeds when the child's completion rate is at or above their difficulty threshold (Easy 60%, Normal 80%, Hard 90%). Required completions round up (80% of 12 = 10).
- **CH-13** A collaborative challenge (two or more children) has one team prize, won or lost together. It succeeds when the **average of each child's own completion rate** is at or above the **average of each child's own threshold**. Each child counts equally regardless of task count.
- **CH-14** Example: Dan (Normal, 80%) completes 19 of 20 = 95%; Zoe (Easy, 60%) completes 5 of 10 = 50%. Team rate (95 + 50) ÷ 2 = 72.5% vs team threshold (80 + 60) ÷ 2 = 70% → success.

### 12.5 Editing, pause, extension and deletion

- **CH-15** Difficulty locks when the challenge period starts; changing it needs an explicit parent action with a preview (DIF-5).
- **CH-16** The parent can pause a challenge. The period clock freezes and the end date shifts by the pause length. Pauses last at most **7 days in total**; at 7 days the challenge resumes automatically and the parent is notified. Pausing a collaborative challenge pauses it for every child.
- **CH-17** The parent can extend a challenge before its period ends, or during its confirmation window after a fail. The total period must stay within 28 days, excluding paused days. The thresholds stay unchanged, and the result is recalculated at the new end date, which starts a fresh 72-hour confirmation window. *(v2)*
- **CH-18** Deleting a challenge always shows a warning first.

## 13. Confirmation windows and rejected prizes

Every prize — a reached Golden Reward, a completed Milestone, a successful Challenge — is shown to the child at once, then held for 72 hours so the parent can still catch dishonest claims.

### 13.1 Confirmation window

- **CW-1** A confirmation window lasts **72 hours** from the moment a Golden Reward is reached, a Milestone completes, or a challenge period ends. An item that qualifies again after being reopened, or a challenge whose period was extended, starts a fresh 72-hour window. *(v2)*
- **CW-2** The parent can close a window early by confirming the item. Confirming a prize handover also confirms it.
- **CW-3** During the window, earnings continue to credit open balances, and linked occurrences stay unlocked for retrospective actions.
- **CW-4** The daily summary flags every item whose window closes within the next 24 hours.

### 13.2 Rejecting a prize

- **CW-5** A prize is rejected only by correcting the occurrences the child gamed (APR-13). The parent cannot reject a prize without naming at least one dishonest or mistaken occurrence.
- **CW-6** If the item no longer qualifies after the corrections, it is rejected. If it still qualifies, the prize stands.
- **CW-7** Corrections remove base points and any Milestone completion bonus that no longer applies. Checkpoint bonuses and shared-window shares already paid stay, unless the correction falls under APR-19. *(v2)*
- **CW-8** A rejected Golden Reward or Milestone reopens. If its deadline or end date has not passed, it keeps running and the child can continue earning toward it. If it has passed, the parent is prompted to **extend, edit, or delete** it, with a daily reminder until they decide. A rejected Challenge is a fail: the parent can still extend it during its confirmation window (CH-17), and the fail is final when the window closes (CH-11). *(v2)*
- **CW-9** The child sees a neutral notice, e.g. "Not approved: Bike reward", with an optional parent note and no penalty animation.

## 14. Lifecycle: pause, end date, extension, deletion, cancellation

A Golden Reward moves through draft → active ⇄ paused → past end date (under review) → confirming → achieved, or ends early by deletion or cancellation. A rejected prize returns it to active, or to review if its end date has passed.

| **State** | **Earns points** | **Windows and deadlines** | **Counts toward one-per-type limit** |
| --- | --- | --- | --- |
| Draft | No | Not started | No |
| Active | Yes | Running | Yes |
| Paused | No | Frozen | Yes |
| Past end date, awaiting review | Base points only | No new windows | Yes |
| Confirming (reached, voucher held) | Yes | Current windows stay open | Yes |
| Achieved | No | Closed | No |
| Deleted or cancelled | No; balance deleted | Closed | No |

### 14.1 Pause

- **LC-1** Pausing keeps the balance and stops new earnings.
- **LC-2** It also stops the calendar: window clocks and connected Milestone deadlines freeze, and the end date shifts by the pause length. A partly completed window resumes where it stopped.
- **LC-3** A pause lasts at most **14 days in total per reward**. At 14 days the reward resumes automatically and the parent is notified.
- **LC-4** Paused days do not count toward the 365-day maximum.
- **LC-5** Pausing a shared reward pauses it for every participant.

### 14.2 End date and review

- **LC-6** The end date is a planning and review date, not an expiry.
- **LC-7** If the target is not met by the end date, the parent is asked to review: extend the timeframe, edit it (for example agree a replacement prize), or delete it as a separate warned action.
- **LC-8** Until the parent decides, the reward stays open and keeps earning base points, with no new streak windows. The parent gets a daily reminder.

### 14.3 Extension

- **LC-9** Total duration after extension must stay within 365 days (excluding paused days).
- **LC-10** An extension never raises the target.
- **LC-11** For shared rewards, the extension adds whole windows only; their bonuses are added to the forecast, not the target. Leftover days get no window (SSW-3).

### 14.4 Deleting a Golden Reward

- **LC-12** Deletion is always preceded by a warning explaining the consequences.
- **LC-13** The reward's entire balance is deleted, including points from linked tasks and bonuses.
- **LC-14** Connected Milestones are deleted with the reward (MS-42). The warning lists them and offers to delete their future tasks too; otherwise those tasks become routine. *(v2)*

### 14.5 Cancelling a shared reward

- **LC-15** A shared reward is cancelled when removing a participant would leave only one child (SH-8). Cancellation behaves like deletion: warning first (showing the remaining child's contribution and suggesting a pause), balance deleted, history kept as a record. *(v2)*

### 14.6 Summary across item types

|  | **Golden Reward** | **Milestone** | **Challenge** |
| --- | --- | --- | --- |
| Duration | 28–365 days | Deadline on or before the connected reward's end date | 3–28 days |
| Difficulty | Set at setup; shared: one team difficulty | Set at setup | Set per child at setup |
| Pause limit (total) | 14 days | 14 days (own pauses) | 7 days |
| Completes when | Earned balance ≥ target (+ required Milestone) | Approved linked count ≥ completion count | Period ends with rate ≥ threshold |
| Confirmation window | 72 hours | 72 hours | 72 hours |
| Extension | Within 365 days; target unchanged | Before deadline; after it only with explicit bonus choice; never past the reward's end date | Before end or after a fail; within 28 days |
| Deletion | Warned; balance deleted | Warned; earned points stay | Warned |

## 15. Notifications and child-facing feedback

The parent gets one summary a day at the end of the evening slot plus a few event notifications; the child gets instant feedback on every submission and a neutral notice on every rejection.

### 15.1 Parent

| **Notification** | **When** | **Content** |
| --- | --- | --- |
| Daily summary | End of the evening slot, only on days with pending items or open confirmation windows | All pending submissions; items that will auto-approve within the next 24 hours; confirmation windows closing within 24 hours |
| No per-completion notification | — | Individual submissions are never pushed one by one |
| Milestone completed | When a Milestone completes | Confirmation window open; option to delete future milestone-linked tasks (otherwise they become routine) |
| Reward reached | When a Golden Reward is reached | Confirmation window open; voucher held; connected Milestones will close when the voucher is issued *(v2)* |
| Challenge result | When a challenge period ends | Provisional result; confirmation window open; extend option after a fail |
| End-date review | Daily from the end date until the parent decides | Target status and the extend, edit or delete choice |
| Rejected prize decision | Daily after a rejection whose period, deadline or end date has passed | Extend, edit or delete |
| Pause auto-resume | When a reward's or Milestone's pause reaches 14 days, or a challenge's reaches 7 | Item has resumed |
| Forecast warning | When a schedule change, excusal, deletion or leaver makes a target or completion count unreachable | Gap and replanning options |
| Milestone window reminder *(v2)* | Separate push on a personal reward's active days 3, 6, 9 and 12; stops early per MS-41 | Days left to add a Milestone, and the last date |
| Milestone deadline review *(v2)* | Daily from a Milestone's deadline until the parent decides (MS-22a) | Extend, lower the count, or delete |
- **NT-1** Submissions made after the summary is sent appear in the next day's summary. Every submission appears in at least two summaries before it auto-approves.

### 15.2 Child

- **NT-2** Every submission shows immediate visual feedback, with its points shown as greyed out points.
- **NT-3** Approval turns greyed out points into earned points.
- **NT-4** A rejected submission or correction shows a neutral notice ("Not approved: Tidy room, Tuesday") with an optional parent note. Points disappear without a penalty animation.
- **NT-5** The child sees checkpoint and shared-window qualification, Milestone completion, challenge results and reward progress as they happen (celebration design is out of scope here).
- **NT-6** "Points achieved — milestone remaining" is shown when the points target is met but a required Milestone is not.
- **NT-7** "Reward reached — confirming" is shown while a reached Golden Reward is in its confirmation window.
- **NT-8** A rejected prize shows a neutral notice ("Not approved: Bike reward") with an optional parent note.
- **NT-9** The child never sees a prize's monetary value.
- **NT-10** When a Milestone is added to a running reward, the child sees a neutral notice: "Your goal changed: new Milestone added". When the target is renegotiated (GR-4b), the notice is "Your goal changed". *(v2)*

## 16. Validation, warnings and rounding

The app blocks only what is impossible and warns about what is tight; it never changes a locked number silently.

### 16.1 Blocks (activation not allowed)

- Golden Reward duration outside 28–365 days, or no end date.
- A child would have a second open personal or a second open shared Golden Reward.
- Zero earning opportunities, or target above available points.
- A Milestone activated without a connection to the child's open personal reward.
- A Milestone whose deadline is after the reward's end date, including through an extension. *(v2)*
- A Milestone added to a running reward after its first 14 active days, or once its earned balance has reached the target. *(v2)*
- A Milestone completion count below 1 or above its planned milestone-linked occurrences.
- A checkpoint or shared window with fewer eligible days than the required streak, or a shared-window child with fewer than 2 eligible days.
- A shared reward with fewer than two participants, or a child with no streak-linked task.
- A Challenge period outside 3–28 days (excluding paused days), including after an extension.
- A Golden Reward extension beyond 365 days (excluding paused days).

### 16.2 Warnings (allowed after confirmation)

- Streak longer than half the eligible days in its window.
- A third concurrent Milestone.
- A third running Challenge for a child.
- More than 5 occurrences in a slot, more than 10 in a day, or the same task twice on one day.
- Remaining available points can no longer reach the target, or remaining milestone-linked occurrences can no longer reach the completion count.
- Excusing or un-excusing an occurrence, or adding or deleting a Milestone, with a preview of the new target or completion count. *(v2)*
- Every deletion, cancellation and participant removal, with its consequences.
- Deleting a required Milestone when the reward would be reached at once.
- A Prize Calculator suggestion that exceeds 365 days before clamping.

### 16.3 Rounding

| **Quantity** | **Rule** |
| --- | --- |
| Milestone bonus budget | 50% of planned milestone-linked task points (always whole for 10-point tasks) |
| Checkpoint pool | 50% × budget, nearest whole point, halves up |
| Completion bonus | Budget − checkpoint pool, exact |
| Individual checkpoint | Pool ÷ count; leftover single points to the earliest checkpoints |
| Milestone completion count | Difficulty % × planned milestone-linked occurrences, rounded up |
| Shared window maximum | 50% of planned streak-linked points in the window, rounded up to a multiple of the participant count |
| Golden Reward target | Rounded up to the next whole point at activation |
| Target change (GR-4a, GR-4b) *(v2)* | Difficulty % × points added or removed, rounded in the child's favour: decreases up, increases down |
| Shared window share *(v2)* | Maximum ÷ headcount, rounded up to a whole point |
| Completion count after excusals *(v2)* | Reduced by ⌊count ÷ planned ratio × total excused linked occurrences⌋, minimum 1 (TSK-13) |
| Challenge required completions | Rounded up |
| Prize Calculator suggestion | Rounded up to whole days, then clamped to 28–365 |

## 17. Worked examples

The examples below run the rules end to end; every figure is computed from the rules above. Assume the parent approves each evening unless stated.

### 17.1 Personal reward with a gamed Milestone — Maya, Normal, 28 days

Setup: two routine tasks daily (make bed, tidy toys) and a required Milestone "Read three books" (Normal, deadline day 28) with one milestone-linked task daily (read 15 minutes).

| **Item** | **Calculation** | **Points** |
| --- | --- | --- |
| Planned task points | (2 + 1) × 28 = 84 occurrences × 10 | 840 |
| Milestone budget | 50% × 280 milestone-linked task points | 140 |
| Checkpoint pool | 50% × 140 | 70 |
| Completion bonus | 140 − 70 | 70 |
| Checkpoints | Streak 5 (Normal); largest count with ≥ 10 days per window = 2 windows of 14 days; 70 ÷ 2 | 35 each |
| Completion count | ⌈80% × 28⌉ | 23 occurrences |
| Available points | 840 + 140 | 980 |
| Target (Normal 80%) | 0.8 × 980 | 784 |

Run:

1. Day 3: Maya misses "make bed". It is a routine task, so her reading streak is unaffected. Checkpoints pay 35 on day 5 and 35 on day 19.
2. Day 23: the 23rd reading is approved, so the Milestone completes on time and pays 70. Balance: 68 approved occurrences × 10 + 35 + 35 + 70 = 820 ≥ 784, and the required Milestone is complete. Maya sees "Reward reached — confirming"; the voucher is held. Both 72-hour windows start.
3. Day 24: after the day's approvals (+30, balance 850), the parent finds the reading on days 21–23 was faked and corrects those 3 occurrences. That removes 30 base points; the count drops from 24 to 21, so the Milestone reopens and its 70 bonus is removed. Checkpoint 2 stays, because its streak (days 15–19) is not broken by these corrections (APR-19). *(v2)* Balance: 750. The reward is no longer reached and keeps running. Maya sees "Not approved" notices.
4. Day 26: the count reaches 23 again, still on time, so the Milestone completes again (+70). Balance: 750 + 60 + 70 = 880 → "Reward reached — confirming" again, and fresh 72-hour windows start for both. *(v2)*
5. Days 27–28 add 60 during the window → 940. Both windows close on day 29: voucher issued, final total 940 recorded, balance reset to 0. The Milestone closes into history with the reward (GR-17) and "Read 15 minutes" becomes a routine task. *(v2)*

### 17.2 Shared reward with a sibling out ill — Dan and Zoe, Normal, 30 days, 14-day windows

Setup: Dan has 3 streak-linked tasks and 1 routine task daily (the parent deselected it); Zoe has 2 streak-linked tasks daily. Two windows (days 1–14, 15–28); days 29–30 have no window.

| **Item** | **Calculation** | **Points** |
| --- | --- | --- |
| Planned task points | Dan 4 × 30 + Zoe 2 × 30 = 180 occurrences × 10 | 1,800 |
| Window maximum | 50% × (3 + 2) × 14 × 10 = 350; multiple of 2 already | 350 per window |
| Window bonuses | 2 × 350 | 700 |
| Available points | 1,800 + 700 | 2,500 |
| Target (Normal 80%) | 0.8 × 2,500 | 2,000 |
| Suggested streaks | Dan min(5, 7) = 5; Zoe min(5, 7) = 5 | — |

The parent keeps Dan at 5 and sets Zoe to 3; both are within range and at or below half the window, so no warning.

1. Window 1: Zoe completes days 1–3 → qualifies on day 3, +175. Dan misses one task on day 3, his streak resets, then days 4–8 are complete → qualifies on day 8, +175. Balance after day 14: Dan 55 × 10 + Zoe 28 × 10 + 350 = 1,180.
2. Window 2: Zoe completes day 15, misses a task on day 16, then falls ill. On day 17 the parent excuses all her occurrences for days 17–28. She now has no eligible days left, so she leaves the window 2 headcount (SSW-17).
3. Day 19: Dan completes his fifth straight day → qualifies. Earned bonus = 350 × 1 ÷ 1 = 350, the full window (SSW-18). Balance: 1,180 + 200 (Dan days 15–19) + 30 (Zoe days 15–16) + 350 = 1,760.
4. Excusing Zoe's 24 occurrences (days 17–28) removes 240 points from available points: the excusal preview shows the target falling from 2,000 by 0.8 × 240 = 192 to 1,808 (TSK-13, GR-4a), and the parent confirms. *(v2)*
5. Dan earns 40 a day from day 20. After day 21 the balance is 1,760 + 2 × 40 = 1,840 ≥ 1,808 → "Reward reached — confirming"; team voucher held; window 2 stays open. *(v2)*
6. Days 22–24 add 120 during the window → 1,960. The window closes at the end of day 24 with no rejection: team voucher issued, 1,960 recorded, balance reset to 0, and window 2 closes. Days 25–30 are tracked only. *(v2)*

### 17.3 Both open — one approval, two balances

Dan also has a personal reward with a Milestone like Maya's (2 checkpoints of 35). His "read" task is both milestone-linked and streak-linked. On day 7 the parent approves Dan's evening read, which completes both his checkpoint streak and his shared-window streak. One action produces:

| **Balance** | **Credit** |
| --- | --- |
| Personal | 10 base + 35 checkpoint = 45 |
| Shared | 10 base + 175 window share = 185 |

The base points are parallel credit, not 10 split in two. Milestone bonuses never reach the shared balance; window shares never reach the personal one.

### 17.4 Late approval, auto-approval and correction

1. Tuesday 20:15: Zoe submits "tidy toys" before the evening slot ends. She immediately sees +10 as greyed out points.
2. The parent ignores Tuesday's, Wednesday's and Thursday's summaries. Friday 20:15, 72 hours after submission, the completion auto-approves and becomes 10 earned shared points, dated Tuesday.
3. The following Monday the parent learns the toys were never tidied and corrects it. The shared reward is still open, so 10 points are removed; Zoe sees "Not approved: Tidy toys, Tuesday". Had that Tuesday completed her window streak, her 175 share would be revoked only if the correction came within 3 days after that window ended (APR-19); otherwise it stays. *(v2)*

### 17.5 Window grace period

Dan's qualifying day is the last day of a window (day 14), but the parent approves it on day 16: it still counts, because approvals for in-window activity can complete qualification until day 17. Approved on day 18, the same occurrence earns its 10 base points but the window result stays closed. Checkpoint windows follow the same rule (MS-17). *(v2)*

### 17.6 Deleting a required Milestone

Leo's personal reward target is 900 and requires the Milestone "Learn to swim 25 m". His earned balance is 930. The parent deletes the Milestone. The warning first states that the requirement will be removed and the reward reached at once. On confirmation: requirement removed, the target drops by 80% of the Milestone's unearned bonuses (MS-32) *(v2)*, reward reached, 72-hour confirmation window starts. With no corrections, the voucher is issued when the window closes and the balance resets to 0. Bonuses Leo earned from the Milestone were already in the 930 and stay part of the recorded total.

### 17.7 Shared reward cancelled by a leaver

A two-child shared reward has 1,200 points banked. The parent removes one child. The warning states that only one participant would remain, so the reward will be cancelled and its 1,200 points deleted; it shows how many of those points the remaining child contributed and suggests pausing instead. *(v2)* On confirmation the reward is cancelled; its history is kept as a record, and neither child's personal reward changes.

### 17.8 Collaborative challenge with pause and extension — "Tidy fortnight"

Setup: 14 days; Dan on Normal (80%) with 4 tasks a day (56 occurrences); Zoe on Easy (60%) with 2 a day (28 occurrences). Team threshold = (80 + 60) ÷ 2 = 70%. Prize: pizza night.

1. The parent pauses the challenge for 2 days (a weekend away). The clock freezes and the end date shifts by 2 days; tasks on paused days don't count.
2. Period ends: Dan 40/56 = 71.4%, Zoe 18/28 = 64.3%. Team average 67.9% < 70%, so the fail shows at once.
3. That evening, within the confirmation window, the parent extends the challenge by 4 days (18 days total, within the 28-day cap). This adds 16 occurrences for Dan and 8 for Zoe; both complete them all.
4. New period end: Dan 56/72 = 77.8%, Zoe 26/36 = 72.2%. Team average 75% ≥ 70% → success, shown at once. Dan is below his own 80%, but the team passes on the averages (CH-13).
5. The next day the parent confirms the pizza night handover, closing the window early. Nothing is pending; had anything been, it would have been approved first (CH-11). *(v2)* The result is final.

### 17.9 Prize Calculator — a bike worth 400 *(v2)*

The parent's daily rate is 4 per day, in the currency from their settings.

1. Suggested timeframe: ⌈400 ÷ 4⌉ = 100 days (within 28–365). The parent accepts it.
2. Schedule: 2 routine tasks daily, plus a Milestone "Ride 1 km without stopping" (Normal) with 1 milestone-linked task daily for the 100 days.

| **Item** | **Calculation** | **Points** |
| --- | --- | --- |
| Planned task points | 3 × 100 = 300 occurrences × 10 | 3,000 |
| Milestone budget | 50% × 1,000 milestone-linked task points | 500 |
| Available points | 3,000 + 500 | 3,500 |
| Target (Normal 80%) | 0.8 × 3,500 | 2,800 |
3. The prize value of 400 never enters the calculation: the same schedule for a cheaper prize would give the same 2,800 target. The prize's value only shaped the 100-day timeframe.
4. Clamping: a prize worth 100 at the same rate gives 25 days and is suggested as 28; a prize worth 2,000 gives 500 days and is suggested as 365, with a note that it may suit a longer plan or a higher daily rate.

## 18. Dependencies

- Morning and evening slot start and end times, configured app-wide (TSK-7). The daily summary and the child's submission deadline depend on them.
- Push notification delivery for the daily summary, event notifications and reminders.
- App user settings providing the parent's currency and the Prize Calculator daily rate (PC-2, PC-3). Editing the daily rate there is outside this feature.

## 19. Open items

- Targets for the success measures in Section 1 are not yet set.
- Celebration design for qualification, completion and achievement (NT-5) is out of scope for this document.
