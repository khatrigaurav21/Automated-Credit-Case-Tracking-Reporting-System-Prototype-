# Automated-Credit-Case-Tracking-Reporting-System-Prototype (Zapier + Google Sheets)-
Prototype demonstrating a no-code automation to notify analysts and auto-generate status summaries when credit cases are added or updated.

**Project context:** A simplified prototype based on a process I led as Unit Lead at the Royal Bank of Scotland — where credit case intake and queue monitoring created a persistent operational bottleneck.

---

## LinkedIn Post (final)
**How many hours do skilled analysts lose just checking if new cases have been added to their queue?**  
In my time as a Unit Lead at the Royal Bank of Scotland, I saw firsthand how this necessary but manual process slowed credit operations.

**The Context:**  
In our corporate credit unit, analysts managed case writing for business clients. Every day, new cases were added to a shared log — each representing a client’s credit application that needed to be reviewed and documented. Analysts often had to *manually monitor* that log throughout the day to see if new cases appeared. At the end of the week, a senior analyst would compile a summary of all completed and pending cases to share with stakeholders. This process was repetitive, time-consuming, and dependent on manual updates — creating delays and occasional misses when workloads were high.

**The Solution (prototype):**  
To explore how modern tools could improve this workflow, I built an **automated credit case tracking system** using **Zapier**.  
- The **Google Sheet** serves as the shared case log.  
- **Zapier** continuously monitors the sheet for new entries or status changes.  
- When a new case is added or an existing one is completed, the automation instantly notifies the assigned analyst and updates the manager via an automated email summary.  

This automation replaces the need to manually check queues, providing real-time visibility and eliminating reporting delays.

> **PM takeaway:** This is the mindset I bring to project management — solving operational inefficiencies with practical, no-code automation. By integrating simple tools like Zapier into existing systems, we can improve visibility, reduce wait times, and let skilled professionals focus on high-value work like analysis and exception handling, rather than data entry.

---

## What’s in this repo
- `assets/` — demo recording, GIF, screenshots
- `docs/HOWTO.md` — step-by-step instructions to reproduce the Zap (manual)
- `docs/architecture.png` — simple flow diagram
- `samples/sample-cases.csv` — sample case log to import into Google Sheets
- `README.md` — (this file)
- `CONTRIBUTING.md` — how to contribute or suggest edits

---

## How to reproduce (high level)
1. Copy `samples/sample-cases.csv` into a new Google Sheet (or create your own case log).
2. In Zapier, create a new Zap:
   - Trigger: **Google Sheets → New or Updated Spreadsheet Row**
   - Action: Format or Filter (optional) to select only relevant status changes
   - Action: **Email by Zapier** (or Gmail) to send a templated status summary to stakeholders OR
             **Slack → Send Channel Message** to notify a team channel.
3. Test the Zap: add a new row in the sheet and confirm the email/Slack message arrives.
4. Export a short recording (screen capture) of the test for the LinkedIn proof.

> See `docs/HOWTO.md` for more granular steps and recommended Zap field mappings.

---

## Assets & Proof quality
- Demo must be ≤ 30s, clear, and minimal UI. Include captions overlayed or short text in README describing each clip.
- Prefer MP4 for clarity; GIF for embedded preview in README (smaller GIFs work best).
- If the video is large, consider Git LFS (see note below).

---

## Notes on large files
If your demo video is larger than 50MB, consider:
- Using **Git LFS** to store large binary files, or
- Hosting the video on YouTube (unlisted) or Vimeo and embedding a link in the README instead of uploading the MP4 to the repo.

---

## Contributing
Please open an issue for suggestions or to request help reproducing the Zap steps. Pull requests are welcome for improving docs or visual assets.

